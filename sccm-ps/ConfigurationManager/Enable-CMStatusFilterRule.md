---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: D0E060EA-EF7D-47EC-86E9-2C4E027FA54B
online version: https://go.microsoft.com/fwlink/?linkid=833999
schema: 2.0.0
---

# Enable-CMStatusFilterRule

## SYNOPSIS
Enables a Configuration Manager filter rule for status messages.

## SYNTAX

### SearchByName (Default)
```
Enable-CMStatusFilterRule [-SiteCode <String>] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValue
```
Enable-CMStatusFilterRule -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-CMStatusFilterRule** cmdlet enables a specified Microsoft System Center Configuration Manager filter rule for status messages.

Status filter rules specify how System Center Configuration Manager responds to status messages.
Each filter rule contains criteria and actions for status messages.
You configure status filter rules for each site, not across all sites.

Use the rule name and site code to specify a rule to enable.
You can use the [Disable-CMStatusFilterRule](Disable-CMStatusFilterRule.md) cmdlet to disable a rule.
To remove a rule permanently, use the [Remove-CMStatusFilterRule](Remove-CMStatusFilterRule.md) cmdlet.

## EXAMPLES

### Example 1: Enable a status filter rule
```
PS C:\>Enable-CMStatusFilterRule -Name "Status change to critical" -SiteCode "CM1"
```

This command enables a status filter rule that has the specified name in a site that has the site code CM1.

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
Specifies a status filter rule object to enable.
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
Parameter Sets: SearchByName
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
Parameter Sets: SearchByName
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

[Get-CMStatusFilterRule](Get-CMStatusFilterRule.md)

[New-CMStatusFilterRule](New-CMStatusFilterRule.md)

[Remove-CMStatusFilterRule](Remove-CMStatusFilterRule.md)

[Set-CMStatusFilterRule](Set-CMStatusFilterRule.md)


