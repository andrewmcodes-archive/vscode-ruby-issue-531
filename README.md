# vscode-ruby issue #531

## Reproduction

`config/environments/development.rb`

### Example of rubocop lint in file

![rubocop_lint](screenshots/rubocop_lint.png)

### Example of standardrb lint in file

![standard_lint](screenshots/standard_lint.png)

## Settings

### Global

```json
// PLUGIN: Ruby
// Use built-in language server
"ruby.useLanguageServer": true,
// Time (ms) to wait after keypress before running enabled linters.
"ruby.lintDebounceTime": 1500,
// Method to use for intellisense (go to definition, etc.). Use `false` to disable or if another extension provides this feature.
// "ruby.intellisense": false,
//run non-lint commands with bundle exec
"ruby.useBundler": false,
"ruby.lint": {
  // enable rubocop via bundler
  "rubocop": {
    "useBundler": false
  }
},
// use rubocop for formatting
"ruby.format": "rubocop",
```

### Workspace

```json
{
  "ruby.useBundler": true,
  "ruby.useLanguageServer": true,
  "ruby.lint": {
    "rubocop": false,
    "standard": true
  },
  "ruby.format": "standard",
}
```
