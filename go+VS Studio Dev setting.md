# VS Studio + Go Development environment setting
## install extentions 
go
## install and update tool
F1>Go:install>Update Tools>select all>OK  to install all select. 

## Use the VSCode-Go plugin, with the following configuration:
F1>preferences:open Settings(JSON)


```
"go.useLanguageServer": true,
"[go]": {
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
        "source.organizeImports": true,
    },
    // Optional: Disable snippets, as they conflict with completion ranking.
    "editor.snippetSuggestions": "none",
},
"[go.mod]": {
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
        "source.organizeImports": true,
    },
},
"gopls": {
     // Add parameter placeholders when completing a function.
    "usePlaceholders": true,

    // If true, enable additional analyses with staticcheck.
    // Warning: This will significantly increase memory usage.
    "staticcheck": false,
}
```


reference setting  https://github.com/golang/tools/blob/master/gopls/doc/vscode.md
