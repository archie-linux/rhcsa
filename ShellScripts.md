### Create simple shell scripts

Example:

#!/bin/
echo "Hello, World!"

### Conditionally execute code

if [ -f file ]; then echo "File exists"; fi

### Use looping constructs

for i in {1..5}; do echo $i; done

### Process script inputs

echo "Argument 1: $1"

### Process output of shell commands

files=$(ls *.txt)
echo $files
