---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
ms.assetid: 9303F7BE-B1E8-482F-8270-1C77249566BF
online version: https://go.microsoft.com/fwlink/?linkid=834054
schema: 2.0.0
---

# Set-CMSoftwareMeteringRule

## SYNOPSIS
Changes properties and security scopes for Configuration Manager software metering rules.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMSoftwareMeteringRule -InputObject <IResultObject> [-FileName <String>] [-FileVersion <String>]
 [-OriginalFileName <String>] [-Comment <String>] [-LanguageId <Int32>] [-SiteCode <String>]
 [-NewProductName <String>] [-Path <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMSoftwareMeteringRule -Id <String> [-FileName <String>] [-FileVersion <String>]
 [-OriginalFileName <String>] [-Comment <String>] [-LanguageId <Int32>] [-SiteCode <String>]
 [-NewProductName <String>] [-Path <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSoftwareMeteringRule [-FileName <String>] [-FileVersion <String>] [-OriginalFileName <String>]
 [-Comment <String>] [-LanguageId <Int32>] [-SiteCode <String>] -ProductName <String>
 [-NewProductName <String>] [-Path <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareMeteringRule** cmdlet changes properties for software metering rules in Microsoft System Center Configuration Manager and adds or removes security scopes for software metering rules.
Every rule must have at least one security scope.

Software metering monitors and collects software usage data from System Center Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

To change rule properties, you can specify rules to change by ID or by product name, or use the [Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md) cmdlet.
Likewise, you can change security scope for rules for specified ID, product name, or by using **Get-CMSoftwareMeteringRule**.

For more information about software metering in System Center Configuration Manager, see [Introduction to Software Metering in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268432) on TechNet.
For more information about security scopes, see [Planning for Security in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268426).

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


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
For more information and a list of locale identifiers, see the Locale IDs Assigned by Microsoft topic at [http://go.microsoft.com/fwlink/?LinkId=262651](http://go.microsoft.com/fwlink/?LinkId=262651).

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
Returns the current working object.
By default, this cmdlet does not generate any output.

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

[Disable-CMSoftwareMeteringRule](Disable-CMSoftwareMeteringRule.md)

[Enable-CMSoftwareMeteringRule](Enable-CMSoftwareMeteringRule.md)

[Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md)

[New-CMSoftwareMeteringRule](New-CMSoftwareMeteringRule.md)

[Remove-CMSoftwareMeteringRule](Remove-CMSoftwareMeteringRule.md)
