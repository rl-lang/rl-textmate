# rl-textmate

Canonical TextMate grammar for [rl-lang](https://github.com/rl-lang/rl-lang):
`syntaxes/rl.tmLanguage.json` (`scopeName: source.rl`, file type `.rl`).

## Who uses it

| Consumer | How |
|----------|-----|
| [vscode-rl-lang](https://github.com/rl-lang/vscode-rl-lang) | git submodule at `syntaxes/` |
| JetBrains IDEs | import the grammar as a TextMate bundle |
| GitHub Linguist | mirrored into [tree-sitter-rl](https://github.com/rl-lang/tree-sitter-rl) `syntaxes/` for language detection |
| Any TextMate-compatible editor | drop `syntaxes/rl.tmLanguage.json` into the grammars folder |

## For maintainers

This copy is canonical. The mirrors (VSCode submodule, tree-sitter-rl
`syntaxes/`) must match it exactly:

```bash
diff syntaxes/rl.tmLanguage.json ../vscode-rl-lang/syntaxes/rl.tmLanguage.json
diff syntaxes/rl.tmLanguage.json ../tree-sitter-rl/syntaxes/rl.tmLanguage.json
```

When the language gains syntax, update this file first, then sync the
mirrors and note it in the commit message.

## License

MIT or Apache 2.0 at your option.
