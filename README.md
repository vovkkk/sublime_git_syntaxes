# Git Syntaxes
Syntax Highlighting for SublimeText

![](https://camo.githubusercontent.com/6bc71ab0aaf080e3e40faba31aac56bceb0b0d4a/68747470733a2f2f636c6f75642e67697468756275736572636f6e74656e742e636f6d2f6173736574732f313937353239382f383530383536392f34666135333433362d323239372d313165352d393638312d6435393663363539303265642e706e67)

## Features
* Highlight all Git files (gitconfig, gitattributes, commit message, interactive rebase todo)
* Toggle comments in all files above with default keystroke whatever it is (usually <kbd>ctrl</kbd> + <kbd>/</kbd>)
* Many scopes, e.g. you can set separate colour for every command in rebase file (i.e. `pick`, `fixup`, etc.)

## Customisation
Sublime Text supports per-syntax settings, for instance, you may want to enable spell check whenever write commit message, or make a font size bigger, or maybe even use completely different colour scheme — all these possible.

Create files:

1. For commits `Packages/User/commit-message.sublime-settings`
2. For rebase `Packages/User/rebase.sublime-settings`

Content of those files:
```json
{
    "spell_check": true,
    "font_size": 22
}
```

For available settings look at `Preferences` → `Settings — Default` (note, some settings are global and cannot be syntax-specific, e.g. `"font_options"`).

## How to use ST as editor for Git
**Note** for Windows, you must have `Build 3065` or later to have command line support, or just add the folder into `PATH` and call `sublime_text` instead of `subl`

- Mac / Linux: `subl -n -w`
- Windows: `subl.exe -n -w`

### Preferred method: edit `.bashrc`
This will allow for more editing options than just the git commit, like editing diffs. This also leaves flexibility as it can be easily overridden, by the `.gitconfig` for example.
Add the following to your `.bashrc`:
On Mac and Linux:

```
export EDITOR="subl -n -w"
```

### Alternate method: amend your `.gitconfig`
You can run the following command to let git update your `.gitconfig`

```
git config --global core.editor 'subl -n -w'
```

Or add the following line manually to your `.gitconfig`
```
[core]
    editor = 'subl -n -w'
```

You also can hide menu (as on screenshot above) and tabs:

    editor = "sublime_text -n -w --command toggle_menu --command toggle_tabs"


## SFAQ
### Aren’t there similar packages for those syntaxes? Why another one? Why not contribute into existing one?
I’ve [tried](https://github.com/adambullmer/sublime_git_commit_syntax/pull/1) with no luck, or any feedback.
So this package is an attempt (the first one, in fact) to bring all related syntaxes in one place.

### But what about Git, GitSavvy and many others?
Those packages add integration in an IDE fashion — so you call git from-within Sublime Text.  
This package does an opposite thing — make stuff more readable whenever you call ST from-within git, so ST remains an editor with extra features rather than IDE.

### Are you interested in pull requests or collaboration in general?
Sure, absolutely.

### What is ‘s’ in SFAQ for?
<b>S</b>upposedly frequently asked questions.

### Do you even push-up?
Nope.

## Credits
* Commit definitions are provided by [Josh Goebel](https://github.com/yyyc514)
* Base for Config definitions is borrowed from <https://github.com/textmate/git.tmbundle>

<hr>

All sources under [MIT](LICENSE)
