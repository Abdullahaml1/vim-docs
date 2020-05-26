# Copy and Paste Outside vim

vim has acess to the *os* registers that sotres copy and paste information. We need to acess the clipboard register to copy outside or even inside vim.

## The OS Registers:
1. a
2. b
3. + (the clipboard register)

* To copy to a spedific register `"(register name)y`. ex: `"ay` will copy the higlighted text to the `a` register.

* To paste from a specific register `"(register name)p`. Ex: `"+p` will paste form the `+` register.


## Create shortcut
```
vnormemap <C-c> "+y
map <C-v> "+P
```
for copying in both the clibpoead and the primary selection 
```
vnormemap <C-c> "*y @*=@*<CR>
```


##  Rsources 
1. [copy paste tutorial](https://vim.fandom.com/wiki/Copy,_cut_and_paste).
2. [youtube video](https://www.youtube.com/watch?v=E_rbfQqrm7g)
3. [stack overflow](https://stackoverflow.com/questions/11489428/how-to-make-vim-paste-from-and-copy-to-systems-clipboard
