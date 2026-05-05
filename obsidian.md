Display tasks and sort by folder.

```dataview
task
where !completed
group by (split(file.folder, "/")[0] + "/" + split(file.folder, "/")[1])
```
