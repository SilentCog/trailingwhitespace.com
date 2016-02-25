---
title: Vim commands of note
author: mimiflynn
date: 2016-02-25
template: article.jade
---

Lately, I decided to switch from trusty old Sublime Text 3 to Vim. Why?

<span class="more"></span>

## Layout

`ctrl+w, v` opens new panel vertically

`ctrl+w, h` opens new panel horizonally

`ctrl+w, w` switches to next panel

## Folding

`zo` open

`zc` close

[Folding documentation](http://vim.wikia.com/wiki/Folding)

## Moving around a file

`0` beginning of the line

`^` first non-blank character in a line

`G` end of file

`gg` beggin of file

`H` top of the screen

`M` middle of the screen

`L` bottom of the screen

[Moving around](http://vim.wikia.com/wiki/Moving_around)


## Delete
`dw` deletes word

`d$` deletes to the end of the line

`d^` deletes to the beginning of the line

`dit` delete inside tag where cursor is located

## Change

`caw` change word

`cas` change sentence

`cb<` replace whole element

`ci"` change inside quote when inside quotes

[A powerful vim command I never knew](http://everythingsysadmin.com/2010/09/a-powerful-vim-command-i-never.html)

## Buffer

`:b 4` go to buffer #4

## Search and Replace

`:%s/foo/bar/g` Find each occurrence of 'foo' (in all lines), and replace it with 'bar'.

`:s/foo/bar/g` Find each occurrence of 'foo' (in the current line only), and replace it with 'bar'.

`:%s/foo/bar/gc` Change each 'foo' to 'bar', but ask for confirmation first.

`:%s/\<foo\>/bar/gc` Change only whole words exactly matching 'foo' to 'bar'; ask for confirmation.

[Search and Replace](http://vim.wikia.com/wiki/Search_and_replace)

## Marks

`:marks` list current marks

### Setting a mark
`m` plus a letter to identify the mark so `ma`

### Deleting marks
`:delmarks a`	delete mark a

### Jumping to a mark
`'a` jump to the first non blank character in the line at mark 'a'

`\`a` jump to mark

### Modifying content in a mark
`d'a`	delete from current line to line of mark a

`d`a`	delete from current cursor position to position of mark a

`c'a`	change text from current line to line of mark a


[Marks](http://vim.wikia.com/wiki/Using_marks)


# Plugin Specific Notes

## Cntrl-P

`fn+f5` refreshed buffer when search panel is open


# Personal .*RC notes

`cntrl+n` Nerdtree



