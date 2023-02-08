VIM settings are stored in the .vimrc or \_vimrc file in your home directory

```
vim .vimrc
```

These are my settings for Norwegian keyboard

``` vim
set laststatus=2
set incsearch

set clipboard=unnamed



__________________________________________
"nnoremap <c-h> :set hlsearch!<cr>

" --------------[ Keymaps ]---------------
map  ø [
map! ø [
map  æ ]
map! æ ]
map  Ø {
map! Ø {
map  Æ }
map! Æ }
map  rø r[
map  rØ r{
map  ræ r]
map  rÆ r}
vmap Sø S[
vmap SØ S{
vmap Sæ S]
vmap SÆ S}

vnoremap <C-c> "+y
```