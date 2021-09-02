---
description: Sets hierarchy settings in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMHierarchySetting
---

# Set-CMHierarchySetting

## SYNOPSIS
Sets hierarchy settings in Configuration Manager.

## SYNTAX

```
Set-CMHierarchySetting [-AllowPrestage <Boolean>] [-ApprovalMethod <ApprovalMethodType>]
 [-AutoResolveClientConflict <Boolean>] [-AutoUpgradeDays <Int32>] [-EnableAutoClientUpgrade <Boolean>]
 [-EnableExclusionCollection <Boolean>] [-EnablePreProduction <Boolean>] [-EnablePrereleaseFeature]
 [-ExcludeServer <Boolean>] [-ExclusionCollection <IResultObject>] [-ExclusionCollectionId <String>]
 [-ExclusionCollectionName <String>] [-FallbackSiteCode <String>] [-Force] [-PassThru]
 [-PreferBoundaryGroupManagementPoint <Boolean>] [-TargetCollection <IResultObject>]
 [-TargetCollectionId <String>] [-TargetCollectionName <String>] [-TelemetryLevel <TelemetryLevelType>]
 [-UnlimitTargetCollectionMember] [-UseFallbackSite <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMHierarchySetting** cmdlet sets hierarchy settings in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify the hierarchy setting
```
PS XYZ:\> Set-CMHierarchySetting -AllowPrestage -ApprovalMethod AutomaticallyApproveAllComputers
```

This command uses the **Set-CMHierarchySetting** cmdlet to modify the hierarchy setting.
The command specifies the value AutomaticallyApproveAllComputers for the *ApprovalMethod* parameter, and also specifies the *AllowPrestage* parameter.

## PARAMETERS

### -AllowPrestage
Indicates whether to allow prestaging.

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

### -ApprovalMethod
Specifies an approval method.
Valid values are:

- AutomaticallyApproveAllComputers
- AutomaticallyApproveComputersInTrustedDomains
- ManuallyApproveEachComputer

```yaml
Type: ApprovalMethodType
Parameter Sets: (All)
Aliases:
Accepted values: AutomaticallyApproveComputersInTrustedDomains, ManuallyApproveEachComputer, AutomaticallyApproveAllComputers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoResolveClientConflict
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AutomaticallyResolveConfictingRecord, AutomaticallyResolveConflictingRecord

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoUpgradeDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: AutomaticallyUpgradeDays

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

### -EnableAutoClientUpgrade
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableProgram

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableExclusionCollection
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

### -EnablePreProduction
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

### -EnablePrereleaseFeature
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnablePrereleaseFeatures

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeServer
Indicates whether the cmdlet excludes the server.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ExcludeServers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExclusionCollection
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExclusionCollectionId
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

### -ExclusionCollectionName
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

### -FallbackSiteCode
Specifies the site code for a fallback site.

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

### -PreferBoundaryGroupManagementPoint
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: PreferBoundaryGroupManagementPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetCollection
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: PreProductionCollection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetCollectionId
```yaml
Type: String
Parameter Sets: (All)
Aliases: PreProductionCollectionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetCollectionName
```yaml
Type: String
Parameter Sets: (All)
Aliases: PreProductionCollectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TelemetryLevel
{{ Fill TelemetryLevel Description }}

```yaml
Type: TelemetryLevelType
Parameter Sets: (All)
Aliases: DiagnosticLevel
Accepted values: Basic, Enhanced, Full

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnlimitTargetCollectionMember
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: UnlimitPreProductionCollectionMemberCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseFallbackSite
Indicates whether to use a fallback site.

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

### None
## OUTPUTS

### IResultObject#SMS_SCI_SiteDefinition
### IResultObject[]#SMS_SCI_SiteDefinition
## NOTES

## RELATED LINKS
