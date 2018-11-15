---
external help file: AdminUI.PS.ClientOperations.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMScript

## SYNOPSIS

Gets Configuration Manager PowerShell scripts.

## SYNTAX

```powershell
Get-CMScript [-Author <String>] [-ScriptName <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling]
```

## DESCRIPTION

The **Get-CMScript** cmdlet gets one or more Microsoft System Center Configuration Manager Powershell scripts.
You can get a specific script by specifying the author or the name of the script.

For more information, see [Create and run PowerShell scripts from the Configuration Manager console](https://docs.microsoft.com/sccm/apps/deploy-use/create-deploy-scripts).

## EXAMPLES

### Example 1: Get all scripts

```powershell
PS C:\> Get-CMScript
```

This command gets all scripts that System Center Configuration Manager manages.

### Example 2: Get scripts by using name

```powershell
PS C:\> Get-CMScript -ScriptName "D*"
```

This command gets all scripts that have a name that begins with the letter D.

## PARAMETERS

### -Author

Specifies an author.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

{{Fill Fast Description}}

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

ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -ScriptName

Specifies a script name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_Scripts

IResultObject#SMS_Scripts

## NOTES

## RELATED LINKS

* [Approve-CMScript](Approve-CMScript.md)
* [Deny-CMScript](Deny-CMScript.md)
* [Invoke-CMScript](Invoke-CMScript.md)
* [Remove-CMScript](Remove-CMScript.md)