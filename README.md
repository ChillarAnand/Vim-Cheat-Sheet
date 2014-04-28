## Modes and Basic movement
    vim -  shows info about vim
    default mode is command mode
    j/k/h/l - navigation
    i - insert mode
    esc - go back to command mode

## Faster Movement 
    w - jump from word to word
    W - move whole word
    b - go back to word
    B - back to whole word
    A - append at the end of line 
    $ - go to end of line
    ^ - go to first non space char of line
    0 - go to very beginning of line
    gg - begining of file
    G - go to end of file
    } - jump to next paragraph
    { - back to paragraph
    f* - will find the first occurance of * in the line
    F* - find backwords the * char
    t* - till the occurence of *
    T* - backward occurence of *
    8gg - 8th line
    8G - 8th line
    :8 - go to 8th line
    ; - repeat the last search
    , - repeat last search on opposite direction


## Basic Editing
    :e ~/.vimrc
    x - delete current character
    u - undo the previous change
    dw - delete the word
    db - delete the previous word
    5dw - delete 5 words
    cw - change the word
    dd - delete the current line
    cc - change the whole line
    dt" - delete inside quotes
    ct" - change the string inside the ""
    ci" - change inside "/{/[/' and so on
    ca" - change around "


## Cut, Copy and Paste
    dw - delete the word
    p - paste from buffer
    P - paste from buffer starting from one column behind
    dj - delete current and immediate follwing line
    yw - copy the current word
    yy - copy the current line
    y0 - copy everything before the cursor to beginning of the line
    dh - delete  previous character  
    dl - delete current char
    dj - delete current line and next line
    dk - delete current line and above line
    x - delete char under the cursor


Lesson 06: SEARCHING IN VIM  -----------------------------------------------------------------------------------------------------------------
/ - search for something - case sensitive
n - take to next search result
N - back to previous search result
? - search the doc backwards
:set incsearch - set incremental search
:set ignorecase - case insensitive search
:set hlsearch - highlight search
:nohlsearch - disable highligh search
:noh - a shortcut for :nohlsearch
d/chalam - delete all the text from the postion of cursor to chalam.
    it works the same with change and yank.
/.[gain] - finds *gain
/\n\n - finds all empty lines in the file

Lesson 07: Replace
:s/find/replace - substitute a word for another
:%s/find/replace - repeat the above for entire file
:%/find/replace/g - substitute globally ( all occurances in the file )
v - visual mode
shit + v - visual line mode
shift + % - finding matched brace
:%/find/replace/gc - substitute after conformation
gv - select previous visually
:s/find/replace/gci - case insensitive replacement
/[^ ](
/[^ ]\zs(
/),
/)\ze,

Lesson 08: Macros and registers
:registers
qa - to record a macro
@a -execute a macro
ctrl + g - inforamtion about current file

Lesson 09: Advanced Movements
ctrl + d - move half wat down in the current screen
crtl + u - move half up in current screenct
ctrl + f - full screen down
crtl + b - full screen up
M - go to middle
L - last line of window
H - go to top
3L - 3rd line from the last
3H - 3rd from the top
zt - current line stays on the top of page
zb - bottom
zz - middle of the window
Markers
m followed by register to mark
' followed by register to go to mark
'' - go to visited places

Lesson 10: Invoking the command line directly from vim
:! - can use commands
:read !command - brings command result into the file
:r  !curl --silent url - brings url to file
:se ft=javascript

Lesson 11: Buffers
:bn - navigate to the next buffer
:bp - previous buffer in the list
:b# - navigate to previous buffer
:bf - first buffer
O - inset new line before
@@ - recent macro again
:bd - delete current buffer
:bd12 - delete 12 buffer

Lesson 12: Windows and tabs
:e url - edit a file
:vsplit url - vertical split the screen
ctrl + w + hjkl - switch between files in a screen
ctrl + w + +/- to resize the window
ctrl + w + e - resize all windows equally
:sb2 - new split window in top
:vert sb3 - 
:tabedit url -
:tabe url - open a new tab
gt - go to next tab
gT - go to previous tab
 :gf - go to first tab

Lesson 13: Graphical vim


Lesson 14: Indents and folds
>> - indentation of tab
:set list - 
:set expandtab
:set noexpandtab
:set shiftwidth = 4
<< - undo indent
2>> - indent 2 lines
:set nolist
'o' - other side of visual selection
gv - reselect the previous select
o - go to new after the cursor
:set smartindent
= - auto indentation
=3j - auto indent 3 lines next to current postion
:set softtabstop = 4
ctrl + t - indent in insert mod3e
ctrl + d - undo indent
zf5j - fold the next five lines
zo - open fold
zc - close
zd - delete
zi - invert foldings
:set foldmenthod = s:yntax
:se fdm = syntax
zC - close fold from current to top
zO - to every single folding inside
:se fmd = marker 
:set foldmarker = {{{,}}}

Lesson 15: Vimrc file
set nocompatible
filetype on
filetype indent on
filetype plugin on
set backspace=indent,eol,start
set smartcase
set gdefault
set incsearch
set showmatch
set list
:so %
set noswapfile
set visualbell
set cursorline






OTHERS:
:newtab - open a new tab






