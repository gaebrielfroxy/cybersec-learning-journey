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

