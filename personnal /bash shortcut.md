# Bash terminal shortcuts

## Controlling the Screen
The following shortcuts allow you to control what appears on the screen.

- __Ctrl+L:__ Clear the screen. This is similar to running the “clear” command.

- __Ctrl+S:__ Stop all output to the screen. This is particularly useful when running commands with a lot of long, verbose output, but you don’t want to stop the command itself with Ctrl+C.

- __Ctrl+Q:__ Resume output to the screen after stopping it with Ctrl+S.

## Moving the Cursor
Use the following shortcuts to quickly move the cursor around the current line while typing a command.


- __Ctrl+A or Home:__ Go to the beginning of the line.

- __Ctrl+E or End:__ Go to the end of the line.

- __Alt+B:__ Go left (back) one word.

- __Ctrl+B:__ Go left (back) one character.

- __Alt+F:__ Go right (forward) one word.

- __Ctrl+F:__ Go right (forward) one character.

- __Ctrl+XX:__ Move between the beginning of the line and the current position of the cursor. This allows you to press Ctrl+XX to return to the start of the line, change something, and then press Ctrl+XX to go back to your original cursor position. To use this shortcut, hold the Ctrl key and tap the X key twice.


## Deleting Text
Use the following shortcuts to quickly delete characters:


- __Ctrl+D or Delete:__ Delete the character under the cursor.

- __Alt+D:__ Delete all characters after the cursor on the current line.

- __Ctrl+H or Backspace:__ Delete the character before the cursor.
Fixing Typos
These shortcuts allow you to fix typos and undo your key presses.


- __Alt+T:__ Swap the current word with the previous word.

- __Ctrl+T:__ Swap the last two characters before the cursor with each other. You can use this to quickly fix typos when 
you type two characters in the wrong order.

- __Ctrl+_:__ Undo your last key press. You can repeat this to undo multiple times.
Cutting and Pasting
Bash includes some basic cut-and-paste features.


- __Ctrl+W:__ Cut the word before the cursor, adding it to the clipboard.

- __Ctrl+K:__ Cut the part of the line after the cursor, adding it to the clipboard.

- __Ctrl+U:__ Cut the part of the line before the cursor, adding it to the clipboard.

- __Ctrl+Y:__ Paste the last thing you cut from the clipboard. The y here stands for “yank”.

## Capitalizing Characters
The bash shell can quickly convert characters to upper or lower case:

- __Alt+U:__ Capitalize every character from the cursor to the end of the current word, converting the characters to upper case.

- __Alt+L:__ Uncapitalize every character from the cursor to the end of the current word, converting the characters to 
lower case.

- __Alt+C:__ Capitalize the character under the cursor. Your cursor will move to the end of the current word.
Tab Completion

- __RELATED:__ Use Tab Completion to Type Commands Faster on Any Operating System

Tab completion is a very useful bash feature. While typing a file, directory, or command name, press Tab and bash will automatically complete what you’re typing, if possible. If not, bash will show you various possible matches and you can continue typing and pressing Tab to finish typing.


- __Tab:__ Automatically complete the file, directory, or command you’re typing.
For example, if you have a file named really_long_file_name in /home/chris/ and it’s the only file name starting with “r” in that directory, you can type /home/chris/r, press Tab, and bash will automatically fill in /home/chris/really_long_file_name for you. If you have multiple files or directories starting with “r”, bash will inform you of your possibilities. You can start typing one of them and press “Tab” to continue.



## Working With Your Command History
RELATED: How to Use Your Bash History in the Linux or macOS Terminal

You can quickly scroll through your recent commands, which are stored in your user account’s bash history file:


- __Ctrl+P or Up Arrow:__ Go to the previous command in the command history. Press the shortcut multiple times to walk back through the history.

- __Ctrl+N or Down Arrow:__ Go to the next command in the command history. Press the shortcut multiple times to walk forward through the history.

- __Alt+R:__ Revert any changes to a command you’ve pulled from your history if you’ve edited it.
Bash also has a special “recall” mode you can use to search for commands you’ve previously run:

- __Ctrl+R:__ Recall the last command matching the characters you provide. Press this shortcut and start typing to search your bash history for a command.

- __Ctrl+O:__ Run a command you found with Ctrl+R.

- __Ctrl+G:__ Leave history searching mode without running a command.


## emacs vs. vi Keyboard Shortcuts
The above instructions assume you’re using the default keyboard shortcut configuration in bash. By default, bash uses emacs-style keys. If you’re more used to the vi text editor, you can switch to vi-style keyboard shortcuts.

The following command will put bash into vi mode:

```set -o vi```

The following command will put bash back into the default emacs mode:

```set -o emacs```


With a few of these in your toolbelt, you’ll be a Terminal master in no time.