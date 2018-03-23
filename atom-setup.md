# Setting Up a Development Environment with Atom

Download at [atom.io](http://atom.io) for Windows or Mac.

All packages and themes are optional. I list them here as a matter of personal preference and for use based on the kind of work to be done. You have the freedom to choose whatever packages you wish.

## Packages

To install: Settings > Install > [Packages] > Search for packages<br>
To manage: Packages > Installed Packages > Community Packages

**General**

* [file-icons](https://atom.io/packages/file-icons)
* [highlight-line](https://atom.io/packages/highlight-line)
* [pigments](https://atom.io/packages/pigments)
* [tool-bar](https://atom.io/packages/tool-bar)
* [tool-bar-atom](https://atom.io/packages/tool-bar-atom)
* [atom-ide-ui](https://atom.io/packages/atom-ide-ui) _(contains Hyperclick)_
* [document-outline](https://atom.io/packages/document-outline) _Useful for navigating large markdown documents_
* [platformio-ide-terminal](https://atom.io/packages/platformio-ide-terminal) _Working fork of terminal-plus_
* [autoclose-html](https://atom.io/packages/autoclose-html)
* [autoupdate-packages](https://atom.io/packages/auto-update-packages)
* [autocomplete-modules](https://atom.io/packages/autocomplete-modules) _Useful for quickly including node_modules_
* [sync-settings](https://atom.io/packages/sync-settings)
* [todo-show](https://atom.io/packages/todo-show)
* [color-picker](https://atom.io/packages/color-picker)
* [markdown-preview-enhanced](https://shd101wyy.github.io/markdown-preview-enhanced/#/) - Replacement for default `markdown-preview`

**JS Development**

* [atom-ternjs](https://atom.io/packages/atom-ternjs) _(optional: used for js/nodejs/jquery + more development)_
* [docblockr](https://atom.io/packages/docblockr) _Makes writing documentation easy_

## Themes

To install: Settings > Install > [Themes] > Search for themes<br>

* [chester-atom-syntax](https://atom.io/themes/chester-atom-syntax)
* [dash-ui](https://atom.io/themes/dash-ui) - UI Theme
* [dash-syntax](https://atom.io/themes/dash-syntax) - Syntax Theme

Theme of choice: One Dark (UI Theme and Syntax Theme)

You can also install packages (and themes) using Atom's package manager command line utility "apm" in the Terminal. All packages are installed in ~/.atom/packages.

``apm install file-icons``

## Other Tweaks

Hide Specific Files

TO hide files or folders such as .git and .DS_Store, Check the box Packages > tree-view > Settings > Hide Ignored Names. This will enable the setting and use the list of "Ignored Names" shown under Settings > Core > Ignored Names. By default, this list consists of .git, .hg, .svn, .DS_Store, ._*, Thumbs.db, desktop.ini.









