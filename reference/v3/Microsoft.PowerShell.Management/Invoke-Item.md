---
external help file: PSITPro3_Management.xml
online version: http://go.microsoft.com/fwlink/?LinkID=113345
schema: 2.0.0
---

# Invoke-Item
## SYNOPSIS
Performs the default action on the specified item.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Invoke-Item [-Path] <String[]> [-Credential <PSCredential>] [-Exclude <String[]>] [-Filter <String>]
 [-Include <String[]>] [-Confirm] [-WhatIf] [-UseTransaction]
```

### UNNAMED_PARAMETER_SET_2
```
Invoke-Item [-Credential <PSCredential>] [-Exclude <String[]>] [-Filter <String>] [-Include <String[]>]
 -LiteralPath <String[]> [-Confirm] [-WhatIf] [-UseTransaction]
```

## DESCRIPTION
The Invoke-Item cmdlet performs the default action on the specified item.
For example, it runs an executable file or opens a document file in the application associated with the document file type.
The default action depends on the type of item and is determined by the Windows PowerShell provider that provides access to the data.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
PS C:\>invoke-item C:\Test\aliasApr04.doc
```

This command opens the file aliasApr04.doc in Microsoft Office Word.
In this case, opening in Word is the default action for .doc files.

### -------------------------- EXAMPLE 2 --------------------------
```
PS C:\>invoke-item "C:\Documents and Settings\Lister\My Documents\*.xls"
```

This command opens all of the Microsoft Office Excel spreadsheets in the C:\Documents and Settings\Lister\My Documents folder.
Each spreadsheet is opened in a new instance of Excel.
In this case, opening in Excel is the default action for .xls files.

## PARAMETERS

### -Credential
Specifies a user account that has permission to perform this action.
The default is the current user.

Type a user name, such as "User01" or "Domain01\User01", or enter a PSCredential object, such as one generated by the Get-Credential cmdlet.
If you type a user name, you will be prompted for a password.

This parameter is not supported by any providers installed with Windows PowerShell.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Current user
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Exclude
Omits the specified items.
The value of this parameter qualifies the Path parameter.
Enter a path element or pattern, such as "*.txt".
Wildcards are permitted.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: True
```

### -Filter
Specifies a filter in the provider's format or language.
The value of this parameter qualifies the Path parameter.
The syntax of the filter, including the use of wildcards, depends on the provider.
Filters are more efficient than other parameters, because the provider applies them when retrieving the objects rather than having Windows PowerShell filter the objects after they are retrieved.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: True
```

### -Include
Performs the default action only on the specified items.
The value of this parameter qualifies the Path parameter.
Enter a path element or pattern, such as "*.txt".
Wildcards are permitted.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: True
```

### -LiteralPath
Specifies a path to the item.
The value of LiteralPath is used exactly as it is typed.
No characters are interpreted as wildcards.
If the path includes escape characters, enclose it in single quotation marks.
Single quotation marks tell Windows PowerShell not to interpret any characters as escape sequences.

```yaml
Type: String[]
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: 
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Path
Specifies the path to the selected item.

```yaml
Type: String[]
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: 1
Default value: 
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseTransaction
Includes the command in the active transaction.
This parameter is valid only when a transaction is in progress.
For more information, see Includes the command in the active transaction.
This parameter is valid only when a transaction is in progress.
For more information, see

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### System.String
You can pipe a string that contains a path to Invoke-Item.

## OUTPUTS

### None
The command does not generate any output.
However, output might be generated by the item that it invokes.

## NOTES
* The Invoke-Item cmdlet is designed to work with the data exposed by any provider. To list the providers available in your session, type "Get-PsSProvider". For more information, see about_Providers.

*

## RELATED LINKS

[Clear-Item](Clear-Item.md)

[Copy-Item](Copy-Item.md)

[Get-Item](Get-Item.md)

[Invoke-Command](../Microsoft.PowerShell.Core/Invoke-Command.md)

[Move-Item](Move-Item.md)

[New-Item](New-Item.md)

[Remove-Item](Remove-Item.md)

[Rename-Item](Rename-Item.md)

[Set-Item](Set-Item.md)

[about_Providers](about_Providers.md)
