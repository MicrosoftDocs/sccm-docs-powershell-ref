---
author: aczechowski
description: Modifies a software update point.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMSoftwareUpdatePointComponent
titleSuffix: Configuration Manager
---

# Set-CMSoftwareUpdatePointComponent

## SYNOPSIS
Modifies a software update point.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Set-CMSoftwareUpdatePointComponent [-SiteCode <String>] [-DefaultWsusServer <String>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>]
 [-ReportingEvent <ReportingEventType>] [-RemoveUpdateClassification <String[]>]
 [-AddUpdateClassification <String[]>] [-AddCompany <String[]>] [-RemoveCompany <String[]>]
 [-AddProductFamily <String[]>] [-RemoveProductFamily <String[]>] [-AddProduct <String[]>]
 [-RemoveProduct <String[]>] [-EnableSynchronization <Boolean>] [-Schedule <IResultObject>]
 [-EnableSyncFailureAlert <Boolean>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] [-EnableCallWsusCleanupWizard <Boolean>]
 [-WaitMonth <Int32>] [-WaitMonthForFeature <Int32>] [-AddLanguageUpdateFile <String[]>]
 [-RemoveLanguageUpdateFile <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-RemoveLanguageSummaryDetail <String[]>] [-ContentFileOption <ContentFileOptions>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMSoftwareUpdatePointComponent -Name <String> [-DefaultWsusServer <String>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>]
 [-ReportingEvent <ReportingEventType>] [-RemoveUpdateClassification <String[]>]
 [-AddUpdateClassification <String[]>] [-AddCompany <String[]>] [-RemoveCompany <String[]>]
 [-AddProductFamily <String[]>] [-RemoveProductFamily <String[]>] [-AddProduct <String[]>]
 [-RemoveProduct <String[]>] [-EnableSynchronization <Boolean>] [-Schedule <IResultObject>]
 [-EnableSyncFailureAlert <Boolean>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] [-EnableCallWsusCleanupWizard <Boolean>]
 [-WaitMonth <Int32>] [-WaitMonthForFeature <Int32>] [-AddLanguageUpdateFile <String[]>]
 [-RemoveLanguageUpdateFile <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-RemoveLanguageSummaryDetail <String[]>] [-ContentFileOption <ContentFileOptions>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMSoftwareUpdatePointComponent [-DefaultWsusServer <String>] [-SynchronizeAction <SynchronizeActionType>]
 [-UpstreamSourceLocation <String>] [-ReportingEvent <ReportingEventType>]
 [-RemoveUpdateClassification <String[]>] [-AddUpdateClassification <String[]>] [-AddCompany <String[]>]
 [-RemoveCompany <String[]>] [-AddProductFamily <String[]>] [-RemoveProductFamily <String[]>]
 [-AddProduct <String[]>] [-RemoveProduct <String[]>] [-EnableSynchronization <Boolean>]
 [-Schedule <IResultObject>] [-EnableSyncFailureAlert <Boolean>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] [-EnableCallWsusCleanupWizard <Boolean>]
 [-WaitMonth <Int32>] [-WaitMonthForFeature <Int32>] [-AddLanguageUpdateFile <String[]>]
 [-RemoveLanguageUpdateFile <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-RemoveLanguageSummaryDetail <String[]>] [-ContentFileOption <ContentFileOptions>]
 -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdatePointComponent** cmdlet modifies a software update point.
A software update point component interacts with a Windows Server Update Services (WSUS) server to configure update settings, request synchronization to the upstream update source, and synchronize updates from the WSUS database to the site server database on the central site.

You can specify a software update point to modify by name, by site code, or by using the [Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md) cmdlet.

## EXAMPLES

### Example 1: Modify a software update point
```
PS XYZ:\> $CIObj = Get-CMSoftwareUpdatePointComponent -SiteSystemServerName "Contoso-SiteSysSrv.Western.Contoso.com"
PS XYZ:\> Set-CMSoftwareUpdatePointComponent -InputObject $CIObj
```

The first command retrieves a software update point component object on the server named Contoso-SiteSysSrv.TSQA.Contoso.com.
The command stores the object in the **$CIObj** variable.

The second command modifies the software update point component in **$CIObj**.

## PARAMETERS

### -AddCompany
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddCompanies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguageSummaryDetail
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddLanguageSummaryDetails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguageUpdateFile
Specifies an array of languages, as strings.
The cmdlet adds these languages to the languages supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddProduct
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddProducts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddProductFamily
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddProductFamilies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddUpdateClassification
Specifies an array of software update classifications, as strings.
This cmdlet adds these classifications to the classifications supported for software updates at this site.

```yaml
Type: String[]
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

### -ContentFileOption
```yaml
Type: ContentFileOptions
Parameter Sets: (All)
Aliases:
Accepted values: FullFilesOnly, ExpressForWindows10Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultWsusServer
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

### -EnableCallWsusCleanupWizard
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

### -EnableSyncFailureAlert
Indicates whether Configuration Manager creates an alert when synchronization fails on a site.

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

### -EnableSynchronization
Indicates whether this site automatically synchronizes updates according to a schedule.
Specify a schedule by using the *Schedule* parameter.

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

### -ImmediatelyExpireSupersedence
Indicates whether a software update expires immediately after another update supersedes it or after a specified period of time.
If you specify a value of $False for this parameter, specify the number of months to wait for expiration by using the *WaitMonth* parameter.

System Center 2016 Endpoint Protection definition updates and software updates that Service Packs supersede never expire.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ImmediatelyExpireSupersedenceForNonFeature

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImmediatelyExpireSupersedenceForFeature
{{ Fill ImmediatelyExpireSupersedenceForFeature Description }}

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

### -InputObject
Specifies a software update point component object.
To obtain a software update point component object, use the [Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Site, SiteComponent

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a site system server in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
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

### -RemoveCompany
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveCompanies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLanguageSummaryDetail
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveLanguageSummaryDetails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLanguageUpdateFile
Specifies an array of languages, as strings.
The cmdlet removes these languages from the languages supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveProduct
Specifies an array of products, as strings.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveProducts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveProductFamily
Specifies an array of product families, as strings.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveProductFamilies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveUpdateClassification
Specifies an array of software update classifications, as strings.
This cmdlet removes these classifications from the classifications supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportingEvent
Specifies whether to create event messages for WSUS reporting for status reporting events or for all reporting events.
The acceptable values for this parameter are:

- CreateAllWsusReportingEvents
- CreateOnlyWsusStatusReportingEvents
- DoNotCreateWsusReportingEvents

```yaml
Type: ReportingEventType
Parameter Sets: (All)
Aliases:
Accepted values: DoNotCreateWsusReportingEvents, CreateOnlyWsusStatusReportingEvents, CreateAllWsusReportingEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a **Schedule** object.
Configuration Manager can synchronize updates according this schedule if you specify a value of $True for the *EnableSynchronization* parameter.
To obtain a **Schedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -SiteCode
Specifies a site code in Configuration Manager.

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

### -SynchronizeAction
Specifies a source for synchronization for this software update point.
The acceptable values for this parameter are:

- DoNotSynchronizeFromMicrosoftUpdateOrUpstreamDataSource
- SynchronizeFromAnUpstreamDataSourceLocation
- SynchronizeFromMicrosoftUpdate

If you select a value of SynchronizeFromAnUpstreamDataSourceLocation, specify the data source location by using the **UpstreamSourceLocation** parameter.

```yaml
Type: SynchronizeActionType
Parameter Sets: (All)
Aliases:
Accepted values: SynchronizeFromMicrosoftUpdate, SynchronizeFromAnUpstreamDataSourceLocation, DoNotSynchronizeFromMicrosoftUpdateOrUpstreamDataSource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpstreamSourceLocation
Specifies an upstream data location as a URL.
To use this location, specify a value of SynchronizeFromAnUpstreamDataSourceLocation for the *SynchronizeAction* parameter.

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

### -WaitMonth
Specifies how long, in months, to wait before a software update expires after another update supersedes it.
Specify a value of $True for the *ImmediatelyExpireSupersedence* parameter for software updates to expire immediately.

Endpoint Protection definition updates and software updates that Service Packs supersede never expire.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: WaitMonthForNonFeature

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitMonthForFeature
{{ Fill WaitMonthForFeature Description }}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md)

[New-CMSchedule](New-CMSchedule.md)

[Set-CMCollectionMembershipEvaluationComponent](Set-CMCollectionMembershipEvaluationComponent.md)

[Set-CMEmailNotificationComponent](Set-CMEmailNotificationComponent.md)

[Set-CMManagementPointComponent](Set-CMManagementPointComponent.md)

[Set-CMStatusReportingComponent](Set-CMStatusReportingComponent.md)

[Set-CMSystemHealthValidatorPointComponent](Set-CMSystemHealthValidatorPointComponent.md)
