---
layout: post
title: Setting Up A Thesis Environment with Latex and Vim
---

# Vimtex

That's it. It's just vimtex, vim and latex. I will be trying to write as efficiently as possible, so I'm implementing a 10 times rule.

1. If I have done something ten times, find a way to make it more efficient.

Because of the extensibility of vim, this can lead to an unending rabbit hole of optimizations, so I'm not going to just blindly apply it.


## vimtex and subfile

I did stumble across something which delayed me a little. vimtex has a really nice feature where you can type \cite{ and press <c-x> <c-o>, it will omni complete by searching your bibtex file. However, if you are in a subfile, then the omni-complete gives you nothing. 

To fix this, you first have to type :VimtexToggleMain, which makes the subfile you are in the mainfile. (This is documented, kinda, in the help.) There is no discussion of VimtexToggleMain in the omni-complete section, I just had to try it and hope for the best. 

## vim and regular expressions

I also, didn't know this, but you can use regular expressions or vim patterns when doing omni complete-- very helpful for adding links to files!

![vim-regex](/assets/vimregex.gif){:class='img-responsive'} 

