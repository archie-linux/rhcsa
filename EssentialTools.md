### Understand and Use Essential Tools

Access a shell prompt and issue commands with correct syntax
Use terminal emulators (e.g., GNOME Terminal) or TTY consoles. Issue commands like ls, pwd, and echo. Syntax:

- command [options] [arguments]

### Use input-output redirection (>, >>, |, 2>, etc.)

Example:

- echo "Hello" > file.txt      # Overwrite output to file
- echo "World" >> file.txt     # Append output to file
- ls | grep "txt"              # Pipe output
- ls nonexistent 2> error.log  # Redirect errors

### Use grep and regular expressions to analyze text

Example:

- grep 'pattern' file.txt
- grep -E '^abc|xyz$' file.txt  # Extended regex: starts with abc or ends with xyz

### Access remote systems using SSH

- ssh user@remote-host

### Transfer Files using scp

- scp file user@remote-host:/home/remote-user

### Log in and switch users in multiuser targets

- su - username
