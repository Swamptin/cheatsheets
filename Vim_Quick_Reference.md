---
title:
- Vim Quick Reference Guide
author:
- Eoghan O'Brien
---

## Movement

h   move one character left
j   move one row down
k   move one row up
l   move one character right
w   move to beginning of next word
b   move to previous beginning of word
e   move to end of word
W   move to beginning of next word after a whitespace
B   move to beginning of previous word before a whitespace
E   move to end of word before a whitespace
**All the above movements can be preceded by a count; e.g. 4j moves down 4 lines.**
:{number} jumps to that line number

0   move to beginning of line (zero)
$   move to end of line
_   move to first non-blank character of the line
g\_  move to last non-blank character of the line

gg  move to first line
G   move to last line
ngg move to n'th line of file (n is a number; 12gg moves to line 12)
nG  move to n'th line of file (n is a number; 12G moves to line 12)
H   move to top of screen
M   move to middle of screen
L   move to bottom of screen

zz  scroll the line with the cursor to the center of the screen
zt  scroll the line with the cursor to the top
zb  scroll the line with the cursor to the bottom

Ctrl-D  move half-page down
Ctrl-U  move half-page up
Ctrl-B  page up
Ctrl-F  page down
Ctrl-O  jump to last (older) cursor position
Ctrl-I  jump to next cursor position (after Ctrl-O)
Ctrl-Y  move view pane up
Ctrl-E  move view pane down

%   jump to matching bracket { } [ ] ( )
}   Move down by paragraph
{   Move up by paragraph

## Auto-complete

Ctrl-X Ctrl-P tab completion from buffer
Ctrl-X Ctrl-L Autocomplete a previous line.

Ctrl-n  Autocomplete from suggested words

https://www.youtube.com/watch?v=3TX3kV3TICU <-- This goes into built in
	autocomplete much better than I have here.

## Search/replace

/   search for the following string
?   Search backwards
n   next matching search pattern
N   previous matching search pattern
\*   next whole word under cursor
\#   previous whole word under cursor
g\*  next matching search (not whole word) pattern under cursor
g#  previous matching search (not whole word) pattern under cursor
gd  go to definition/first occurrence of the word under cursor
V   Highlight a line (Visual line)
vap Highlight an entire paragraph
Ctrl-V Highlight a block (Visual Block - Can delete columns)

fx  to next 'x' after cursor, in the same line (x is any character)
FX  to previous 'X' before cursor (f and F put the cursor on X)
tX  til next 'X' (similar to above, but cursor is before X)
TX  til previous 'X'
;   repeat above, in same direction
,   repeat above, in reverse direction
%s   search. ie: :%s/foo/bar/g

## Dictionary Use
zg  Add word to dictionary
zw  Add word as incorrect to dictionary
zuw Undo zw
z=  Brings up the dictionary suggestions
[s  Moves to next miss spelled work
]s  Moves to previous miss spelled work

## Manipulation ie: delete/indent/etc.

~   Capitalize the char under the cursor.
>   Indent a line
diw Delete Inner Word
di{ Delete inside {...}
da{ Delete including {...}
d$  Delete to end of line
x   Save and close
q!  Quit without saving
r   Replace a character without entering insert mode
cw  Change Word -> deletes word and puts you in insert mode.
i   Insert mode
o   Enters insert mode on a new line below the current line.
O   Enters insert mode on a new line above the current one (capital o)
A   Enters insert mode at the end of the current line.
w   Write without a close

## Misc

tabn Next tab
tabp Previous tab
tabm {i} Move a tab to position i/i+1

rnu  	Relative Line Numbers
nornu	Unset Relative Line Numbers

gg=G Reindent a file, automated indentation.

gqG  Reapply text width formating

(Opening multiple files in one vim on terminal ie: vim this that other)
next Next file
prev Previous file

## Macros

q<letter><commands>q Record a series of commands in register <letter>
<number>@<letter>    Apply series of commands to current line/x lines
@@		     Repeat macro just run

## Fold activation and deactivation <-- This will allow you to collapse methods

To activate fold use following command:
:set foldenable
:set foldmethod=indent
To deactivate fold use following command:
:set nofoldenable 

:setlocal foldmethod=manual
zfa} create a fold until }
zO   Open a fold
zC   Close a fold

:vert diffsplit <filename>
:diffsplit filename		(CTRL+w CTRL+w to change files. )



https://www.tutorialspoint.com/vim/vim_tutorial.pdf
