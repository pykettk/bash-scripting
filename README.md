# bash-scripting
https://www.udemy.com/course/bash-scripting/learn/lecture/5739688#overview

## Cheatsheet
### Testing Files
`-d FILE` checks if the file is a directory 

`-e FILE` checks if the file exists

`-f FILE` checks if the file exists and is a regular file (i.e. not a symlink)

`-r FILE` checks if the file is readable

`-s FILE` checks if the file exists and is not empty

`-w FILE` checks if the file is writable

`-x FILE` checks if the file is executable

### String Operators
`-z STRING` checks if the string is empty

`-n STRING` checks if the string is not empty

`STRING1 = STRING2` checks equality between two strings

`STRING1 != STRING2` checks inequality between two strings

### Arithmetic Operators
`NUM1 -eq NUM2` checks if the two numbers are equal 

`NUM1 -ne NUM2` checks if the two numbers are not equal 

`NUM1 -lt NUM2` checks if number one is less than number two 

`NUM1 -le NUM2` checks if number one is less than or equal to number two 

`NUM1 -gt NUM2` checks if number one is greater than number two 

`NUM1 -ge NUM2` checks if number one is greater than or equal to number two 

### Logical Operators
`&&` is AND

`||` is OR

### Control Statements
```bash
if [ condition ] then
    # do this
elif [ another condition ] then
    # do that
else
    # do something else
fi
```

```bash
for VARIABLE_NAME in ITEM_1 ITEM_N do
    # do this
    # do that
    # do something else
done
```

### Script Parameters
Scripts will often accept parameters. These can be accessed using `$X` where `X` is the parameter number.
`$0` is a special parameter and is reserved for the name of the shell or shell script.
`$@` is another special parameter. This parameter is an array of all of the parameters passed to the script.

### User Input
`read -p "PROMPT MESSAGE" VAR` will prompt the user for input using the `"PROMPT MESSAGE"` and store it in `$VAR`

### Exit Status
Every command returns an exit status. This return code can range from `0` to `255`. `0` means the command executed
successfully whilst any other return code means an error occurred - which can be useful for error checking.

`$?` is a variable that contains the return code of the previously executed command.

`exit NUM` explicitly defines the return code
