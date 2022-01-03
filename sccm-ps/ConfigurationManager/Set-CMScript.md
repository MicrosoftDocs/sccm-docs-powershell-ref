---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
online version:
schema: 2.0.0
---

# Set-CMScript

## SYNOPSIS

Edit a PowerShell script in Configuration Manager.

## SYNTAX

### ByScript
```
Set-CMScript -InputObject <IResultObject> [-ScriptFile <String>] [-ScriptText <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMScript [-ScriptFile <String>] -ScriptGuid <String> [-ScriptText <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMScript [-ScriptFile <String>] -ScriptName <String> [-ScriptText <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to edit an existing PowerShell script in Configuration Manager. These scripts are integrated and managed in Configuration Manager.

For more information, see [Create and run PowerShell scripts from the Configuration Manager console](/mem/configmgr/apps/deploy-use/create-deploy-scripts).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the script from a new imported file

This example gets a script by name, and then imports a new file as the script source.

```powershell
Get-CMScript -ScriptName "myScript" -Fast | Set-CMScript -ScriptFile "\\server\share\script.ps1"
```

## PARAMETERS

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

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

### -InputObject

Specify a script object to modify. To get this object, use the [Get-CMScript](Get-CMScript.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByScript
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ScriptFile

Specify the network path to a PowerShell script to import and use for this script.

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

### -ScriptGuid

Specify the GUID for the script to modify.

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

Specify the name of the script to modify.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ScriptText

Specify the text to use for this script.

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Approve-CMScript](Approve-CMScript.md)
[Deny-CMScript](Deny-CMScript.md)
[Get-CMScript](Get-CMScript.md)
[Invoke-CMScript](Invoke-CMScript.md)
[New-CMScript](New-CMScript.md)
[Remove-CMScript](Remove-CMScript.md)

[Create and run PowerShell scripts from the Configuration Manager console](/mem/configmgr/apps/deploy-use/create-deploy-scripts)
