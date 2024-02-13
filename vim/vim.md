# Vim
Vim is a highly configurable text editor built to make creating and changing any kind of text very efficient.

## Settings
- Create a `.vimrc` file in your home directory: `mkdir ~/.vimrc`
- and add following content to `.vimrc`:
```vim
"default vim
source $VIMRUNTIME/defaults.vim
    
"Enable line number
set number

"Enable syntax highlight
syntax on
filetype on
colorscheme default

"To scroll horizontally one character at a time to reveal more text as needed.
set sidescroll=1

"Enable autoindent
set autoindent
```
