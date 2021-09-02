---
description: Changes properties and security scopes for Configuration Manager software metering rules.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSoftwareMeteringRule
---

# Set-CMSoftwareMeteringRule

## SYNOPSIS
Changes properties and security scopes for Configuration Manager software metering rules.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMSoftwareMeteringRule [-Comment <String>] [-FileName <String>] [-FileVersion <String>]
 -InputObject <IResultObject> [-LanguageId <Int32>] [-NewProductName <String>] [-OriginalFileName <String>]
 [-PassThru] [-Path <String>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSoftwareMeteringRule [-Comment <String>] [-FileName <String>] [-FileVersion <String>]
 [-LanguageId <Int32>] [-NewProductName <String>] [-OriginalFileName <String>] [-PassThru] [-Path <String>]
 -ProductName <String> [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMSoftwareMeteringRule [-Comment <String>] [-FileName <String>] [-FileVersion <String>] -Id <String>
 [-LanguageId <Int32>] [-NewProductName <String>] [-OriginalFileName <String>] [-PassThru] [-Path <String>]
 [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareMeteringRule** cmdlet changes properties for software metering rules in Configuration Manager and adds or removes security scopes for software metering rules.
Every rule must have at least one security scope.

Software metering monitors and collects software usage data from Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

To change rule properties, you can specify rules to change by ID or by product name, or use the [Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md) cmdlet.
Likewise, you can change security scope for rules for specified ID, product name, or by using **Get-CMSoftwareMeteringRule**.

For more information about software metering in Configuration Manager, see [Introduction to Software Metering in Configuration Manager](/mem/configmgr/apps/deploy-use/monitor-app-usage-with-software-metering).
For more information about security scopes, see [Planning for Security in Configuration Manager](/mem/configmgr/core/plan-design/security/plan-for-security).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change locale for rules for a product
```
PS XYZ:\> Set-CMSoftwareMeteringRule -ProductName "Accounting Package" -LanguageID 1036
```

This command sets the locale ID for rules that include the product name Accounting Package.

### Example 2: Add a security scope to rules for a product
```
PS XYZ:\> Set-CMSoftwareMeteringRule -ProductName "Accounting Package" -SecurityScopeAction AddMembership -SecurityScopeName "Scope05"
```

This command adds the security scope called Scope05 to rules for the product name Accounting Package.

## PARAMETERS

### -Comment
Specifies a comment for a software metering rule.

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

### -FileName
Specifies the filename of the software that a rule meters.

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

### -FileVersion
Specifies a version of the software that a rule meters.

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
Specifies an array of IDs for software metering rules.

```yaml
Type: String
Parameter Sets: SetById
Aliases: RuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software metering rule object.
To obtain a software metering rule object, use the [Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LanguageId
Specifies a LocaleID of the software that a rule meters.
For more information and a list of locale identifiers, see [Appendix A: Product Behavior](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewProductName
Specifies a new name for the software that a rule meters.

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

### -OriginalFileName
Specifies an original file name of the software that a rule meters.
This parameter can differ from the *FileName* parameter if a user changed the name.

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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -Path
Specifies a file path of the software that a rule meters.

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

### -ProductName
Specifies a name for a product that a rule meters.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code of a Configuration Manager site.

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
Default value: False
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
Default value: False
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

[Disable-CMSoftwareMeteringRule](Disable-CMSoftwareMeteringRule.md)

[Enable-CMSoftwareMeteringRule](Enable-CMSoftwareMeteringRule.md)

[Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md)

[New-CMSoftwareMeteringRule](New-CMSoftwareMeteringRule.md)

[Remove-CMSoftwareMeteringRule](Remove-CMSoftwareMeteringRule.md)
