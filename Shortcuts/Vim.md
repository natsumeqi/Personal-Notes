## Vim

Level 1
`cat filename`		//preview the content of the file
Load/Save/Quit/Change File (Buffer)
`:new filename.suffix`	//new file
`:e <path/to/file>` → open
`:w` → save
`:file filename.suffix`	//save uncreated file 
`:saveas <path/to/file>` → save to <path/to/file>
`:x` 				//exit file with save
`:x, ZZ` or `:wq` → save and quit (:x only save if necessary)
`:q!` → quit without saving, also `:qa!` to quit even if there are modified hidden buffers.
`:bn` (resp. `:bp`) → show next (resp. previous) file (buffer)
`i` → Insert mode. Type `ESC` to return to Normal mode.
`:help <command>` → Show help about <command>. You can use :help without a <command> to get general help.



Level 2
Insert mode variations:
`a` → insert after the cursor
`A`→ insert at the end of line
`I`→ insert at the beginning of line
`o` → insert a new line after the current one
`O` → insert a new line before the current one
`cw` → replace from the cursor to the end of the word

Basic moves
`0` → go to column 0
`^` → go to first character on the line
`$` → go to the last column
`g_` → go to the last character on the line
`fa` → go to next occurrence of the letter `a` on the line. `;`(resp. `,`) will find the next (resp. previous) occurrence.
`t,` → go to just before the character `,`.
`3fa` → find the 3rd occurrence of `a` on this line.
`F` and `T` → like `f` and `t` but backward.

`w`  `b` `e` `ge`  move forward or backword to the start or end of a word

N`G` → Go to line N
`gg` → shortcut for `1G` - go to the start of the file
`G` → Go to last line 

`%` : Go to the corresponding `(`, `{`, `[`.
`*` (resp. `#`) : go to next (resp. previous) occurrence of the word under the cursor





格式化全文： gg=G

Copy/Paste
`P` → paste before, remember p is paste after current position.
`yy` → copy the current line, easier but equivalent to `ddP`
`dd` → Delete (and copy) the current line
`x` → Delete the char under the cursor
A useful tip is: dt" → remove everything until the ".

Undo/Redo
`u` → undo
`<C-r>` → redo




Level 3
`. `→ (dot) will repeat the last command
`N<command>` → will repeat the command N times



search
If your cursor stopped on a match before the one you were aiming for, press ; to repeat the search. Keep pressing ; until you hit your mark. If you overshoot, press , to reverse the search.
`/pattern` → search for pattern
`nohl`→no highlight o


Ctrl+w q    close current window
:sp <filename>    split a new file vertically
:vs <filename>  horizontal split
:split → create a split (:vsplit create a vertical split)
<C-w><dir> : where dir is any of hjkl or ←↓↑→ to change the split.
<C-w>_ (resp. <C-w>|) : maximise the size of the split (resp. vertical split)
<C-w>+ (resp. <C-w>-) : Grow (resp. shrink) split
<C-w> =    same height in all windows


Level 4

**faster**

Most commands can be used using the following general format:
<start position><command><end position>

For example : `0y$` means
0 → go to the beginning of this line
y → yank from here
$ → up to the end of this line
We also can do things like `ye`, yank from here to the end of the word. But also `y2/foo` yank up to the second occurrence of “foo”.

But what was true for y (yank), is also true for `d` (delete), `v` (visual select), `gU` (uppercase), `gu` (lowercase), etc…

**Zone selection**
These command can only be used after an operator in visual mode. Their main pattern is:
<action>a<object> and <action>i<object>
Where action can be any action, for example, `d` (delete), `y` (yank), `v` (select in visual mode). The object can be: `w` a word, `W` a WORD (extended word), `s` a sentence, `p` a paragraph. But also, natural character such as `"`, `'`, `)`, `}`, `]`.

**Select rectangular blocks: <C-v>.**
Rectangular blocks are very useful for commenting many lines of code. Typically: 0<C-v><C-d>I-- [ESC]
^ → go to the first non-blank character of the line
<C-v> → Start block selection
<C-d> → move down (could also be jjj or %, etc…)
I-- [ESC] → write -- to comment each line

**Completion: `<C-n>` and `<C-p>`** 
In Insert mode, just type the start of a word, then type `<C-p>`, magic…

**Macros : qa do something q, @a, @@**
`qa` record your actions in the register `a`. Then `@a` will replay the macro saved into the register `a` as if you typed it. `@@` is a shortcut to replay the last executed macro.
On a line containing only the number 1, type this:
`qaYp<C-a>q` →
`qa` start recording.
`Yp` duplicate this line.
`<C-a>` increment the number.
`q` stop recording.
`@a` → write 2 under the 1
`@@` → write 3 under the 2
Now do `100@@` will create a list of increasing numbers until 103.

**Visual selection: v,V,<C-v>** 
We saw an example with <C-v>. There is also v and V. Once the selection has been made, you can:
`J` → join all the lines together.
`<` (resp. `>`) → indent to the left (resp. to the right).
`=` → auto indent
Add something at the end of all visually selected lines:
`<C-v>` 
go to desired line (jjj or <C-d> or /pattern or % etc…)
`$` go to the end of the line
`A`, write text, ESC.




## Plugin

NERDTree
tr   开启和隐藏

Ctrl-p 搜索