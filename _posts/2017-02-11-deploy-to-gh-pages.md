---
layout: post
title: Deploy to GH-Pages with Travis-CI
tags:
- deploy
- gh-pages
- travis-ci
---

This setup will deploy content from a `dist/` folder to GH-Pages via Travis-CI.

## Repository
Create or use one of your existing repositories on GitHub. Clone it, and create a `master` branch if you don't already have one. Use this branch for the rest of the setup.

## Initialize your project
In the root of your project, initialize with `npm init -f` to create a default `package.json` file if you don't already have one. Edit it, add the `build` script seen below to generate dummy output into a `dist` folder:

{% gist lthr/80f54aa8a7fe70e5d768fe80c93ebf3c package.json %}

## Deploy script
Create a file called `deploy-to-gh-pages.sh` containing this (replace `user.name` and `user.email` values):

{% gist lthr/80f54aa8a7fe70e5d768fe80c93ebf3c deploy-to-gh-pages.sh %}

## Travis setup script
Create a file called `.travis.yml` containing this:

{% gist lthr/80f54aa8a7fe70e5d768fe80c93ebf3c .travis.yml %}


## GitHub access token
Generate a new access token from [GitHub](https://github.com/settings/tokens/new). Give it a description, and the following permissions found [here](https://docs.travis-ci.com/user/github-oauth-scopes/). Don't close the window after you've created your token, you'll need the token later in this setup.

## Install Travis command line client
Install [Travis Command Line Client](https://github.com/travis-ci/travis.rb#readme) with `gem install travis`.

## Encrypt token
With the terminal, go into your project and execute the following (replace the text marked with **bold**):
<pre>
travis encrypt -r <b>YOUR-GITHUB-USERNAME</b>/<b>YOUR-GITHUB-REPOSITORY-NAME</b> GITHUB_TOKEN=<b>YOUR-GITHUB-TOKEN-HERE</b> --add
</pre>
This will add the encrypted token to your `.travis.yml` file.

## Travis-CI
Add your GitHub repository in your [Travis CI](https://travis-ci.org/profile) repository overview.

## GitHub repository settings
Go to your GitHub repository, under settings go to `Integration & Services`. Click the `Add service` dropdown and find `Travis CI`.

1. Under `User`, type your GitHub username.
2. Under `Token`, add your GitHub token.
3. Under Domain, type `notify.travis-ci.org`

## Add `dist/` folder
Create a folder in the root of your project called `dist`. Inside it, add a file called `index.html` containing some basic HTML. This is only for testing purpose, later you can add Gulp, Webpack or similar to generate your distribution content for this folder. Right now it's the `build` script from `package.js` that generates content in the `dist` folder.

## Create branch
In your GitHub repository, create a branch called `gh-pages`.

## Push your changes to GitHub
Now commit and push your changes to the `master` branch to GitHub. Travis-CI will detect this, and start deploying the content of the `dist` folder to GH-Pages. After deployment your page is available at:

<pre>http://<b>YOUR-GITHUB-USERNAME</b>.github.io/<b>YOUR-GITHUB-REPOSITORY-NAME</b></pre>
