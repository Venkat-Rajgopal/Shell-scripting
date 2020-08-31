# VIM Editor

Vim as a inbuilt editor has a rich history; it originated from the Vi editor (1976), and it’s still being developed today. Vim has some really cleam ideas behind it, and for this reason, lots of tools support vim.

## Editing in VIM
Vim has multiple operating modes, keeping in mind the different ideas like reading, navigation, edits etc. Here are the main ones. 


Modes | Shortcuts 
--- | ---
- **Normal**: for moving around a file and making edits |
- **Insert**: for inserting text | `i`
- **Replace**: for replacing text | `R`
- **Visual** (plain, line, or block): for selecting blocks of text | `v`
- **Command-line**: for running a command | `:`

You change modes by pressing `<ESC>` to switch from any mode back to Normal mode. 

## Command Line 
VIM has the following command line options which can entered after typing `:` in *Normal Model*. 

`:q` quit (close window)

`:w` save (“write”)

`:wq` save and quit

`:e` {name of file} open file for editing

`:ls` show open buffers

`:help` {topic} open help

    `:help :w` opens help for the :w command
    `:help w` opens help for the w movement

## Movements inside Vim 
Movements inside VIM are extremely essential and these keys will help you move around the vim editor efficiently. 

Movement | Keys 
--- | ---
(left, down, up, right) | `hjkl`
Lines | `0` (beginning of line), `^` (first non-blank character), `$` (end of line)
Scroll | `Ctrl-u` (up), `Ctrl-d` (down)
File | `gg` : beginning of line. `G` End of line. 
Start of the line | `.`
End of the line | `$`
Move to next word | `w`

## Edits in Vim

Edits | Keys 
--- | ---
 insert line below / above | `o` , `O`
 delete {motion} | `dw` is delete word, `d$` is delete to end of line, `d0` is delete to beginning of line  
 delete character  | `x`
 undo | `u`
 copy, paste | `y` to copy / “`p`” to paste. 

## Counts

Counts | Keys 
--- | ---
move 3 words forward | `3w`
move 5 lines down | `5j`
delete 7 words | `7dw`
