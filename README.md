# Git-Mastering2
Bottlenecks : Files changed by many tasks
![alt text](https://github.com/aichimoaie/Git-Mastering2/blob/main/bottlenecks.jpg)
<br>
The --dirstat option shows which directories have changed in the commit and how much they have changed compared to each other. The default setting is to count the number of lines added to or removed from the commit. So, rearranging the code potentially does not count for any change as the line count might be the same. You can compensate for this slightly by using --dirstat=lines. This option will look at each file line by line and see whether they have changed compared to the previous version.
<br> Alternatively the --numstat options shows which files have changed
<br>
git log -1 --numstat
<br>
git log -1 --numstat=files
<br>
git log -1 --dirstat=lines,10,cumulative
<br>
between two releases
<br>
git log release1.0..release1.1 --format=format: --name-only | sed '/^$/d'  | sort | uniq -c | sort -r | head -10
<br>
git diff --pretty  release1.0..release1.1 --numstat  --relative
<br>
git diff --pretty  release1.0..release1.1 --numstat  --relative="org.tutorial.module/test/"  org.eclipse.module/test/
<br>
https://stackoverflow.com/questions/6349139/can-i-get-git-to-tell-me-all-the-files-one-user-has-modified
<br>

https://stackoverflow.com/questions/1580596/how-do-i-make-git-ignore-file-mode-chmod-changes
<br>
git config core.fileMode false
<br>
git log --format=%aD ./shell/design_updates.csv | tail -1
