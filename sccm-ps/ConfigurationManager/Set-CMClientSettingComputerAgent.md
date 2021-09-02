---
description: Sets a client setting computer agent.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMClientSettingComputerAgent
---

# Set-CMClientSettingComputerAgent

## SYNOPSIS
Sets a client setting computer agent.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingComputerAgent [-AddPortalToTrustedSiteList <Boolean>]
 [-AllowPortalToHaveElevatedTrust <Boolean>] [-BrandingTitle <String>] [-DisableDeadlineRandom <Boolean>]
 [-DisplayNewProgramNotification <Boolean>] [-EnableHealthAttestation <Boolean>]
 [-EnableThirdPartyOrchestration <EnableThirdPartyOrchestrationType>] [-FinalReminderMins <Int32>]
 [-HealthAttestationUrl <String>] [-InitialReminderHr <Int32>] [-InstallRestriction <InstallRestrictionType>]
 [-InterimReminderHr <Int32>] [-PortalUrl <String>]
 [-PowerShellExecutionPolicy <PowerShellExecutionPolicyType>]
 [-SelectWebsitePoint <ApplicationCatalogWebsitePointType>] [-SuspendBitLocker <SuspendBitLockerType>]
 [-UseNewSoftwareCenter <Boolean>] [-UseOnPremisesHealthAttestation <Boolean>]
 [-WebsitePointServerName <String>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingComputerAgent [-AddPortalToTrustedSiteList <Boolean>]
 [-AllowPortalToHaveElevatedTrust <Boolean>] [-BrandingTitle <String>] [-DisableDeadlineRandom <Boolean>]
 [-DisplayNewProgramNotification <Boolean>] [-EnableHealthAttestation <Boolean>]
 [-EnableThirdPartyOrchestration <EnableThirdPartyOrchestrationType>] [-FinalReminderMins <Int32>]
 [-HealthAttestationUrl <String>] [-InitialReminderHr <Int32>] [-InstallRestriction <InstallRestrictionType>]
 [-InterimReminderHr <Int32>] [-PortalUrl <String>]
 [-PowerShellExecutionPolicy <PowerShellExecutionPolicyType>]
 [-SelectWebsitePoint <ApplicationCatalogWebsitePointType>] [-SuspendBitLocker <SuspendBitLockerType>]
 [-UseNewSoftwareCenter <Boolean>] [-UseOnPremisesHealthAttestation <Boolean>]
 [-WebsitePointServerName <String>] [-DefaultSetting] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingComputerAgent [-AddPortalToTrustedSiteList <Boolean>]
 [-AllowPortalToHaveElevatedTrust <Boolean>] [-BrandingTitle <String>] [-DisableDeadlineRandom <Boolean>]
 [-DisplayNewProgramNotification <Boolean>] [-EnableHealthAttestation <Boolean>]
 [-EnableThirdPartyOrchestration <EnableThirdPartyOrchestrationType>] [-FinalReminderMins <Int32>]
 [-HealthAttestationUrl <String>] [-InitialReminderHr <Int32>] [-InstallRestriction <InstallRestrictionType>]
 [-InterimReminderHr <Int32>] [-PortalUrl <String>]
 [-PowerShellExecutionPolicy <PowerShellExecutionPolicyType>]
 [-SelectWebsitePoint <ApplicationCatalogWebsitePointType>] [-SuspendBitLocker <SuspendBitLockerType>]
 [-UseNewSoftwareCenter <Boolean>] [-UseOnPremisesHealthAttestation <Boolean>]
 [-WebsitePointServerName <String>] -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -AddPortalToTrustedSiteList
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

### -AllowPortalToHaveElevatedTrust
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

### -BrandingTitle
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

### -DefaultSetting
```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableDeadlineRandom
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DisableDeadlineRandomization

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

### -DisplayNewProgramNotification
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

### -EnableHealthAttestation
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableHealthAttestationService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableThirdPartyOrchestration
```yaml
Type: EnableThirdPartyOrchestrationType
Parameter Sets: (All)
Aliases:
Accepted values: No, Yes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FinalReminderMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: FinalReminderMinutesInterval, FinalReminderMinutes

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

### -HealthAttestationUrl
```yaml
Type: String
Parameter Sets: (All)
Aliases: OnPremisesHealthAttestationServiceUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitialReminderHr
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: InitialReminderHoursInterval, InitialReminderHours

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallRestriction
```yaml
Type: InstallRestrictionType
Parameter Sets: (All)
Aliases:
Accepted values: AllUsers, OnlyAdministrators, OnlyAdministratorsAndPrimaryUsers, NoUsers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InterimReminderHr
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: InterimReminderHoursInterval, InterimReminderHours

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -PortalUrl
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

### -PowerShellExecutionPolicy
```yaml
Type: PowerShellExecutionPolicyType
Parameter Sets: (All)
Aliases:
Accepted values: AllSigned, Bypass, Restricted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelectWebsitePoint

Don't use this parameter. The application catalog is no longer supported.

```yaml
Type: ApplicationCatalogWebsitePointType
Parameter Sets: (All)
Aliases: SelectApplicationCatalogWebsitePoint
Accepted values: Fqdn, AutoDetect, NetBios

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuspendBitLocker
```yaml
Type: SuspendBitLockerType
Parameter Sets: (All)
Aliases:
Accepted values: Never, Always

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseNewSoftwareCenter
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

### -UseOnPremisesHealthAttestation
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UseOnPremisesHealthAttestationService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebsitePointServerName
```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationCatalogWebsitePointServerName

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
