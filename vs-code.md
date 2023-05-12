## Extensions
Edit csv
ESLint
GitLens
LiveShare
Text Marker (Highlighter)
Word Count (md word count) by rido3

## Code snippets
in `console.code-snippets` or maybe `User/snippets/javascript.json` -  I think there already should be an empty object and you put this inside (hence the seemingly missing outermost brackets).

```
".source.js": {
		"Console log Block": {
			"prefix": "clb",
			"body": "console.log('================')\nconsole.log(\"$1\", $1);\nconsole.log('================')"
		},
		"Console log": {
			"prefix": "cl",
			"body": "console.log(\"$1\");"
		},
		"Console log dupe": {
			"prefix": "cll",
			"body": "console.log(\"$1\", $1);"
		},
		"Describe Block": {
			"prefix": "desc",
			"body": "describe('$1', () => {\n\t$2\n});"
		},
		"beforeEach": {
			"prefix": "befo",
			"body": "beforeEach(() => {\n\t$1\n});"
		},
		"afterEach": {
			"prefix": "afte",
			"body": "afterEach(() => {\n\t$1\n});"
		},
		"it": {
			"prefix": "it",
			"body": "it('$1', () => {\n\t$2\n});"
		},
		"context": {
			"prefix": "cont",
			"body": "context('$1', () => {\n\t$2\n});"
		}
	}
```

## settings.json

Double check the bracket-pair-colorizer as it's now default in VSCode - see Joel's confluence post.

```
{
	"editor.wordWrap": "on",
	"eslint.format.enable": true,
	"editor.renderWhitespace": "all",
	"editor.insertSpaces": false,
	"editor.codeActionsOnSave": {
		"source.fixAll": true,
	},
	"javascript.validate.enable": false,
	"javascript.updateImportsOnFileMove.enabled": "always",
	"editor.acceptSuggestionOnCommitCharacter": false,
	"files.insertFinalNewline": true,
	"files.trimFinalNewlines": true,
	"diffEditor.ignoreTrimWhitespace": false,
	"workbench.statusBar.visible": true,
	"[javascript]": {
		"editor.defaultFormatter": "dbaeumer.vscode-eslint"
	},
	"bracket-pair-colorizer-2.depreciation-notice": false,
	"[javascriptreact]": {
		"editor.defaultFormatter": "dbaeumer.vscode-eslint"
	},
}
```
