---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Approve-CMScript
---

# Approve-CMScript

## SYNOPSIS

Approve a PowerShell script in Configuration Manager.

## SYNTAX

### ByScript
```
Approve-CMScript [-Comment <String>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByScriptId
```
Approve-CMScript [-Comment <String>] -ScriptGuid <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to approve a Powershell script in Configuration Manager. These scripts are integrated and managed in Configuration Manager. You can't run a script on devices until it's approved. After you approve a script, to run it use the [Invoke-CMScript](Invoke-CMScript.md) cmdlet.

By default, you can't approve scripts that you author.

For more information, see [Create and run PowerShell scripts from the Configuration Manager console](/mem/configmgr/apps/deploy-use/create-deploy-scripts).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Approve a script by using the script ID

This command approves a script that has the ID `DF8E7546-FD66-4A3D-A129-53AF5AA54F80`.

```powershell
Approve-CMScript -ScriptGuid "DF8E7546-FD66-4A3D-A129-53AF5AA54F80"
```

### Example 2: Approve a script by using script object variable

The first command gets a script object with ID `DF8E7546-FD66-4A3D-A129-53AF5AA54F80`. It then stores the object in the **$ScriptObj** variable.

The second command approves the script stored in the variable.

```powershell
$ScriptObj = Get-CMScript -Id "DF8E7546-FD66-4A3D-A129-53AF5AA54F80"
Approve-CMScript -InputObject $ScriptObj
```

### Example 3: Bulk approve all unapproved scripts

This command gets all scripts in Configuration Manager that aren't approved. It then loops through each script in the **scripts** array. If the current user is not the author of the script, it approves it.

```powershell
$scripts = Get-CMScript -Fast | Where-Object { -not $_.ApprovalState }

$me = $env:userdomain + "\" + $env:username
foreach ( $script in $scripts ) {
  if ( $script.Author -ne $me ) {
    Approve-CMScript -InputObject $script
  }
}
```

## PARAMETERS

### -Comment

Specifies a comment about the approval of the script.

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

### -InputObject

Specify a script object to approve. To get this object, use the [Get-CMScript](Get-CMScript.md) cmdlet.

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

### -ScriptGuid

Specify the ID of the script to approve. The format is a standard GUID.

```yaml
Type: String
Parameter Sets: ByScriptId
Aliases:

Required: True
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

[Deny-CMScript](Deny-CMScript.md)
[Get-CMScript](Get-CMScript.md)
[Invoke-CMScript](Invoke-CMScript.md)
[New-CMScript](New-CMScript.md)
[Remove-CMScript](Remove-CMScript.md)
[Set-CMScript](Set-CMScript.md)

[Create and run PowerShell scripts from the Configuration Manager console](/mem/configmgr/apps/deploy-use/create-deploy-scripts)
