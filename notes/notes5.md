# Notes Lecture 5 | Command Line text editors 
## The basics of Nano
* **Nano** is the default text editor of Ubuntu.
* Start nano type nano in the cmd line
and the program opens. 
* The options are listed on the bottom of the text editor.
* **^O** to save 
* After you save you it asks for the file name 
* Ctrl X to exit
* nano is easy to use and very limited

## The basic of Vim
### What is Vim?
* The vi command-line text editor is included in all POSIX compliant operating system
* Vim is not installed on ubuntu
* Vi is installed on all linux systems
* Why VIM?
  * vim is lighter,easier to learn, and has more features.

### How to start and quit vim
* Type **VIM** to start
* To quit vim, press esc and type :q and enter
**:** - entering cmd mode
**q** - quit
**a** - all buffers
**!** - force 
**:qa** - quit all now
To set line number-set number

### Vim modes
* ***Insert mode***: used for writing text
  * from normal mode press i to enter insert mode
* ***Normal mode***: used for manipulating text
  * from insert mode to switch back to normal mode press esc
* ***Command mode***: used for entering vim commands
* ***Visual mode***: used for navigation and manipulation of text selections
* ***Select mode***: similar to visual mode

### Insert text
* You can create a file and open vim at the same time by typing vim and a file name.
* Example: 
  * vim notes.txt

### Saving and quitting vim
* To save a text file you need to enter normal mode using : and the use the w key
* **:w** - new.txt will save the file as new.txt
* **:wq** - will save the file and quit

### Editing a file with vim
* You can tell vim that you want to edit another file by using the e command
* **:e** new.txt - will open new.txt file and allow you to edit

### Navigating a file
*In normal mode use the keys:
  * *H = left*
  * *J = down*
  * *K = up*
  * *L = right*
* By adding the number after the letter
10H, it will move 10 character to the left.

### To move between words using w or e
* **w** : moves word by word to the beginning of each word
* **e** : moves word by word to the end of each word
* To move between sentences use ()
    * **(** for previous sentences 
    * **)** for next sentence
* To move between paragraphs use {}
  * **{** for previous paragraph 
  * **}** for  next paragraph

### Searching words in vim
* Use **/** and the word you are looking for to search forward
  * /hello
* letter **n** will repeat the search for the next word
* **?** To search backward
  * ?hello

### Screen Movement
* **G** (uppercase g) Moves to end of the file
* **gg** (2 lowercase g) moves to the beginning of a file
* **CTRL + f** moves a page forward at a time
* **CTRL + b** moves a page backward at a time


### Moving to Lines
* To move to a specific line use : plus the line number 
  * **:8** will move you to line 8
* **$** will move to the end of the line
* **0** will move to the beginning of the line

### Delete text and copy and paste
* In *normal mode* under the cursor is print, press **d** for delete (d) **w** for the word and the word is gone. 
* To undo press **u** . 
* To delete whole line **dd** to under cursor. 
* copy current word **y** and then **w** for word. 
* paste for **p** after the insertion point. 
* before insertion point **P** copy
* whole line - **yy**

### Change text
* **cw** = deletes the word under the cursor and enters insert mode
* **c /hello** = deletes until it finds the word hello and enters insert mode

### Work in split screen mode
* To open a new VIM window next to the existing one, press:
  * CTRL + w then press v
* To open a new window below the current window press:
  * CTRL + w then press j
* To move to the window on the right/left/down/up press: 
  * CTRL + w then press h/l/j/k 


