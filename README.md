# Vimrc

filetype plugin indent on

" show existing tab with 4 spaces width
set tabstop=4
" when indenting with '>', use 4 spaces width
set shiftwidth=4
" On pressing tab, insert 4 spaces
set expandtab
set ruler
set number
highlight LineNr term=bold cterm=NONE ctermfg=DarkGrey ctermbg=NONE gui=NONE guifg=DarkGrey guibg=NONE

function! ToggleHome(var)
    if col(".") == 1
        normal 0w
    else
        normal 0
    endif
    if a:var == 1
        startinsert
    endif
endfunction

noremap <silent> <Home> :call ToggleHome(0)<CR>
inoremap <silent> <Home> <ESC>:call ToggleHome(1)<CR>
  
