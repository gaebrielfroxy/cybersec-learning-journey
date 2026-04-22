
`cmdlets` - `Verb-Noun`
eg. `Get-Content` `Set-Location`
`Get-Command` - list of commands
to open Powershell type `powershell` in cmd using remmina
`Get-Command -CommandType "Function"` - filters all cmdlets with "Function" CommandType
`Get-Help` - provides detailed information about cmdlets (parameters, examples and usage)
eg. `Get-Help Get-Date` returns details about "Get-Date" cmdlet, related commands, syntax, etc.
`Get-Alias` - shortcuts for cmdlets like `cd` - `Set-Location` or `clc` - `Clear-Content` 
You can search in online repositories for extended functionality of cmdlets:
`Find-Module -Name "PowerShell*"`
Then you can install from repository with `Install-Module` - eg. `Install-Module -Name "PowerShellGet"`
If You Don't know exact name of the module use wildcard `*`
`Get-ChildItem` - list the files in location specified with 
`-Path`  Parameter
`Remove-Item`
`Copy-Item`
`Get-Content` - similar to `type` and `cat`

`Piping | Piping` - output of first command will be input of the second, with cmdlets it passes objects not just a text, which means also properties and description and interactions with data
eg. `Get-ChildItem | Where-Object -Property "Extenstion" -eq ".txt"` 
`Where-Object` - filters files by their property

**Operators**
`-ne` - not equal
`-gt` - greater than
`-ge` - greater than or equal to
`-lt` - less than
`-le` - less than or equal to
`-like` - filter properties that matched specific pattern (eg. 
Get-ChildItem | Where-Object -Property "Name" -like "ship*")

