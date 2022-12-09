configure under `~/.vimrc`

Vim Modes: Normal, Insert, Visual, Command

| Vim Modes      | Description                                                                                                                                                                                                    |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `N`ormal       | The initial mode you find yourself in, you are unable to type in this mode. This is the "editor" part of the text editor.                                                                                      |
| `I`nsert       | The mode you are used to in a text editor, your type letters directly, so this is the mode you use to write anything.                                                                                          |
| `V`isual       | *Visual* visualizes selecting/highlighting of text. There is also "visual block mode", a *very* useful sub-mode of visual mode which lets you work with actual blocks in your text and multiple lines at once. |
| Command<Br>`:` | By pressing `:` (in normal or visual mode), you can type in a command at the bottom of window. Commands are essential and include functions such as:<Br>:w (write)<Br>:q (quit)<Br>:wq (write and quit)                                   |

Normal (Default Mode)
Insert (I)
Visual (V)
Command (:)

### ESSENTIAL COMMANDS

'#' manually input number

NAVIGATION

#h (right)
#l (left)

#k (up)
#j (down)

0  (beginning of line)
$  (end of line)
gg (beginning of file)
G  (end of file)

#### EDITING (insert mode)

##### --Inserting
i (left of cursor)
a (right of cursor)
I (initial position of text)
A (append to text)
o (new line on bottom)
O (new line on top)

##### --Cut,Copy,Paste 

| Key(s) | Function                            |
| ------ | ----------------------------------- |
| v      | (selecting) => x (delete selection) |
| y      | (copying)                           |
| d      | (cut)                               |
| p      | (paste after cursor)                |
| P      | (paste before cursor)               |

> Does not use system clipboard by default, but a thing called registers

##### --Deleting
#d + direction[h/l/space]  (deletes # of characters)
dd (delete line)
D  (delete everything from cursor to end of line)
x  (deletes cursor character/selection)
X  (deletes character before cursor)

### Configuration
NUMBERING
:set number (displays line numbers)
:set nonumber (not show line numbers)
:set relativenumber (set relative numbers)
:set norelativenumber (reset to absolute numbering)