# Git Syntaxes
Syntax Highlighting for SublimeText

![](https://leto21h.storage.yandex.net/rdisk/ba2874260630e3a93d2f9e2f85d90842af2bc4de368e9fb5b7aabf95eda95c9f/inf/f9LX--q8AvzANsoPK90KCkq6HKdoWKAz5oCEO2sJcBokNtdo2f4iuKc3PsG1PsPeYFediDpOOiaC5nZiGRUlMA==?uid=0&filename=2015-06-18%2014-43-50%20C%20%20Users%20vova%20.gitconfig%20-%20Sublime%20Text%202.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&tknv=v2&rtoken=b3a47b6091b952b1ec8f1bb701abb096&force_default=no)

# Features
* Highlight all Git files (gitconfig, gitattributes, commit message, interactive rebase todo)
* Toggle comments in all files above with default keystroke whatever it is (usually <kbd>ctrl+/</kbd>)
* Many scopes, e.g. you can set separate colour for every command in rebase file (i.e. `pick`, `fixup`, etc.)

## How to use ST as editor for Git
**Note** for Windows, you must have `Build 3065` or lated to have command line support, Or just add folder into `PATH` and call `sublime_text` instead of `subl`

- Mac / Linux: `subl -n -w`
- Windows: `subl.exe -n -w`

### Preferred Method: Edit `.bashrc`
This will allow for more editing options than just the git commit, like editing diffs. This also leaves flexibility as it can be easily overridden, by the `.gitconfig` for example.
Add the following to your `.bashrc`:
On Mac and Linux:

```
export EDITOR="subl -n -w"
```

### Alternate Method: Ammend your `.gitconfig`
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


## Credits
* Base for Config definitions is borrowed from <https://github.com/textmate/git.tmbundle>
* Commit definitions are borrowed from <https://github.com/adambullmer/sublime_git_commit_syntax>

<hr>

All sources under [MIT](LICENSE)