"File created on April 5, 2021
"Initial configuration
set nocp
set encoding=utf8
set ffs=unix,dos,mac
set wildmenu
set belloff=all
"Show location of cursor
set ruler
"Setting up numbering in editor
set number
set so=7
"moving from insert mode to normal mode using jh key"
set timeoutlen=300
"imap \c <Esc>^ 
set showcmd
"Match setting of brackets,
set showmatch
"How many tenth of second to blink for matching bracket
set mat=2
let mapleader = ","
let maplocalleader = "\\"
function Change_LineNumber()
	"echom "Toggle between showing line number, relative number and no number" 
	if &number == 1 && &relativenumber == 0
		set nonumber | set relativenumber
	elseif &number == 0 && &relativenumber == 1
		set norelativenumber | set nonumber
	else 
		set number | set norelativenumber
	endif 
	return 0
endfunction
"set foldcolumn=1
"nmap <C-L> :call Change_LineNumber()<CR> 
nmap <leader>l :call Change_LineNumber()<CR>
"Basic Operations saving, exit and exit and save 
nmap <leader>w :w!<CR>
nmap <leader>q :q!<CR>
"nmap <leader>e :wq<CR>
map <leader>v :set paste!<CR>
nmap <leader>b 0
nmap <leader>e $
"Search related configuration
set hlsearch
set ignorecase
set incsearch
nmap <space> /
nmap <C-space> ?
nmap <Leader><space> :noh<CR>
"Bindkey for local leader
imap <localleader>c <Esc>
"Auto closing brackets C+v escape completion
inoremap " ""<left>
inoremap ' ''<left>
inoremap ( ()<left>
inoremap [ []<left>
inoremap { {}<left>
inoremap < <><left>
inoremap {<CR> {<CR>}<ESC>O
inoremap {;<CR> {<CR>};<ESC>O
syntax enable

"Learning Vim in hard way
nmap <ScrollWheelUp> <nop>
" Remove newbie crutches in Command Mode
" cnoremap <Down> <Nop>
" cnoremap <Left> <Nop>
" cnoremap <Right> <Nop>
" cnoremap <Up> <Nop>

" Remove newbie crutches in Insert Mode
inoremap <Down> <Nop>
inoremap <Left> <Nop>
inoremap <Right> <Nop>
inoremap <Up> <Nop>

" Remove newbie crutches in Normal Mode
nnoremap <Down> <Nop>
nnoremap <Left> <Nop>
nnoremap <Right> <Nop>
nnoremap <Up> <Nop>

" Remove newbie crutches in Visual Mode
vnoremap <Down> <Nop>
vnoremap <Left> <Nop>
vnoremap <Right> <Nop>
vnoremap <Up> <Nop>
