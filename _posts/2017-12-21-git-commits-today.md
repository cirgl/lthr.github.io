---
layout: post
title: Git commits today
tags:
- git
- bash
---

This little command will show you what commits you did today. Good for when you need to register time on what you did at the end of the day.

```bash
git log --committer="your name" --since="yesterday" --oneline --no-merges
```

Output:
```bash
b7d676d220 use defineDs
ecb15be34c (tag: 2.1.239-IU-9549-bingo-a) IU-9549: fix broken path to bingo
24494691fa IU-9549: get values from new feed structure
6ca01e83a2 (feature/IU-9911-frontend-skal-styre-visning-af-jackpots) IU-9911: remove unused cs var
6aaff48a4b IU-9911: use better naming for js arguments
dcde1bb65d IU-9911: add better name for js css class
e830930bef IU-9911: better js class
7e6534cf1d IU-9911: only transform should be translated
```
