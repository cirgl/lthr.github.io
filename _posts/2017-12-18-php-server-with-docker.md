---
layout: post
title: Run a local PHP server with Docker
tags:
- php
- apache
- docker
---

### Step 1
Install [Docker](https://www.docker.com/).

### Step 2
From terminal, run the following (fix the `~/your-php-project/` path to point to your local PHP project folder):
```bash
docker run -tid -p 80:80 --name apache -v ~/your-php-project/:/var/www/html nimmis/apache-php5
```

### Step 3
Enjoy on `http://localhost/`.

### Additional
Stop the server with `docker stop apache`.  
