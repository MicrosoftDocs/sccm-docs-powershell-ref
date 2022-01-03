---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Get-CMScript
---

# Get-CMScript

## SYNOPSIS

Get a PowerShell script in Configuration Manager.

## SYNTAX

### ByName (Default)
```
Get-CMScript [-Author <String>] [-Fast] [-ScriptName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMScript [-Author <String>] [-Fast] -ScriptGuid <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a Configuration Manager PowerShell script. These scripts are integrated and managed in Configuration Manager. For more information, see [Create and run PowerShell scripts from the Configuration Manager console](/mem/configmgr/apps/deploy-use/create-deploy-scripts).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all unapproved scripts

This command gets all scripts in Configuration Manager that aren't approved.

```powershell
Get-CMScript -Fast | Where-Object { -not $_.ApprovalState }
```

### Example 2: Get scripts by using name

This command gets all scripts that have a name that begins with the letter `D`.

```powershell
Get-CMScript -ScriptName "D*"
```

### Example 3: Get scripts from a specific author

This command gets all scripts for the author with username **jqpublic**. Since it uses the asterisk (`*`) wildcard, the specific domain doesn't matter. It then returns a table that lists the script name, approval state, and last update time.

```powershell
Get-CMScript -Fast -Author "*jqpublic" | Select-Object ScriptName, ApprovalState, LastUpdateTime
```

## PARAMETERS

### -Author

Specify the author of the script to get. For example, `contoso\jqpublic`.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptGuid

Applies to version 2010 and later. Specify the GUID of a script to get.

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptName

Specify a script name to get.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_Scripts
### IResultObject#SMS_Scripts

## NOTES

This cmdlet returns an object for the **SMS_Scripts** WMI class.

## RELATED LINKS

[Approve-CMScript](Approve-CMScript.md)
[Deny-CMScript](Deny-CMScript.md)
[Invoke-CMScript](Invoke-CMScript.md)
[New-CMScript](New-CMScript.md)
[Remove-CMScript](Remove-CMScript.md)
[Set-CMScript](Set-CMScript.md)

[Create and run PowerShell scripts from the Configuration Manager console](/mem/configmgr/apps/deploy-use/create-deploy-scripts)
