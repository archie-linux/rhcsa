### Create and edit text files
Use vi, nano, or cat:

- vi file.txt
- nano file.txt
- cat > file.txt

### Create, delete, copy, and move files and directories

- mkdir dir
- rm file
- cp file1 file2
- mv file1 file2

### Create hard and soft links

- ln file1 hardlink
- stat file1 # to check number of links (outputs 2)

- ln -s file2 softlink
- stat file2 # to check number of links (outputs 1)

### List, set, and change standard ugo/rwx permissions

- chmod 755 file
- chown user:group file

### Locate, read, and use system documentation

- man command
- info command
