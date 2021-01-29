# Git-Mastering2
Bottlenecks : Files changed by many tasks
![alt text](https://github.com/aichimoaie/Git-Mastering2/blob/main/bottlenecks.jpg)

git log -1 --numstat
git log -1 --numstat=files
git log -1 --disrtat=lines,10,cumulative
git log release1.0..release1.1 --format=format: --name-only | sed '/^$/d'  | sort | uniq -c | sort -r | head -10


git diff --pretty  release1.0..release1.1 --numstat  --relative
git diff --pretty  release1.0..release1.1 --numstat  --relative="org.tutorial.module/test/"  org.eclipse.module/test/
