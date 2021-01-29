# Git-Mastering2
Bottlenecks : Files changed by many tasks
![alt text](https://github.com/aichimoaie/Git-Mastering2/blob/main/bottlenecks.jpg)
<br>
git log -1 --numstat
<br>
git log -1 --numstat=files
<br>
git log -1 --disrtat=lines,10,cumulative
<br>
git log release1.0..release1.1 --format=format: --name-only | sed '/^$/d'  | sort | uniq -c | sort -r | head -10
<br>
git diff --pretty  release1.0..release1.1 --numstat  --relative
<br>
git diff --pretty  release1.0..release1.1 --numstat  --relative="org.tutorial.module/test/"  org.eclipse.module/test/
