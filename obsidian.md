Display tasks and sort by folder.


    ```dataview
    task
    where !completed
    group by (split(file.folder, "/")[0] + "/" + split(file.folder, "/")[1])
    ``` 

# CSS Snippets

`yesterday-review.css`
```
.markdown-embed-content h2 {
  display: none;
  /* color: red; */
}

.markdown-embed-content p, .markdown-embed-content ul {
    font-size: small;
    opacity: 0.5;
}
```

`dataview.css`
```
/* I may want to change in the future is to specifically redesign the text
in-line fields as they don't look amazing... but also I'm not sure I'll use them
anyway. */

/* ===[ Task field properties ]=======================================================*/

li > .dataview.task-list-item > span {
    display: contents;
}

.dataview.inline-field { 
    font-size: x-small;
    margin: 0;
    width: 180px;
    display: grid;
    grid-template-columns: auto auto;
}

li .dataview.inline-field-value {
    width: 200px;
    color: var(--text-muted);
    background-color: var(--background-primary);  
    margin: 0;
}

li .dataview.inline-field-key {
    width: 80px;
    /* color: var(--text-faint); */
    border-right: 1px solid var(--text-faint);
    background-color: var(--background-primary);
    margin: 0;
}

a.tag:empty {
  display: none !important;
}

/* ===[ Dataview group by file.name headers ]=========================================*/

.dataview.dataview-container > h4 {
    font-size: medium;
    color: var(--bold-color);
}
```
