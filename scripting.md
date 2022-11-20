# Scripting (MATA Cyber CP)

## Note on Scripting
`Scripting can be powerful, but is not the end-all be-all`
- **You should always understand what your scripts are doing and should check the output**
## Windows (PowerShell) [^1]
[^1]: [PowerShell Link](https://blog.netwrix.com/2018/02/21/windows-powershell-scripting-tutorial-for-beginners/)

- PowerShell is a scripting language native to Windows that works with CMDlets that allow you to automate processes on windows

### Running PowerShell 
- PowerShell can be run from the run window (`Windows+R`)
	- From the start menu (powershell.exe)
	- Or from the ISE (useful when creating scripts)

- Get-ExecutionPolicy: A policy that will limit the ability to run scripts 
	- **Restricted**: No scripts are allowed. This is the default setting.
	- **AllSigned**: You can run scripts signed by a trusted developer. Before executing the script Windows will ask for conformation.
	- **RemoteSigned**: You can run your own scripts or scripts signed by a trusted developer
	- **Unrestricted**: You can run any script you want
- This can be changed with the `Set-ExecutionPolicy` command

### PowerShell Cmdlets
- Cmdlet: PowerShell Commands
	- 3 Types: System, User, and Custom
	- Output results are either objects or an array of objects
	- Cmdlets can be piped together
- `Get-Help` to see available Cmdlets


#### Cmdlet Format
- \*Cmdlets always consists of a verb and a noun separated with a `-`
	- **Get**: To get something
	- **Set**: To define something
	- **Start**: To run something
	- **Stop**: To stop something that is running
	- **Out**: To output something
	- **New**: To create something

### Writing PS1 Files
- Each cmdlet has parameters that can be passed to it (options)
	- Use the ISE to better see these options
- Alias: Shorthand for longer commands
	- This can be used to write shorter code
	- Run `Get-Alias` to see all the possible aliases
- Comments are defined by `#` for single line and `#>` for multi-line
- Pipes (`|`): Allows you to pass the output of one command as the input of the next
	- Allows for commands to be chained into a single line


## Linux (Bash)
- Bash is a scripting based in Linux
	- Bash is the shell the most Linux systems run on and a bash script is a compilation of these commands into a file

### Running Bash Scripts
- As long as the script has been set to executable, then it can be run with `./[script-name]`
- To check if a script is executable, run `ls -la`
	- If the permissions has an 'x' in the last position then it can be run (clarify this)
- This permission can be set with `chmod +x`

### Commands
- Any valid Linux command is also a valid Bash command in a Bash script
- The command line can be a good place to test a command before you put it in a script

### Writing Shell Scripts [^2]

[^2]: [Bash Scripting How To](https://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO-1.html)
- Bash scripts are often denoted as `.sh`
- The first line is known as the sha-bang line (`#!/bin/bash`)
- Tells the interpreter that this is a bash script
- The rest of the script consists of variables, commands, and control logic

#### Variables and Control Flow
- Variables are denoted as `VARIABLE=...` and can be accessed using `$[var_name]`
- Bash has no data types so variables work like weakly typed languages in that you do not need to specify a data type
- Variables can hold a number, string, or character

- NOTE: variables can be local to a function and are preceded with the local keyword

- You can use functions in bash and parameters can be passed to them
``` function func_name {
		code
	}
```
- Parameters are accessed as `$1, $2, $3, ..., $n` 
- If statements, while loops, for loops, and other control flow methods can be used in Bash

```
if [ CONDITION ]; then
	code
else
	code
fi
```

- FOR Example
```
for i in INTERATOR;
do
	code
done
```
- Note for loops are a bit different in Bash they let you iterate of a series of 'words' in a string

- WHILE Example
```
while [ CONDITION ]; do
	code
done
```

- UNTIL Example
```
until [ CONDITION ]; do
	code
done
```
