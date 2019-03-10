# VS code

## Basic Editing Shortcuts

| Key                 | Command                                     | Command id                                        |
|---------------------|---------------------------------------------|---------------------------------------------------|
| Ctrl+X              | Cut line (empty selection)                  | editor.action.clipboardCutAction                  |
| Ctrl+C              | Copy line (empty selection)                 | editor.action.clipboardCopyAction                 |
| Ctrl+Shift+K        | Delete Line                                 | editor.action.deleteLines                         |
| Ctrl+Enter          | Insert Line Below                           | editor.action.insertLineAfter                     |
| Ctrl+Shift+Enter    | Insert Line Above                           | editor.action.insertLineBefore                    |
| Alt+Down            | Move Line Down                              | editor.action.moveLinesDownAction                 |
| Alt+Up              | Move Line Up                                | editor.action.moveLinesUpAction                   |
| Ctrl+Shift+Alt+Down | Copy Line Down                              | editor.action.copyLinesDownAction                 |
| Ctrl+Shift+Alt+Up   | Copy Line Up                                | editor.action.copyLinesUpAction                   |
| Ctrl+D              | Add Selection To Next Find Match            | editor.action.addSelectionToNextFindMatch         |
| Ctrl+K Ctrl+D       | Move Last Selection To Next Find Match      | editor.action.moveSelectionToNextFindMatch        |
| Ctrl+U              | Undo last cursor operation                  | cursorUndo                                        |
| Shift+Alt+I         | Insert cursor at end of each line selected  | editor.action.insertCursorAtEndOfEachLineSelected |
| Ctrl+Shift+L        | Select all occurrences of current selection | editor.action.selectHighlights                    |
| Ctrl+F2             | Select all occurrences of current word      | editor.action.changeAll                           |
| Ctrl+L              | Select current line                         | expandLineSelection                               |
| Shift+Alt+Down      | Insert Cursor Below                         | editor.action.insertCursorBelow                   |
| Shift+Alt+Up        | Insert Cursor Above                         | editor.action.insertCursorAbove                   |
| Ctrl+Shift+\        | Jump to matching bracket                    | editor.action.jumpToBracket                       |
| Ctrl+]              | Indent Line                                 | editor.action.indentLines                         |
| Ctrl+[              | Outdent Line                                | editor.action.outdentLines                        |
| Home                | Go to Beginning of Line                     | cursorHome                                        |
| End                 | Go to End of Line                           | cursorEnd                                         |
| Ctrl+End            | Go to End of File                           | cursorBottom                                      |
| Ctrl+Home           | Go to Beginning of File                     | cursorTop                                         |
| Ctrl+Down           | Scroll Line Down                            | scrollLineDown                                    |
| Ctrl+Up             | Scroll Line Up                              | scrollLineUp                                      |
| Alt+PageDown        | Scroll Page Down                            | scrollPageDown                                    |
| Alt+PageUp          | Scroll Page Up                              | scrollPageUp                                      |
| Ctrl+Shift+[        | Fold (collapse) region                      | editor.fold                                       |
| Ctrl+Shift+]        | Unfold (uncollapse) region                  | editor.unfold                                     |
| Ctrl+K Ctrl+[       | Fold (collapse) all subregions              | editor.foldRecursively                            |
| Ctrl+K Ctrl+]       | Unfold (uncollapse) all subregions          | editor.unfoldRecursively                          |
| Ctrl+K Ctrl+0       | Fold (collapse) all regions                 | editor.foldAll                                    |
| Ctrl+K Ctrl+J       | Unfold (uncollapse) all regions             | editor.unfoldAll                                  |
| Ctrl+K Ctrl+C       | Add Line Comment                            | editor.action.addCommentLine                      |
| Ctrl+K Ctrl+U       | Remove Line Comment                         | editor.action.removeCommentLine                   |
| Ctrl+/              | Toggle Line Comment                         | editor.action.commentLine                         |
| Ctrl+Shift+A        | Toggle Block Comment                        | editor.action.blockComment                        |
| Ctrl+F              | Find                                        | actions.find                                      |
| Ctrl+H              | Replace                                     | editor.action.startFindReplaceAction              |
| F3                  | Find Next                                   | editor.action.nextMatchFindAction                 |
| Shift+F3            | Find Previous                               | editor.action.previousMatchFindAction             |
| Alt+Enter           | Select All Occurrences of Find Match        | editor.action.selectAllMatches                    |
| Alt+C               | Toggle Find Case Sensitive                  | toggleFindCaseSensitive                           |
| Alt+R               | Toggle Find Regex                           | toggleFindRegex                                   |
| Alt+W               | Toggle Find Whole Word                      | toggleFindWholeWord                               |
| Ctrl+M              | Toggle Use of Tab Key for Setting Focus     | editor.action.toggleTabFocusMode                  |
| unassigned          | Toggle Render Whitespace                    | toggleRenderWhitespace                            |
| Alt+Z               | Toggle Word Wrap                            | editor.action.toggleWordWrap                      |

## Shortcuts

| Shortcut                                    | Defintion                                      |
|---------------------------------------------|------------------------------------------------|
| Ctrl+K Ctrl+S                               | Customize keyboard shortcuts                   |
| Ctrl+K Ctrl+T                               | Change your theme                              |
| Ctrl+K Ctrl+F                               | Code formatting selection                      |
| Ctrl+K Ctrl+I                               | Code formatting selection                      |
| Ctrl+Shift+[, Ctrl+Shift+]                  | Code folding                                   |
| Ctrl+Space                                  | Intellisense                                   |
| Ctrl+Shift+F10                              | Peek                                           |
| F12                                         | Go to definition                               |
| Shift+F12                                   | Peak definition                                |
| Shift+Alt+F12                               | find all references                            |
| F2                                          | rename symbol                                  |
| Alt+R                                       | search and modify                              |
| File -> Autosave                            | Toggle autosave "files.autosave": "afterDelay" |
| Ctrl+Shift+X                                | extensions shortcut                            |
| Ctrl+Shift+V                                | open markdown preview                          |
| Ctrl+K V                                    | Side by side markdown with live preview        |
| Ctrl+``                                     | integrated terminal                            |
| Ctrl+,                                      | update user settings                           |
| Ctrl+B                                      | toggle sidebar                                 |
| Ctrl+K z                                    | zen mode                                       |
| Esc Esc                                     | exit zen mode                                  |
| Ctrl+\                                      | side by side editing                           |
| Ctrl+1, Ctrl+2                              | switch between editors                         |
| Ctrl+Shift+E                                | move explorer window                           |
| Ctrl+Click                                  | open or create a file on link                  |
| Ctrl+W                                      | close currently open folder                    |
| Ctrl+Alt+-                                  | back navigate                                  |
| Ctrl+Shift+-                                | Navigate forward                               |
| Ctrl+G                                      | Go to specific line                            |
| Ctrl+Shift+G                                | Git integration                                |
| F7 and Shift+F7                             | git diffs in unified pane                      |
| Ctrl+Shift+P                                | configure debugger                             |
| Ctrl+Shift+P > Open Keyboard Shortcuts File | bind desired shortcut to file                  |
| Ctrl+Shift+M                                | Status bar errors and warnings                 |
| F8                                          | Cycle through errors and warnings              |

## Rich Languages Editing Shortcuts

| Key              | Command                     | Command id                                 |
|------------------|-----------------------------|--------------------------------------------|
| Ctrl+Space       | Trigger Suggest             | editor.action.triggerSuggest               |
| Ctrl+Shift+Space | Trigger Parameter Hints     | editor.action.triggerParameterHints        |
| Ctrl+Shift+I     | Format Document             | editor.action.formatDocument               |
| Ctrl+K Ctrl+F    | Format Selection            | editor.action.formatSelection              |
| F12              | Go to Definition            | editor.action.revealDefinition             |
| Ctrl+K Ctrl+I    | Show Hover                  | editor.action.showHover                    |
| Ctrl+Shift+F10   | Peek Definition             | editor.action.peekDefinition               |
| Ctrl+K F12       | Open Definition to the Side | editor.action.revealDefinitionAside        |
| Ctrl+.           | Quick Fix                   | editor.action.quickFix                     |
| Shift+F12        | Peek References             | editor.action.referenceSearch.trigger      |
| F2               | Rename Symbol               | editor.action.rename                       |
| Ctrl+Shift+<     | Replace with Next Value     | editor.action.inPlaceReplace.down          |
| Ctrl+<           | Replace with Previous Value | editor.action.inPlaceReplace.up            |
| Shift+Alt+Right  | Expand AST Selection        | editor.action.smartSelect.expand           |
| Shift+Alt+Left   | Shrink AST Selection        | editor.action.smartSelect.shrink           |
| Ctrl+K Ctrl+X    | Trim Trailing Whitespace    | editor.action.trimTrailingWhitespace       |
| Ctrl+K M         | Change Language Mode        | workbench.action.editor.changeLanguageMode |

## Navigation Shortcuts

| Key            | Command                         | Command id                                             |
|----------------|---------------------------------|--------------------------------------------------------|
| Ctrl+T         | Show All Symbols                | workbench.action.showAllSymbols                        |
| Ctrl+G         | Go to Line...                   | workbench.action.gotoLine                              |
| Ctrl+P         | Go to File..., Quick Open       | workbench.action.quickOpen                             |
| Ctrl+Shift+O   | Go to Symbol...                 | workbench.action.gotoSymbol                            |
| Ctrl+Shift+M   | Show Problems                   | workbench.actions.view.problems                        |
| F8             | Go to Next Error or Warning     | editor.action.marker.nextInFiles                       |
| Shift+F8       | Go to Previous Error or Warning | editor.action.marker.prevInFiles                       |
| Ctrl+Shift+P   | Show All Commands               | workbench.action.showCommands                          |
| Ctrl+Shift+Tab | Navigate Editor Group History   | workbench.action.openPreviousRecentlyUsedEditorInGroup |
| Ctrl+Alt+-     | Go Back                         | workbench.action.navigateBack                          |
| Ctrl+Alt+-     | Go back in Quick Input          | workbench.action.quickInputBack                        |
| Ctrl+Shift+-   | Go Forward                      | workbench.action.navigateForward                       |

## Preference Shortcuts

| Shortcut      | Command                                | Defintion                  |
|---------------|----------------------------------------|----------------------------|
| Ctrl+,        | workbench.action.openSettingsn         | open settings              |
| unassigned    | workbench.action.openWorkspaceSettings | open workspace settings    |
| Ctrl+K Ctrl+S | workbench.action.openGlobalKeybindings | Open keyboard shortcuts    |
| unassigned    | workbench.action.openSnippets          | open user snippets         |
| Ctrl+K Ctrl+T | workbench.action.selectTheme           | select color theme         |
| unassigned    | workbench.action.configureLocale       | Configure display language |

## Editor/Window Management Shortcuts

| Key                 | Command                              | Command id                                  |
|---------------------|--------------------------------------|---------------------------------------------|
| Ctrl+Shift+N        | New Window                           | workbench.action.newWindow                  |
| Ctrl+W              | Close Window                         | workbench.action.closeWindow                |
| Ctrl+W              | Close Editor                         | workbench.action.closeActiveEditor          |
| Ctrl+K F            | Close Folder                         | workbench.action.closeFolder                |
| unassigned          | Cycle Between Editor Groups          | workbench.action.navigateEditorGroups       |
| Ctrl+\              | Split Editor                         | workbench.action.splitEditor                |
| Ctrl+1              | Focus into First Editor Group        | workbench.action.focusFirstEditorGroup      |
| Ctrl+2              | Focus into Second Editor Group       | workbench.action.focusSecondEditorGroup     |
| Ctrl+3              | Focus into Third Editor Group        | workbench.action.focusThirdEditorGroup      |
| unassigned          | Focus into Editor Group on the Left  | workbench.action.focusPreviousGroup         |
| unassigned          | Focus into Editor Group on the Right | workbench.action.focusNextGroup             |
| Ctrl+Shift+PageUp   | Move Editor Left                     | workbench.action.moveEditorLeftInGroup      |
| Ctrl+Shift+PageDown | Move Editor Right                    | workbench.action.moveEditorRightInGroup     |
| Ctrl+K Left         | Move Active Editor Group Left        | workbench.action.moveActiveEditorGroupLeft  |
| Ctrl+K Right        | Move Active Editor Group Right       | workbench.action.moveActiveEditorGroupRight |
| Ctrl+Alt+Right      | Move Editor into Next Group          | workbench.action.moveEditorToNextGroup      |
| Ctrl+Alt+Left       | Move Editor into Previous Group      | workbench.action.moveEditorToPreviousGroup  |

## Options

| Option                                                     | Description                                 |
|------------------------------------------------------------|---------------------------------------------|
| "editor.tabSize": 4                                        | change the tab size                         |
| "editor.insertSpaces": true                                | spaces or tabs                              |
| "editor.renderWhiteSpace": "all"                           | render whitespace                           |
| "search.exclude": { "someFolder": true, "someFile": true } | ignore certain files                        |
| "[languageid]": { }                                        | language specific settings                  |
| "json.schemas" {}                                          | used to add json validation to many schemas |

## Menu

| Menu                              | Description                          |
|-----------------------------------|--------------------------------------|
| File > Preference > User Snippets | select language and create a snippet |
| Terminal > Run Task               | To run tasks in terminal menu        |

## Command Line

| Command Line                    | Description                                               |
|---------------------------------|-----------------------------------------------------------|
| code .                          | open current directory                                    |
| code -r .                       | open current directory in most currently used code window |
| code -n                         | open a new window                                         |
| code --locale=es                | change the language                                       |
| code --diff \<file1\> \<file2\> | open diff editor                                          |
| code --goto package.json:10:5   | Open file at specific line and column line[:character]    |