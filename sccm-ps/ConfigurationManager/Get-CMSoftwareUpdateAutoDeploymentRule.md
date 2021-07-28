---
description: Get an automatic deployment rule for software updates.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
schema: 2.0.0
title: Get-CMSoftwareUpdateAutoDeploymentRule
---

# Get-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS

Get an automatic deployment rule for software updates.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateAutoDeploymentRule [-Fast] [-IsServicingPlan <Boolean>] [[-Name] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareUpdateAutoDeploymentRule [-Fast] [-Id] <Int32[]> [-IsServicingPlan <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateAutoDeploymentRule** cmdlet gets the specified automatic deployment rules for software updates.

Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, Configuration Manager adds updates that qualify for the rule to a software update group.
The Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

You can specify rules by ID or by name.
You can use this cmdlet to get deployment rules for automatic software updates to use with other cmdlets. For example, the [Invoke-CMSoftwareUpdateAutoDeploymentRule](Invoke-CMSoftwareUpdateAutoDeploymentRule.md) or [Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md) cmdlets.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an ADR by name

This command gets an automatic deployment rule named **Weekly Driver Updates**.

```powershell
Get-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
```

### Example 2: Get an ADR by ID

This command gets an automatic deployment rule that has the ID **33**.

```powershell
Get-CMSoftwareUpdateAutoDeploymentRule -Id "33"
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

### -Id

Specify an array of automatic deployment rule IDs to configure. This value is the **AutoDeploymentID** property of the ADR object.

```yaml
Type: Int32[]
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsServicingPlan
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies a name of a rule for automatic deployment of software updates.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_AutoDeployment
### IResultObject#SMS_AutoDeployment
## NOTES

The SMS_AutoDeployment output object displays many of the ADR settings as the stored XML. Parse this XML for specific settings.

For example:

- The **-Language** parameter is stored in the **UpdateRuleXML** property as `<MatchRules><string>'Locale:10'</string></MatchRules>`
- The **-LanguageSelection** parameter is stored in the **ContentTemplate** property as `<ContentLocales><Locale>Locale:10</Locale></ContentLocales>`

These locale codes are stored as the decimal equivalent of the Windows language ID. For example, `9` is `0x0009` for English, and `10` is `0x000A` for Spanish. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

## RELATED LINKS

[Disable-CMSoftwareUpdateAutoDeploymentRule](Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Enable-CMSoftwareUpdateAutoDeploymentRule](Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](Invoke-CMSoftwareUpdateAutoDeploymentRule.md)

[New-CMSoftwareUpdateAutoDeploymentRule](New-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md)

[Set-CMSoftwareUpdateAutoDeploymentRule](Set-CMSoftwareUpdateAutoDeploymentRule.md)
