This little command will show you what commits you did today. Good for when you need to register time on what you did at the end of the day.

```bash
cd /c/repos/your-git-folder ; git log --committer="your name" --since=yesterday | grep -v Date: | grep -v Author: | grep -v commit | grep -v "^$" | grep -v Merge: | sed -e "s/^[ \t]*/ /" | grep -n  . ; cd - > null
```

Output:
```bash
1: IU-9911: fix js class name
2: IU-9911: fix conflict
3: IU-9911: add animation
4: IU-9911: only show guaranteed jackpot if its larger than 0
5: IU-9911: fix conflict
6: IU-9549: show '0' instead of '--' for jackpots and number of players
7: IU-9549: remove text on mobile bingo images
8: IU-9549: align comment
9: IU-9549: fix missing div
10: IU-9549: don't stretch
11: IU-9878: fix whitespace
```
