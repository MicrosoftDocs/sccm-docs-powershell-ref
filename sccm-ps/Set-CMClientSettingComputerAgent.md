---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-CMClientSettingComputerAgent

## SYNOPSIS
Sets a client setting computer agent

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingComputerAgent [-InitialReminderHr <Int32>] [-InterimReminderHr <Int32>]
 [-FinalReminderMins <Int32>] [-PortalUrl <String>] [-AddPortalToTrustedSiteList <Boolean>]
 [-AllowPortalToHaveElevatedTrust <Boolean>] [-SelectWebsitePoint <ApplicationCatalogWebsitePointType>]
 [-WebsitePointServerName <String>] [-BrandingTitle <String>] [-UseNewSoftwareCenter <Boolean>]
 [-InstallRestriction <InstallRestrictionType>] [-SuspendBitLocker <SuspendBitLockerType>]
 [-EnableThirdPartyOrchestration <EnableThirdPartyOrchestrationType>]
 [-PowerShellExecutionPolicy <PowerShellExecutionPolicyType>] [-DisplayNewProgramNotification <Boolean>]
 [-DisableDeadlineRandom <Boolean>] [-EnableHealthAttestation <Boolean>]
 [-UseOnPremisesHealthAttestation <Boolean>] [-HealthAttestationUrl <String>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingComputerAgent [-InitialReminderHr <Int32>] [-InterimReminderHr <Int32>]
 [-FinalReminderMins <Int32>] [-PortalUrl <String>] [-AddPortalToTrustedSiteList <Boolean>]
 [-AllowPortalToHaveElevatedTrust <Boolean>] [-SelectWebsitePoint <ApplicationCatalogWebsitePointType>]
 [-WebsitePointServerName <String>] [-BrandingTitle <String>] [-UseNewSoftwareCenter <Boolean>]
 [-InstallRestriction <InstallRestrictionType>] [-SuspendBitLocker <SuspendBitLockerType>]
 [-EnableThirdPartyOrchestration <EnableThirdPartyOrchestrationType>]
 [-PowerShellExecutionPolicy <PowerShellExecutionPolicyType>] [-DisplayNewProgramNotification <Boolean>]
 [-DisableDeadlineRandom <Boolean>] [-EnableHealthAttestation <Boolean>]
 [-UseOnPremisesHealthAttestation <Boolean>] [-HealthAttestationUrl <String>] [-DefaultSetting] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingComputerAgent [-InitialReminderHr <Int32>] [-InterimReminderHr <Int32>]
 [-FinalReminderMins <Int32>] [-PortalUrl <String>] [-AddPortalToTrustedSiteList <Boolean>]
 [-AllowPortalToHaveElevatedTrust <Boolean>] [-SelectWebsitePoint <ApplicationCatalogWebsitePointType>]
 [-WebsitePointServerName <String>] [-BrandingTitle <String>] [-UseNewSoftwareCenter <Boolean>]
 [-InstallRestriction <InstallRestrictionType>] [-SuspendBitLocker <SuspendBitLockerType>]
 [-EnableThirdPartyOrchestration <EnableThirdPartyOrchestrationType>]
 [-PowerShellExecutionPolicy <PowerShellExecutionPolicyType>] [-DisplayNewProgramNotification <Boolean>]
 [-DisableDeadlineRandom <Boolean>] [-EnableHealthAttestation <Boolean>]
 [-UseOnPremisesHealthAttestation <Boolean>] [-HealthAttestationUrl <String>] -InputObject <IResultObject>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddPortalToTrustedSiteList
{{Fill AddPortalToTrustedSiteList Description}}

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
{{Fill AllowPortalToHaveElevatedTrust Description}}

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
{{Fill BrandingTitle Description}}

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSetting
{{Fill DefaultSetting Description}}

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
{{Fill DisableDeadlineRandom Description}}

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

### -DisplayNewProgramNotification
{{Fill DisplayNewProgramNotification Description}}

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
{{Fill EnableHealthAttestation Description}}

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
{{Fill EnableThirdPartyOrchestration Description}}

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
{{Fill FinalReminderMins Description}}

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

### -HealthAttestationUrl
{{Fill HealthAttestationUrl Description}}

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
{{Fill InitialReminderHr Description}}

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
{{Fill InputObject Description}}

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
{{Fill InstallRestriction Description}}

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
{{Fill InterimReminderHr Description}}

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
{{Fill Name Description}}

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
{{Fill PortalUrl Description}}

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
{{Fill PowerShellExecutionPolicy Description}}

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
{{Fill SelectWebsitePoint Description}}

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
{{Fill SuspendBitLocker Description}}

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
{{Fill UseNewSoftwareCenter Description}}

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
{{Fill UseOnPremisesHealthAttestation Description}}

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
{{Fill WebsitePointServerName Description}}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

