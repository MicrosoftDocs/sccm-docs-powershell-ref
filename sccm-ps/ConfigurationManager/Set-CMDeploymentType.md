---
description: Change a deployment type for a Configuration Manager application.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/06/2020
schema: 2.0.0
title: Set-CMDeploymentType
---

# Set-CMDeploymentType

## SYNOPSIS

Change a deployment type for a Configuration Manager application.

## SYNTAX

### SetByValuePriority (Default)
```
Set-CMDeploymentType -InputObject <IResultObject> [-PassThru] [-Priority <PriorityChangeType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyMsiConfigureRule
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ClearRequirements] [-ContentLocation <String>] -DeploymentTypeName <String>
 [-DetectDeploymentTypeByCustomScript] [-EnableBranchCache <Boolean>]
 [-EnableContentLocationFallback <Boolean>] [-EstimatedInstallationTimeMins <Int32>]
 [-Force32BitDetectionScript <Boolean>] [-Force32BitInstaller <Boolean>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallationProgram <String>]
 [-InstallationProgramVisibility <UserInteractionMode>] [-InstallationStartIn <String>] [-Language <String[]>]
 [-LogonRequirementType <LogonRequirementType>] [-MaximumAllowedRunTimeMins <Int32>] [-MsiOrScriptInstaller]
 [-NewDeploymentTypeName <String>] [-OnSlowNetworkMode <ContentHandlingMode>] [-PassThru]
 [-PersistContentInClientCache <Boolean>] [-ProductCode <String>] [-RebootBehavior <RebootBehavior>]
 [-RemoveRequirement <Rule[]>] [-RequireUserInteraction <Boolean>] [-ScriptContent <String>]
 [-ScriptType <ScriptLanguage>] [-SourceUpdateProductCode <String>] [-UninstallProgram <String>]
 [-UninstallStartIn <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNamePropertyOtherInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ClearRequirements] [-ContentLocation <String>] -DeploymentTypeName <String> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyWindows8Installer
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ClearRequirements] [-ContentLocation <String>] -DeploymentTypeName <String> [-EnableBranchCache <Boolean>]
 [-EnableContentLocationFallback <Boolean>] [-Language <String[]>] [-MaximumAllowedRunTimeMins <Int32>]
 [-NewDeploymentTypeName <String>] [-OnSlowNetworkMode <ContentHandlingMode>] [-PassThru]
 [-PersistContentInClientCache <Boolean>] [-RemoveRequirement <Rule[]>] [-TriggerVpn <Boolean>]
 [-Windows8AppInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNamePropertyAppV5xInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-AppV5xInstaller] [-ClearRequirements] -DeploymentTypeName <String>
 [-EnableContentLocationFallback <Boolean>] [-EnablePeerToPeerContentDistribution <Boolean>]
 [-Language <String[]>] [-NewDeploymentTypeName <String>] [-OnFastNetworkMode <OnFastNetworkMode>]
 [-OnSlowNetworkMode <ContentHandlingMode>] [-PassThru] [-PersistContentInClientCache <Boolean>]
 [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNamePropertyAppVInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-AppVInstaller] [-ClearRequirements] -DeploymentTypeName <String> [-EnableContentLocationFallback <Boolean>]
 [-EnablePeerToPeerContentDistribution <Boolean>] [-Language <String[]>]
 [-LoadContentIntoAppVCacheBeforeLaunch <Boolean>] [-NewDeploymentTypeName <String>]
 [-OnFastNetworkMode <OnFastNetworkMode>] [-OnSlowNetworkMode <ContentHandlingMode>] [-PassThru]
 [-PersistContentInClientCache <Boolean>] [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyMacInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ClearRequirements] [-ContentLocation <String>] -DeploymentTypeName <String> [-InstallationProgram <String>]
 [-Language <String[]>] [-MacInstaller] [-MacRebootBehavior <MacRebootBehavior>]
 [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyWmInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ClearRequirements] [-ContentLocation <String>] -DeploymentTypeName <String> [-EnableUserUninstall <Boolean>]
 [-Language <String[]>] [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>]
 [-WindowsMobileInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNamePropertyWindowsStoreInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ApplicationNameInWindowsStore <String>] [-ClearRequirements] -DeploymentTypeName <String>
 [-Language <String[]>] [-MaximumAllowedRunTimeMins <Int32>] [-NewDeploymentTypeName <String>] [-PassThru]
 [-RemoteComputerName <String>] [-RemoveRequirement <Rule[]>] [-WindowsStoreInstaller]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyWebAppInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ClearRequirements] -DeploymentTypeName <String> [-Language <String[]>] [-NewDeploymentTypeName <String>]
 [-PassThru] [-RemoveRequirement <Rule[]>] [-WebAppInstaller] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyMobileMsiConfigureRule
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ClearRequirements] [-ContentLocation <String>] -DeploymentTypeName <String>
 [-InstallationCommandLine <String>] -Language <String[]> [-MobileMsiInstaller]
 [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyMobileMsiConfigureRule
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-ClearRequirements]
 [-ContentLocation <String>] -InputObject <IResultObject> [-InstallationCommandLine <String>]
 -Language <String[]> [-MobileMsiInstaller] [-NewDeploymentTypeName <String>] [-PassThru]
 [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValuePropertyMsiConfigureRule
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-ClearRequirements]
 [-ContentLocation <String>] [-DetectDeploymentTypeByCustomScript] [-EnableBranchCache <Boolean>]
 [-EnableContentLocationFallback <Boolean>] [-EstimatedInstallationTimeMins <Int32>]
 [-Force32BitDetectionScript <Boolean>] [-Force32BitInstaller <Boolean>] -InputObject <IResultObject>
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallationProgram <String>]
 [-InstallationProgramVisibility <UserInteractionMode>] [-InstallationStartIn <String>] [-Language <String[]>]
 [-LogonRequirementType <LogonRequirementType>] [-MaximumAllowedRunTimeMins <Int32>] [-MsiOrScriptInstaller]
 [-NewDeploymentTypeName <String>] [-OnSlowNetworkMode <ContentHandlingMode>] [-PassThru]
 [-PersistContentInClientCache <Boolean>] [-ProductCode <String>] [-RebootBehavior <RebootBehavior>]
 [-RemoveRequirement <Rule[]>] [-RequireUserInteraction <Boolean>] [-ScriptContent <String>]
 [-ScriptType <ScriptLanguage>] [-SourceUpdateProductCode <String>] [-UninstallProgram <String>]
 [-UninstallStartIn <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValuePropertyOtherInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-ClearRequirements]
 [-ContentLocation <String>] -InputObject <IResultObject> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyWindows8Installer
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-ClearRequirements]
 [-ContentLocation <String>] [-EnableBranchCache <Boolean>] [-EnableContentLocationFallback <Boolean>]
 -InputObject <IResultObject> [-Language <String[]>] [-MaximumAllowedRunTimeMins <Int32>]
 [-NewDeploymentTypeName <String>] [-OnSlowNetworkMode <ContentHandlingMode>] [-PassThru]
 [-PersistContentInClientCache <Boolean>] [-RemoveRequirement <Rule[]>] [-TriggerVpn <Boolean>]
 [-Windows8AppInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValuePropertyAppV5xInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-AppV5xInstaller]
 [-ClearRequirements] [-EnableContentLocationFallback <Boolean>]
 [-EnablePeerToPeerContentDistribution <Boolean>] -InputObject <IResultObject> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-OnFastNetworkMode <OnFastNetworkMode>]
 [-OnSlowNetworkMode <ContentHandlingMode>] [-PassThru] [-PersistContentInClientCache <Boolean>]
 [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValuePropertyAppVInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-AppVInstaller]
 [-ClearRequirements] [-EnableContentLocationFallback <Boolean>]
 [-EnablePeerToPeerContentDistribution <Boolean>] -InputObject <IResultObject> [-Language <String[]>]
 [-LoadContentIntoAppVCacheBeforeLaunch <Boolean>] [-NewDeploymentTypeName <String>]
 [-OnFastNetworkMode <OnFastNetworkMode>] [-OnSlowNetworkMode <ContentHandlingMode>] [-PassThru]
 [-PersistContentInClientCache <Boolean>] [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyMacInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-ClearRequirements]
 [-ContentLocation <String>] -InputObject <IResultObject> [-InstallationProgram <String>]
 [-Language <String[]>] [-MacInstaller] [-MacRebootBehavior <MacRebootBehavior>]
 [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyWmInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-ClearRequirements]
 [-ContentLocation <String>] [-EnableUserUninstall <Boolean>] -InputObject <IResultObject>
 [-Language <String[]>] [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>]
 [-WindowsMobileInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValuePropertyWindowsStoreInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>]
 [-ApplicationNameInWindowsStore <String>] [-ClearRequirements] -InputObject <IResultObject>
 [-Language <String[]>] [-MaximumAllowedRunTimeMins <Int32>] [-NewDeploymentTypeName <String>] [-PassThru]
 [-RemoteComputerName <String>] [-RemoveRequirement <Rule[]>] [-WindowsStoreInstaller]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyWebAppInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-ClearRequirements]
 -InputObject <IResultObject> [-Language <String[]>] [-NewDeploymentTypeName <String>] [-PassThru]
 [-RemoveRequirement <Rule[]>] [-WebAppInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyWindowsPhoneStoreInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] -ApplicationName <String>
 [-ClearRequirements] [-ContentLocation <String>] -DeploymentTypeName <String> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>] [-WindowsPhoneStoreInstaller]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyWindowsPhoneStoreInstaller
```
Set-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-ClearRequirements]
 [-ContentLocation <String>] -InputObject <IResultObject> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-PassThru] [-RemoveRequirement <Rule[]>] [-WindowsPhoneStoreInstaller]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePriority
```
Set-CMDeploymentType -ApplicationName <String> -DeploymentTypeName <String> [-PassThru]
 [-Priority <PriorityChangeType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByIdPriority
```
Set-CMDeploymentType -ApplicationName <String> -DeploymentTypeId <Int32> [-PassThru]
 [-Priority <PriorityChangeType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMDeploymentType** cmdlet changes a deployment type for an application in Configuration Manager. A deployment type is a part of the application that defines how that application installs on devices.

You can also use this cmdlet to change the priority for dependencies of the deployment type. Configuration Manager evaluates and installs dependencies of a deployment type in order of priorities before it installs the deployment type.

For more information, see [Introduction to application management - Deployment types](/mem/configmgr/apps/understand/introduction-to-application-management#deployment-type).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Increase the priority of a deployment application

This command configures a deployment type named **Configuration Manager Console - Windows Installer (Native)** for a application named **2 - Child** and increases the priority of that application.

```powershell
Set-CMDeploymentType -ApplicationName "2 - Child" -DeploymentTypeName "Configuration Manager Console - Windows Installer (Native)" -Priority Increase
```

## PARAMETERS

### -AddRequirement

Adds an array of requirements for this deployment type.

```yaml
Type: Rule[]
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministratorComment

Specifies a description for the deployment type.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName

Specifies the name of the deployment application that contains the deployment type.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByNamePropertyWindowsPhoneStoreInstaller, SetByNamePriority, SetByIdPriority
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationNameInWindowsStore

Specifies the name of the application in the Windows Store.

```yaml
Type: String
Parameter Sets: SetByNamePropertyWindowsStoreInstaller, SetByValuePropertyWindowsStoreInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppV5xInstaller

Indicates that the deployment type detects application information and deployment types from a Application Virtualization (App-V) 5.0 .appv package file.

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyAppV5xInstaller, SetByValuePropertyAppV5xInstaller
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppVInstaller

Indicates that the deployment type detects application information and deployment types from an App-V .appv package file.

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyAppVInstaller, SetByValuePropertyAppVInstaller
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearRequirements

Indicates that this cmdlet clears the deployment type requirements.

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentLocation

Specifies the path of the content. The site system server requires permission to read the content files.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases: InstallationFileLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeId

Specifies the type ID for a deployment type.

```yaml
Type: Int32
Parameter Sets: SetByIdPriority
Aliases: CIId, CI_ID, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeName

Specifies the name of a deployment type.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByNamePropertyWindowsPhoneStoreInstaller, SetByNamePriority
Aliases: LocalizedDisplayName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DetectDeploymentTypeByCustomScript

Indicates that the deployment type uses a custom script to detect the presence of this deployment type.

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
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

### -EnableBranchCache

Indicates that clients that use Windows BranchCache are allowed to download content from an on-premises distribution point. Content downloads from cloud-based distribution points can always be shared by clients that use Windows BranchCache.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyWindows8Installer, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer
Aliases: AllowClientsToShareContentOnSameSubnet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableContentLocationFallback

Indicate whether allows clients to use fall back source location for the content.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller
Aliases: AllowClientsToUseFallbackSourceLocationForContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePeerToPeerContentDistribution

Indicates whether clients can distribute content to other clients.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUserUninstall

Indicate whether to enable user uninstall.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyWmInstaller, SetByValuePropertyWmInstaller
Aliases: AllowUserToUninstall, AllowsUsersToUninstallThisContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EstimatedInstallationTimeMins

Specifies an estimated installation time in minutes.

```yaml
Type: Int32
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases: EstimatedInstallationTimeMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force32BitDetectionScript

Indicates whether to run script as 32-bit process on 64-bit clients.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases: RunScriptAs32BitProcessOn64BitClient

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force32BitInstaller

Indicates whether to run installer as 32-bit process on 64-bit clients.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases: RunInstallationAndUninstallProgramAs32BitProcessOn64BitClient

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

### -InputObject

Specifies a deployment type object for Configuration Manager. To obtain a deployment type object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValuePriority, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases: DeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallationBehaviorType

Specifies the installation behavior of the deployment type.

```yaml
Type: InstallationBehaviorType
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:
Accepted values: InstallForUser, InstallForSystem, InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationCommandLine

Specify the command line to install the application.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationProgram

Specifies the command line for the Windows Installer.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyMacInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyMacInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationProgramVisibility

Specifies the mode in which the deployment type runs on client devices.

```yaml
Type: UserInteractionMode
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:
Accepted values: Normal, Minimized, Maximized, Hidden

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationStartIn

Specifies the folder that contains the installation program for the deployment type. This folder can be an absolute path on the client, or a path to the distribution point folder that contains the installation files.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Language

Specifies an array of languages that the deployment type supports.

```yaml
Type: String[]
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadContentIntoAppVCacheBeforeLaunch

Indicates whether to load the content into the AppV cache when you deploy the application.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyAppVInstaller, SetByValuePropertyAppVInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogonRequirementType

Specifies the logon requirement for the deployment type.

```yaml
Type: LogonRequirementType
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:
Accepted values: OnlyWhenUserLoggedOn, WhereOrNotUserLoggedOn, WhetherOrNotUserLoggedOn, OnlyWhenNoUserLoggedOn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MacInstaller

Indicates that the deployment type detects application information and deployment types from a macOS installer (.cmmac) file that was created by using the CMAppUtil tool.

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyMacInstaller, SetByValuePropertyMacInstaller
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MacRebootBehavior

Specifies the reboot behavior for computers running macOS.

```yaml
Type: MacRebootBehavior
Parameter Sets: SetByNamePropertyMacInstaller, SetByValuePropertyMacInstaller
Aliases:
Accepted values: NoAction, ForceReboot

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumAllowedRunTimeMins

Specifies the maximum run time in minutes.

```yaml
Type: Int32
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyWindows8Installer, SetByNamePropertyWindowsStoreInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByValuePropertyWindowsStoreInstaller
Aliases: MaximumAllowedRunTimeMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MobileMsiInstaller

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MsiOrScriptInstaller

Indicates that the deployment uses a script installer program.

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewDeploymentTypeName

Specifies the name of a new deployment type.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnFastNetworkMode

Specifies the installation behavior of the deployment type on a fast network.

```yaml
Type: OnFastNetworkMode
Parameter Sets: SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller
Aliases:
Accepted values: RunLocal, RunFromNetwork, DownloadContentForStreaming

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnSlowNetworkMode

Specifies the installation behavior of the deployment type on a slow network.

```yaml
Type: ContentHandlingMode
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller
Aliases:
Accepted values: DoNothing, Download, DownloadContentForStreaming

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Returns the current working object. By default, this cmdlet doesn't generate any output.

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

### -PersistContentInClientCache

Indicates whether the deployment type saves content in cache indefinitely on the client computer.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority

Specifies a change for the priority of the deployment type.

```yaml
Type: PriorityChangeType
Parameter Sets: SetByValuePriority, SetByNamePriority, SetByIdPriority
Aliases:
Accepted values: Increase, Decrease

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductCode

Specifies the product code in the detection method for the deployment type.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RebootBehavior

Specifies the reboot behavior of the client computer.

```yaml
Type: RebootBehavior
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:
Accepted values: BasedOnExitCode, NoAction, ProgramReboot, ForceReboot

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteComputerName

Specifies a remote computer name.

```yaml
Type: String
Parameter Sets: SetByNamePropertyWindowsStoreInstaller, SetByValuePropertyWindowsStoreInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRequirement

Removes the existing installation requirements from this deployment type.

```yaml
Type: Rule[]
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByNamePropertyOtherInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyAppVInstaller, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireUserInteraction

Indicates whether a user can interact with the deployment type installation to configure the installation options.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases: RequiresUserInteraction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptContent

Specifies the script to detect the deployment type.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptType

Specifies the script language that you want to use to detect the deployment type.

```yaml
Type: ScriptLanguage
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:
Accepted values: PowerShell, VBScript, JavaScript

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceUpdateProductCode

Specifies the Windows Installer product code to enable installation source management. Windows Source management enables an MSI represented by this deployment type to be automatically updated or repaired from content source files on an available distribution point.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TriggerVpn

Indicates that a virtual private network (VPN) connection is used automatically.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyWindows8Installer, SetByValuePropertyWindows8Installer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UninstallProgram

Specifies the name of the uninstall program and any parameters it requires.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UninstallStartIn

Specifies the folder that contains the uninstall program for the deployment type. This folder can be an absolute path on the client, or a path that is relative to the distribution point folder that contains the package.

```yaml
Type: String
Parameter Sets: SetByNamePropertyMsiConfigureRule, SetByValuePropertyMsiConfigureRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebAppInstaller

Indicates that this cmdlet uses a web application installer for the deployment.

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyWebAppInstaller, SetByValuePropertyWebAppInstaller
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Windows8AppInstaller

Indicates that the deployment type detects application information and deployment types from a Windows app package (.appx) file.

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyWindows8Installer, SetByValuePropertyWindows8Installer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsMobileInstaller

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyWmInstaller, SetByValuePropertyWmInstaller
Aliases: WMInstaller

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsPhoneStoreInstaller

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsStoreInstaller

```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyWindowsStoreInstaller, SetByValuePropertyWindowsStoreInstaller
Aliases: DeepLinkInstaller

Required: True
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

### IResultObject#SMS_DeploymentType
## NOTES

To configure return codes on a deployment type, use the [Add-CMDeploymentTypeReturnCode](Add-CMDeploymentTypeReturnCode.md) cmdlet.

## RELATED LINKS

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Remove-CMDeploymentType](Remove-CMDeploymentType.md)
