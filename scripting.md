# Scripting (MATA Cyber CP)

## Note on Scripting
`Scripting can be powerful, but is not the end-all be-all`
- **You should always understand what your scripts are doing and should check the output**
## Windows (PowerShell)
- PowerShell is a scripting language native to Windows that works with CMDlets that allow you to automate processes on windows

### Running PowerShell 
[^1]:(https://blog.netwrix.com/2018/02/21/windows-powershell-scripting-tutorial-for-beginners/)
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


