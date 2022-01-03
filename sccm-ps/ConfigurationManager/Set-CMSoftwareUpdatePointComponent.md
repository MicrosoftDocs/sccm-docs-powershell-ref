---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/15/2021
schema: 2.0.0
title: Set-CMSoftwareUpdatePointComponent
---

# Set-CMSoftwareUpdatePointComponent

## SYNOPSIS

Configure the site component for the software update point.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Set-CMSoftwareUpdatePointComponent [-AddCompany <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-AddLanguageUpdateFile <String[]>] [-AddProduct <String[]>] [-AddProductFamily <String[]>]
 [-AddUpdateClassification <String[]>] [-ContentFileOption <ContentFileOptions>] [-DefaultWsusServer <String>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-EnableManualCertManagement <Boolean>]
 [-EnableSyncFailureAlert <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-FeatureUpdateMaxRuntimeMins <Int32>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] [-NonFeatureUpdateMaxRuntimeMins <Int32>] [-PassThru]
 [-RemoveCompany <String[]>] [-RemoveLanguageSummaryDetail <String[]>] [-RemoveLanguageUpdateFile <String[]>]
 [-RemoveProduct <String[]>] [-RemoveProductFamily <String[]>] [-RemoveUpdateClassification <String[]>]
 [-ReportingEvent <ReportingEventType>] [-Schedule <IResultObject>] [-SiteCode <String>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>] [-WaitMonth <Int32>]
 [-WaitMonthForFeature <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMSoftwareUpdatePointComponent [-AddCompany <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-AddLanguageUpdateFile <String[]>] [-AddProduct <String[]>] [-AddProductFamily <String[]>]
 [-AddUpdateClassification <String[]>] [-ContentFileOption <ContentFileOptions>] [-DefaultWsusServer <String>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-EnableManualCertManagement <Boolean>]
 [-EnableSyncFailureAlert <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-FeatureUpdateMaxRuntimeMins <Int32>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] -Name <String> [-NonFeatureUpdateMaxRuntimeMins <Int32>]
 [-PassThru] [-RemoveCompany <String[]>] [-RemoveLanguageSummaryDetail <String[]>]
 [-RemoveLanguageUpdateFile <String[]>] [-RemoveProduct <String[]>] [-RemoveProductFamily <String[]>]
 [-RemoveUpdateClassification <String[]>] [-ReportingEvent <ReportingEventType>] [-Schedule <IResultObject>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>] [-WaitMonth <Int32>]
 [-WaitMonthForFeature <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMSoftwareUpdatePointComponent [-AddCompany <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-AddLanguageUpdateFile <String[]>] [-AddProduct <String[]>] [-AddProductFamily <String[]>]
 [-AddUpdateClassification <String[]>] [-ContentFileOption <ContentFileOptions>] [-DefaultWsusServer <String>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-EnableManualCertManagement <Boolean>]
 [-EnableSyncFailureAlert <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-FeatureUpdateMaxRuntimeMins <Int32>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] -InputObject <IResultObject>
 [-NonFeatureUpdateMaxRuntimeMins <Int32>] [-PassThru] [-RemoveCompany <String[]>]
 [-RemoveLanguageSummaryDetail <String[]>] [-RemoveLanguageUpdateFile <String[]>] [-RemoveProduct <String[]>]
 [-RemoveProductFamily <String[]>] [-RemoveUpdateClassification <String[]>]
 [-ReportingEvent <ReportingEventType>] [-Schedule <IResultObject>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>] [-WaitMonth <Int32>]
 [-WaitMonthForFeature <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the site component for the software update point. Use it after you add a software update point, for example with the **Add-CMSoftwareUpdatePoint** cmdlet. You can also use this cmdlet to reconfigure an existing software update point.

A software update point component interacts with a Windows Server Update Services (WSUS) server to configure update settings, request synchronization to the upstream update source, and synchronize updates from the WSUS database to the site server database on the central site.

For more information, see [Site components for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-components).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a software update point site component

The first command gets a software update point component object from the **XYZ** site. The command stores the object in the **$supComp** variable.

The second command creates a schedule object to recur every three days.

This example then [splats](/powershell/module/microsoft.powershell.core/about/about_splatting) the cmdlet parameters into the **parameters** variable. It's not required to splat the parameters, it just makes it easier to read the parameters for such a long command line.

The last command modifies common properties of the software update point component.

```powershell
$supComp = Get-CMSoftwareUpdatePointComponent -SiteSystemServerName 'sup1.contoso.com' -SiteCode 'XYZ'

$schedule = New-CMSchedule -RecurCount 3 -RecurInterval Days -Start "2020/1/7 12:00:00"

$addLang = "Dutch"
$removeLang = "English"

$parameters = @{
  InputObject = $supComp
  DefaultWsusServer = 'sup.contoso.com'
  SynchronizeAction = 'SynchronizeFromMicrosoftUpdate'
  ReportingEvent = 'CreateAllWsusReportingEvents'
  RemoveUpdateClassification = "Update Rollups"
  AddUpdateClassification = "Critical Updates"
  Schedule = $schedule
  EnableSyncFailureAlert = $true
  ImmediatelyExpireSupersedence = $true
  AddLanguageUpdateFile = $addLang
  AddLanguageSummaryDetails = $addLang
  RemoveLanguageUpdateFile = $removeLang
  RemoveLanguageSummaryDetails = $removeLang
}

Set-CMSoftwareUpdatePointComponent @parameters
```

### Example 2: Disable software update point synchronization

The following command removes the schedule from the site component, which disables synchronization.

```powershell
Set-CMSoftwareUpdatePointComponent -Name "Contoso-SiteSysSrv.Western.Contoso.com" -Schedule $null
```

## PARAMETERS

### -AddCompany

This parameter is a string array of company names. Use this option to synchronize the entire company's list of **Products**.

To remove an entire company from this list, use the **RemoveCompany** parameter.

For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

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

This parameter is a string array of language names. Use this option to download **Summary details** for the specified languages.

To remove languages from this list, use the **RemoveLanguageSummaryDetail** parameter.

For more information, see [Plan for synchronization settings - Languages](/mem/configmgr/sum/plan-design/plan-for-software-updates#BKMK_UpdateLanguages).

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

This parameter is a string array of language names. Use this option to download the **Software update file** for the specified languages.

To remove languages from this list, use the **RemoveLanguageUpdateFile** parameter.

For more information, see [Plan for synchronization settings - Languages](/mem/configmgr/sum/plan-design/plan-for-software-updates#BKMK_UpdateLanguages).

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

This parameter is a string array of product names. Use this option to synchronize **Products**.

To remove a product from this list, use the **RemoveProduct** parameter.

For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

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

This parameter is a string array of product family names. Use this option to synchronize a product family's list of **Products**.

To remove an entire product family from this list, use the **RemoveProductFamily** parameter.

For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

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

This parameter is a string array of update classifications. Use this option to synchronize specific software update **Classifications**.

To remove a classification from this list, use the **RemoveUpdateClassification** parameter.

For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

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

### -ContentFileOption

Use this parameter to configure how the software update point downloads update files. Express installation files provide smaller download and faster installation on computers because only the necessary files are downloaded and installed. They're larger files and will increase download times for your site servers and distribution points.

- `FullFilesOnly`: Download full files for all approved updates
- `ExpressForWindows10Only`: Download both full files for all approved updates and express installation files for Windows 10 or later

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

Specify the FQDN of the WSUS server.

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

### -EnableCallWsusCleanupWizard

Set this parameter to `$true` to enable WSUS cleanup tasks to run after synchronization. For more information, see [Software updates maintenance](/mem/configmgr/sum/deploy-use/software-updates-maintenance).

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

### -EnableManualCertManagement

Set this parameter to `$true` to manually manage the WSUS signing certificate for third-party updates. This parameter is dependent on the **EnableThirdPartyUpdates** parameter.

For more information, see [Enable third-party updates](/mem/configmgr/sum/deploy-use/third-party-software-updates).

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

Set this parameter to `$true` to enable the component to create an alert when synchronization fails.

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

### -EnableThirdPartyUpdates

Set this parameter to `$true` to **Enable third-party software updates**. You can also use the **EnableManualCertManagement** parameter.

For more information, see [Enable third-party updates](/mem/configmgr/sum/deploy-use/third-party-software-updates).

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

### -FeatureUpdateMaxRuntimeMins

Specify an integer value for the default maximum amount of time a software update installation has to complete. You can override this default for a specific update. This setting only affects newly synchronized updates. This parameter only applies to Windows feature updates.

To configure the maximum run time for Office 365 updates and non-feature updates for Windows, use the **NonFeatureUpdateMaxRuntimeMins** parameter.

For more information, see [Plan for synchronization settings](/mem/configmgr/sum/plan-design/plan-for-software-updates#bkmk_maxruntime).

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

### -ImmediatelyExpireSupersedence

Set this parameter to `$true` to immediately expire a software update when another update supersedes it or after a specified period of time.

If you specify a value of `$False` for this parameter, specify the number of months to wait for expiration by using the **WaitMonth** parameter.

Some updates never expire, for example definition updates.

If you change this setting, the site starts a full synchronization.

To configure this behavior for Windows feature updates, use the **ImmediatelyExpireSupersedenceForFeature** parameter.

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

Set this parameter to `$true` to immediately expire a Windows feature update when another update supersedes it or after a specified period of time.

If you specify a value of `$False` for this parameter, specify the number of months to wait for expiration by using the **WaitMonthForFeature** parameter.

If you change this setting, the site starts a full synchronization.

To configure this behavior for non-feature updates, use the **ImmediatelyExpireSupersedence** parameter.

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

Specify a software update point site component object to configure. To get this object, use the [Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md) cmdlet.

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

Specify the name of a site system server with the software update point role.

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

### -NonFeatureUpdateMaxRuntimeMins

Specify an integer value for the default maximum amount of time a software update installation has to complete. You can override this default for a specific update. This setting only affects newly synchronized updates. This parameter only applies to Office 365 updates and non-feature updates for Windows.

To configure the maximum run time for Windows feature updates, use the **FeatureUpdateMaxRuntimeMins** parameter.

For more information, see [Plan for synchronization settings](/mem/configmgr/sum/plan-design/plan-for-software-updates#bkmk_maxruntime).

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

### -RemoveCompany

This parameter is a string array of company names. Use this option to _not_ synchronize the entire company's list of **Products**.

To add an entire company to this list, use the **AddCompany** parameter.

For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

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

This parameter is a string array of language names. Use this option to _not_ download **Summary details** for the specified languages.

To add languages to this list, use the **AddLanguageSummaryDetail** parameter.

For more information, see [Plan for synchronization settings - Languages](/mem/configmgr/sum/plan-design/plan-for-software-updates#BKMK_UpdateLanguages).

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

This parameter is a string array of language names. Use this option to _not_ download the **Software update file** for the specified languages.

To add languages to this list, use the **AddLanguageUpdateFile** parameter.

For more information, see [Plan for synchronization settings - Languages](/mem/configmgr/sum/plan-design/plan-for-software-updates#BKMK_UpdateLanguages).

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

This parameter is a string array of product names. Use this option to _not_ synchronize **Products**.

To add a product to this list, use the **AddProduct** parameter.

For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

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

This parameter is a string array of product family names. Use this option to _not_ synchronize a product family's list of **Products**.

To add an entire product family to this list, use the **AddProductFamily** parameter.

For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

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

This parameter is a string array of update classifications. Use this option to _not_ synchronize specific software update **Classifications**.

To add a classification to this list, use the **AddUpdateClassification** parameter.

For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

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

Specify whether the Windows Update Agent (WUA) on clients create event messages for WSUS reporting. Configuration Manager doesn't use these events. Don't create these events, unless you require them for other uses.

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

Specify a **Schedule** object to enable synchronization. To disable synchronization, set this parameter to `$null`.

To get a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

Specify the three-character code for the site at which to configure its software update point component.

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

Specify the synchronization source for this software update point.

If you select a value of `SynchronizeFromAnUpstreamDataSourceLocation`, specify the data source location by using the **UpstreamSourceLocation** parameter.

For more information, see [Plan for synchronization settings](/mem/configmgr/sum/plan-design/plan-for-software-updates#BKMK_SyncSource).

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

Specify an upstream data location as a URL. For example, `https://wsusserver.contoso.com:8531`

To use this location, specify `SynchronizeFromAnUpstreamDataSourceLocation` for the **SynchronizeAction** parameter.

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

Set the integer value for the number of months to wait before a software update expires after another update supersedes it.

This parameter depends on the **ImmediatelyExpireSupersedence** parameter.

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

Set the integer value for the number of months to wait before a Windows feature update expires after another update supersedes it.

This parameter depends on the **ImmediatelyExpireSupersedenceForFeature** parameter.

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

### IResultObject#SMS_SCI_Component

## NOTES

For more information on this return object and its properties, see [SMS_SCI_Component server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_component-server-wmi-class).

## RELATED LINKS

[Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md)

[Add-CMSoftwareUpdatePoint](Add-CMSoftwareUpdatePoint.md)

[Site components for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-components)
