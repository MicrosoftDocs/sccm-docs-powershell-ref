---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 8B1C6216-49C0-4D0E-A77B-CF7C29E706C9
online version: https://go.microsoft.com/fwlink/?linkid=834237
schema: 2.0.0
---

# Remove-CMStatusFilterRule

## SYNOPSIS
Removes a specified Configuration Manager filter rule for status messages.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMStatusFilterRule -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySiteCodeMandatory
```
Remove-CMStatusFilterRule [-SiteCode <String>] -Name <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMStatusFilterRule** cmdlet removes a specified Microsoft System Center Configuration Manager filter rule for status messages.

Status filter rules specify how System Center Configuration Manager responds to status messages.
Each filter rule contains criteria and actions for status messages.
You configure status filter rules for each site, not across all sites.

Use the rule name and site code to specify a rule to remove.
This cmdlet deletes rules permanently.
You can use the [Disable-CMStatusFilterRule](Disable-CMStatusFilterRule.md) cmdlet to suspend a rule.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove a rule
```
PS XYZ:\> Remove-CMStatusFilterRule -Name "Status change to critical" -SiteCode "CM1" -Force
```

This command removes a status filter rule that has the specified name in a site that has the site code CM1.
The command includes the *Force* parameter, so the cmdlet does not prompt you for confirmation.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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

### -Force
Forces the command to run without asking for user confirmation.

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

### -InputObject
Specifies a status filter rule object to remove.
To obtain a status filter rule object, use the [Get-CMStatusFilterRule](Get-CMStatusFilterRule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a rule.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for the Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMStatusFilterRule](Disable-CMStatusFilterRule.md)

[Enable-CMStatusFilterRule](Enable-CMStatusFilterRule.md)

[Get-CMStatusFilterRule](Get-CMStatusFilterRule.md)

[New-CMStatusFilterRule](New-CMStatusFilterRule.md)

[Set-CMStatusFilterRule](Set-CMStatusFilterRule.md)


