## My Vim for Ruby on Rails development
![](http://f.cl.ly/items/1i2S0x1S060D3m2d2A3M/Screenshot_6_19_13_7_25_PM.png)

## Warning ##
I've stopped using MacVim(mostly) and started using console Vim in Tmux.
The lastest MacVim config extracted to the
[**macvim**](https://github.com/vrybas/dotvim/tree/macvim) branch and no
longer supported. But still contains most of the features described here.

## Features ##
   * **Ruby on Rails projects support** → [VimRails](http://github.com/tpope/vim-rails)
   * **Project Tree View** → [NERDTree](http://github.com/scrooloose/nerdtree)
   * **Project search with Ack** → [Ack.vim](http://github.com/mileszs/ack.vim)
   * **Files switcher** → [BufExplorer](http://github.com/vim-scripts/bufexplorer.zip)
   * **Popup Open File dialog with smart search** → [CtrlP](https://github.com/kien/ctrlp.vim)
   * **Code completion as-you-type (starts on 3rd symbol)** → [NeoComplCache](http://github.com/Shougo/neocomplcache.vim)
   * **Alternative code completion on Tab** → [SuperTab](http://github.com/ervandew/supertab)
   * **Graphical tree-like undo/redo tool** → [Gundo](http://github.com/sjl/gundo.vim)
   * **Incredible GIT support** → [Fugitive](http://github.com/tpope/vim-fugitive)
   * **Indication of added/modified/removed lines** → [Vim-GitGutter](https://github.com/airblade/vim-gitgutter)
   * **Create/manage gists on Github** → [Gist](http://github.com/mattn/gist-vim)
   * **Jump to class/method definition** → [Ctags](http://ctags.sourceforge.net)
   * **Run Rspec for current file/line/all of them** → [Rspec.vim](https://github.com/skwp/vim-rspec)
   * **Open online Ruby/Rails/Rspec documentation** from [APIDock](http://apidock.com)
   * **Open ri documentation** → [Ri.vim](https://github.com/danchoi/ri.vim)
   * **Syntax checking** → [Checksyntax.vim](https://github.com/tomtom/checksyntax_vim)
   * **Bundler support** → [vim-bundler] (https://github.com/tpope/vim-bundler)
   * **Rake support** → [vim-rake] (https://github.com/tpope/vim-rake)
   * **Rbenv support** → [vim-rbenv] (https://github.com/tpope/vim-rbenv)
   * **Tmux splits integration** → [vim-tmux-navigator] (https://github.com/christoomey/vim-tmux-navigator) | [help] (http://robots.thoughtbot.com/post/53022241323/seamlessly-navigate-vim-and-tmux-splits)

=====
   * **Maximize/unmaximize active split** → [ZoomWin](http://github.com/vim-scripts/ZoomWin)
   * **Bulk lines commenting based on syntax** → [NERDCommenter](http://github.com/scrooloose/nerdcommenter)
   * **Auto-closing quotes, brackets etc.** → [DelimitMate](http://github.com/vim-scripts/delimitMate.vim)
   * **Jump between quotes, brackets etc.** → [Matchit](http://github.com/tsaleh/vim-matchit)
   * **Jump around code with keystrokes** → [Easymotion](http://github.com/Lokaltog/vim-easymotion)
   * **Surround selected text with any symbols and replace surroundings on-the-fly** → [Surround](http://github.com/tpope/vim-surround)
   * **Smart text selection** → [Smartpairs](https://github.com/gorkunov/smartpairs.vim)
   * **Open scratch buffer which is never saved** → [VimScratch](http://github.com/duff/vim-scratch)
   * **Solarized theme** → [Solarized](http://github.com/altercation/vim-colors-solarized)

=====
   * **Hide everything, except selected text** (stay focused!)
   * **Toggle straight/relative line numbers to use with movement operations**
   * **Move code blocks left/right/up/down**
   * **Open current split in new tab**
   * **Open tabs by numbers**
   * **Restore cursor position on file open**
   * **Remove spaces from the end of each line on save**
   * **Cyrillic keys mapped to latin to use in command mode**
   * **Friendly text/markdown files editing with wrapping and ULTIMATE paragraph formatter**
   * **Spell checking english and russian(with ё) texts**

## Installation ##
   1. git clone git://github.com/vrybas/dotvim.git ~/.vim
   2. echo "runtime! rc.vim" > ~/.vimrc
   3. git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
   4. vim +BundleInstall +qall
   5. brew install ack
   6. brew install ctags
   7. gem install gem-ctags
   8. gem ctags (see [troubleshooting](https://github.com/tpope/gem-ctags#troubleshooting))
   9. mvim /path/to/project
   10. :e any_file_in_path
   11. :Rtags

## Keymap (above Vim & plugins standard) ##

* `space` -  Save file
* `Ctrl-D` - Open project Tree View
* `Ctrl-P` - Open File dialog

### Tabs
* `,,t` - Open current buffer in new tab
* `,1..9` - Go to 1..9 tab
* `,g` - Open class/function definition in new tab

### Buffers
* `,,b` - Buffer explorer
* `,x` - Close current buffer
* `,Tab` - Open scratch buffer which is never saved

### Splits
* `,v` - Create vertical split
* `,s` - Create horisontal split
* `,o` - Maximize/unmaximize split
* `,x` - Close split
* `,+` - Increase split area
* `,_` - Decrease split area
* `Ctrl-h` - Switch to Left
* `Ctrl-j` - Switch to Down
* `Ctrl-k` - Switch to Up
* `Ctrl-l` - Switch to Right

### Move selected line(s) around (in visually select mode)
* `,fh` - Move left
* `,fj` - Move down
* `,fk` - Move up
* `,fl` - Move right

### Other

* `,m`  - Clear search highlighting
* `,y`  - Toggle display trailing characters
* `,a`  - Search on current path with Ack
* `,l`  - Toggle relative/straight line numbers
* `F6`  - Do not autoindent lines, when paste from OS buffer (when pasting big code block)
* `,u`  - Toggle open graphical tree-based undo
* `,bd` - Switch to the dark colorscheme
* `,bl` - Switch to the light colorscheme

===
* `,d` - Fold selected lines
* `,za` - Fold everything, except selected lines
* `,zs` - Unfold everything

===
* `gh` - Jump to next git change
* `gH` - Jump to previous git change

===
* `,r`   - Run Rspec for current line
* `,,r`  - Run Rspec for current file
* `,,rr` - Run all Rspecs

===
* `,di` - Show all Ruby methods in current file (enter line number to jump)
* `,,i` - Check syntax
* `RR` - APIDock open Rails documentation for method under cursor
* `RB` - APIDock open Ruby documentation
* `RS` - APIDock open Rspec documentation

===
* `RI` - Open Ri documentation with autocompletive search in horisontal split
* `RIV` - Open Ri documentation in vertical split
* `RK` - Open Ri documentation for keyword under cursor

===
When editing Markdown or Text files:
* `,w4..8` - Set vertical ruler and autowrapping to 40..80 symbols
* `,wm`  - Set vertical ruler and autowrapping to 78 symbols (Email standard)
* `,wg`  - Set vertical ruler and autowrapping to 72 symbols for writing
commit messages (@tpope's
[post](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
on that)
* `,c` - Cut text above to the clipboard without line breaks
* `,q` - Insert journal-like current date as next line

