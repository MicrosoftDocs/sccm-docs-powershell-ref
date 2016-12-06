---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833783
schema: 2.0.0
ms.assetid: AB2468DA-0537-401E-A689-523831E85FBE
---

# Set-CMDeploymentType

## SYNOPSIS
Changes a deployment type.

## SYNTAX

### SetByValuePriority (Default)
```
Set-CMDeploymentType -InputObject <IResultObject> [-Priority <PriorityChangeType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyOtherInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] -ApplicationName <String> [-ContentLocation <String>]
 -DeploymentTypeName <String> [-Language <String[]>] [-NewDeploymentTypeName <String>]
 [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyAppV5xInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableContentLocationFallback <Boolean>]
 [-AppV5xInstaller] -ApplicationName <String> -DeploymentTypeName <String>
 [-EnablePeerToPeerContentDistribution <Boolean>] [-Language <String[]>] [-NewDeploymentTypeName <String>]
 [-OnFastNetworkMode <OnFastNetworkMode>] [-OnSlowNetworkMode <ContentHandlingMode>]
 [-PersistContentInClientCache <Boolean>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>]
 [-ClearRequirements] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNamePropertyAppVInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableContentLocationFallback <Boolean>]
 [-AppVInstaller] -ApplicationName <String> -DeploymentTypeName <String>
 [-EnablePeerToPeerContentDistribution <Boolean>] [-Language <String[]>]
 [-LoadContentIntoAppVCacheBeforeLaunch <Boolean>] [-NewDeploymentTypeName <String>]
 [-OnFastNetworkMode <OnFastNetworkMode>] [-OnSlowNetworkMode <ContentHandlingMode>]
 [-PersistContentInClientCache <Boolean>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>]
 [-ClearRequirements] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNamePropertyMacInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] -ApplicationName <String> [-ContentLocation <String>]
 -DeploymentTypeName <String> [-InstallationProgram <String>] [-Language <String[]>] [-MacInstaller]
 [-MacRebootBehavior <MacRebootBehavior>] [-NewDeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyWmInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableUserUninstall <Boolean>]
 -ApplicationName <String> [-ContentLocation <String>] -DeploymentTypeName <String> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-WindowsMobileInstaller] [-AddRequirement <Rule[]>]
 [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyWindowsStoreInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] -ApplicationName <String>
 [-ApplicationNameInWindowsStore <String>] [-WindowsStoreInstaller] -DeploymentTypeName <String>
 [-Language <String[]>] [-MaximumAllowedRunTimeMins <Int32>] [-NewDeploymentTypeName <String>]
 [-RemoteComputerName <String>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>] [-ClearRequirements]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyWebAppInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] -ApplicationName <String> -DeploymentTypeName <String>
 [-Language <String[]>] [-NewDeploymentTypeName <String>] [-WebAppInstaller] [-AddRequirement <Rule[]>]
 [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyMobileMsiConfigureRule
```
Set-CMDeploymentType [-AdministratorComment <String>] -ApplicationName <String> [-ContentLocation <String>]
 -DeploymentTypeName <String> [-InstallationCommandLine <String>] -Language <String[]> [-MobileMsiInstaller]
 [-NewDeploymentTypeName <String>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>]
 [-ClearRequirements] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValuePropertyMobileMsiConfigureRule
```
Set-CMDeploymentType [-AdministratorComment <String>] [-ContentLocation <String>] -InputObject <IResultObject>
 [-InstallationCommandLine <String>] -Language <String[]> [-MobileMsiInstaller]
 [-NewDeploymentTypeName <String>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>]
 [-ClearRequirements] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValuePropertyMsiConfigureRule
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableBranchCache <Boolean>]
 [-EnableContentLocationFallback <Boolean>] [-ContentLocation <String>] [-DetectDeploymentTypeByCustomScript]
 [-EstimatedInstallationTimeMins <Int32>] -InputObject <IResultObject>
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallationProgram <String>]
 [-InstallationProgramVisibility <UserInteractionMode>] [-InstallationStartIn <String>] [-Language <String[]>]
 [-LogonRequirementType <LogonRequirementType>] [-MaximumAllowedRunTimeMins <Int32>] [-MsiOrScriptInstaller]
 [-NewDeploymentTypeName <String>] [-OnSlowNetworkMode <ContentHandlingMode>]
 [-PersistContentInClientCache <Boolean>] [-ProductCode <String>] [-RebootBehavior <RebootBehavior>]
 [-RequireUserInteraction <Boolean>] [-Force32BitInstaller <Boolean>] [-Force32BitDetectionScript <Boolean>]
 [-ScriptContent <String>] [-ScriptType <ScriptLanguage>] [-UninstallProgram <String>]
 [-UninstallStartIn <String>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>] [-ClearRequirements]
 [-SourceUpdateProductCode <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyOtherInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-ContentLocation <String>] -InputObject <IResultObject>
 [-Language <String[]>] [-NewDeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyWindows8Installer
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableBranchCache <Boolean>]
 [-EnableContentLocationFallback <Boolean>] [-ContentLocation <String>] -InputObject <IResultObject>
 [-Language <String[]>] [-MaximumAllowedRunTimeMins <Int32>] [-NewDeploymentTypeName <String>]
 [-OnSlowNetworkMode <ContentHandlingMode>] [-PersistContentInClientCache <Boolean>] [-TriggerVpn <Boolean>]
 [-Windows8AppInstaller] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>] [-ClearRequirements]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyAppV5xInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableContentLocationFallback <Boolean>]
 [-AppV5xInstaller] [-EnablePeerToPeerContentDistribution <Boolean>] -InputObject <IResultObject>
 [-Language <String[]>] [-NewDeploymentTypeName <String>] [-OnFastNetworkMode <OnFastNetworkMode>]
 [-OnSlowNetworkMode <ContentHandlingMode>] [-PersistContentInClientCache <Boolean>] [-AddRequirement <Rule[]>]
 [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyWindows8Installer
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableBranchCache <Boolean>]
 [-EnableContentLocationFallback <Boolean>] -ApplicationName <String> [-ContentLocation <String>]
 -DeploymentTypeName <String> [-Language <String[]>] [-MaximumAllowedRunTimeMins <Int32>]
 [-NewDeploymentTypeName <String>] [-OnSlowNetworkMode <ContentHandlingMode>]
 [-PersistContentInClientCache <Boolean>] [-TriggerVpn <Boolean>] [-Windows8AppInstaller]
 [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyMacInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-ContentLocation <String>] -InputObject <IResultObject>
 [-InstallationProgram <String>] [-Language <String[]>] [-MacInstaller]
 [-MacRebootBehavior <MacRebootBehavior>] [-NewDeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyWmInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableUserUninstall <Boolean>]
 [-ContentLocation <String>] -InputObject <IResultObject> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-WindowsMobileInstaller] [-AddRequirement <Rule[]>]
 [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyWindowsStoreInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-ApplicationNameInWindowsStore <String>]
 [-WindowsStoreInstaller] -InputObject <IResultObject> [-Language <String[]>]
 [-MaximumAllowedRunTimeMins <Int32>] [-NewDeploymentTypeName <String>] [-RemoteComputerName <String>]
 [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyWebAppInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] -InputObject <IResultObject> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-WebAppInstaller] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>]
 [-ClearRequirements] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNamePropertyWindowsPhoneStoreInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-WindowsPhoneStoreInstaller] -ApplicationName <String>
 [-ContentLocation <String>] -DeploymentTypeName <String> [-Language <String[]>]
 [-NewDeploymentTypeName <String>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>]
 [-ClearRequirements] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValuePropertyWindowsPhoneStoreInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-WindowsPhoneStoreInstaller] [-ContentLocation <String>]
 -InputObject <IResultObject> [-Language <String[]>] [-NewDeploymentTypeName <String>]
 [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>] [-ClearRequirements] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNamePropertyMsiConfigureRule
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableBranchCache <Boolean>]
 [-EnableContentLocationFallback <Boolean>] -ApplicationName <String> [-ContentLocation <String>]
 -DeploymentTypeName <String> [-DetectDeploymentTypeByCustomScript] [-EstimatedInstallationTimeMins <Int32>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallationProgram <String>]
 [-InstallationProgramVisibility <UserInteractionMode>] [-InstallationStartIn <String>] [-Language <String[]>]
 [-LogonRequirementType <LogonRequirementType>] [-MaximumAllowedRunTimeMins <Int32>] [-MsiOrScriptInstaller]
 [-NewDeploymentTypeName <String>] [-OnSlowNetworkMode <ContentHandlingMode>]
 [-PersistContentInClientCache <Boolean>] [-ProductCode <String>] [-RebootBehavior <RebootBehavior>]
 [-RequireUserInteraction <Boolean>] [-Force32BitInstaller <Boolean>] [-Force32BitDetectionScript <Boolean>]
 [-ScriptContent <String>] [-ScriptType <ScriptLanguage>] [-UninstallProgram <String>]
 [-UninstallStartIn <String>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>] [-ClearRequirements]
 [-SourceUpdateProductCode <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByValuePropertyAppVInstaller
```
Set-CMDeploymentType [-AdministratorComment <String>] [-EnableContentLocationFallback <Boolean>]
 [-AppVInstaller] [-EnablePeerToPeerContentDistribution <Boolean>] -InputObject <IResultObject>
 [-Language <String[]>] [-LoadContentIntoAppVCacheBeforeLaunch <Boolean>] [-NewDeploymentTypeName <String>]
 [-OnFastNetworkMode <OnFastNetworkMode>] [-OnSlowNetworkMode <ContentHandlingMode>]
 [-PersistContentInClientCache <Boolean>] [-AddRequirement <Rule[]>] [-RemoveRequirement <Rule[]>]
 [-ClearRequirements] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNamePriority
```
Set-CMDeploymentType -ApplicationName <String> -DeploymentTypeName <String> [-Priority <PriorityChangeType>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByIdPriority
```
Set-CMDeploymentType -ApplicationName <String> -DeploymentTypeId <Int32> [-Priority <PriorityChangeType>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDeploymentType** cmdlet changes a deployment type for a deployment application in Microsoft System Center Configuration Manager.
A deployment type is a part of the application that defines how that application deploys other applications to devices.
You can also use this cmdlet to change the priority for dependencies of the deployment type.
Configuration Manager evaluates and installs dependencies of a deployment type in order of priorities before it installs the deployment type.

## EXAMPLES

### Example 1: Increase the priority of a deployment application
```
PS C:\>Set-CMDeploymentType -ApplicationName "2 - Child" -DeploymentTypeName "Configuration Manager Console - Windows Installer (Native)" -Priority Increase
```

This command sets a deployment type named Configuration Manager Console - Windows Installer (Native) for a deployment application named 2 - Child and increases the priority of that application.

### Example 2: Decrease the priority of a deployment application
```
PS C:\>Set-CMDeploymentType -ApplicationName "2 - Child" -DeploymentTypeName "Configuration Manager Console - Windows Installer (Native)" -Priority Decrease
```

This command sets a deployment type named Configuration Manager Console - Windows Installer (Native) for a deployment application named 2 - Child and decreases the priority of that application.

## PARAMETERS

### -AddRequirement


```yaml
Type: Rule[]
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
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
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
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

### -ApplicationName
Specifies the name of the deployment application that contains the deployment type.

```yaml
Type: String
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByNamePropertyWindows8Installer, SetByNamePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule, SetByNamePriority, SetByIdPriority
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

### -ClearRequirements


```yaml
Type: SwitchParameter
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
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

### -ContentLocation
Specifies the path of the content.
The site system server requires permission to read the content files.

```yaml
Type: String
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByNamePropertyWindows8Installer, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule
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
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByNamePropertyWindows8Installer, SetByNamePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule, SetByNamePriority
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
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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


```yaml
Type: Boolean
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByNamePropertyWindows8Installer, SetByNamePropertyMsiConfigureRule
Aliases: AllowClientsToShareContentOnSameSubnet
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableContentLocationFallback


```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
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


```yaml
Type: Int32
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: EstimatedInstallationTimeMinutes
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force32BitDetectionScript


```yaml
Type: Boolean
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: RunScriptAs32BitProcessOn64BitClient
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force32BitInstaller


```yaml
Type: Boolean
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: RunInstallationAndUninstallProgramAs32BitProcessOn64BitClient
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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
Specifies a deployment type object for Configuration Manager.
To obtain a deployment type object, use the **Get-CMDeploymentType** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValuePriority, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByValuePropertyWindowsPhoneStoreInstaller, SetByValuePropertyAppVInstaller
Aliases: DeploymentType
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallationBehaviorType
Specifies the installation behavior of the deployment type.
Valid values are: 

- InstallForSystem
- InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser
- InstallForUser

```yaml
Type: InstallationBehaviorType
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: 
Accepted values: InstallForUser, InstallForSystem, InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationCommandLine


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
Parameter Sets: SetByNamePropertyMacInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyMacInstaller, SetByNamePropertyMsiConfigureRule
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationProgramVisibility
Specifies the mode in which the deployment type runs on client devices.
Valid values are: 

- Normal
- Minimized
- Maximized
- Hidden

```yaml
Type: UserInteractionMode
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: 
Accepted values: Normal, Minimized, Maximized, Hidden
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationStartIn
Specifies the folder that contains the installation program for the deployment type.
This folder can be an absolute path on the client, or a path to the distribution point folder that contains the installation files.

```yaml
Type: String
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
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
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
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
Valid values are: 

- OnlyWhenNoUserLoggedOn
- OnlyWhenUserLoggedOn
- WhereOrNotUserLoggedOn

```yaml
Type: LogonRequirementType
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: 
Accepted values: OnlyWhenUserLoggedOn, WhereOrNotUserLoggedOn, WhetherOrNotUserLoggedOn, OnlyWhenNoUserLoggedOn
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MacInstaller
Indicates that the deployment type detects application information and deployment types from a Mac OS X Installer (.cmmac) file that was created by using the CMAppUtil tool.

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
Specifies the reboot behavior for computers running Mac OS X software.

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


```yaml
Type: Int32
Parameter Sets: SetByNamePropertyWindowsStoreInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByNamePropertyWindows8Installer, SetByValuePropertyWindowsStoreInstaller, SetByNamePropertyMsiConfigureRule
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
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
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
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnFastNetworkMode
Specifies the installation behavior of the deployment type on a fast network.
Valid values are: 

- RunFromNetwork
- RunLocal

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
Valid values are: 

- DoNothing
- Download
- DownloadContentForStreaming

```yaml
Type: ContentHandlingMode
Parameter Sets: SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
Aliases: 
Accepted values: DoNothing, Download, DownloadContentForStreaming
Required: False
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

### -PersistContentInClientCache
Indicates whether the deployment type saves content in cache indefinitely on the client computer.

```yaml
Type: Boolean
Parameter Sets: SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByValuePropertyMsiConfigureRule, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Specifies a change for the priority of the deployment type.
Valid values are: Increase and Decrease.

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
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
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
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
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


```yaml
Type: Rule[]
Parameter Sets: SetByNamePropertyOtherInstaller, SetByNamePropertyAppV5xInstaller, SetByNamePropertyAppVInstaller, SetByNamePropertyMacInstaller, SetByNamePropertyWmInstaller, SetByNamePropertyWindowsStoreInstaller, SetByNamePropertyWebAppInstaller, SetByNamePropertyMobileMsiConfigureRule, SetByValuePropertyMobileMsiConfigureRule, SetByValuePropertyMsiConfigureRule, SetByValuePropertyOtherInstaller, SetByValuePropertyWindows8Installer, SetByValuePropertyAppV5xInstaller, SetByNamePropertyWindows8Installer, SetByValuePropertyMacInstaller, SetByValuePropertyWmInstaller, SetByValuePropertyWindowsStoreInstaller, SetByValuePropertyWebAppInstaller, SetByNamePropertyWindowsPhoneStoreInstaller, SetByValuePropertyWindowsPhoneStoreInstaller, SetByNamePropertyMsiConfigureRule, SetByValuePropertyAppVInstaller
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireUserInteraction


```yaml
Type: Boolean
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: RequiresUserInteraction
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptContent
Specifies the script language that you want to use to detect the deployment type.

```yaml
Type: String
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
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
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: 
Accepted values: PowerShell, VBScript, JavaScript
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceUpdateProductCode
Specifies the Windows Installer product code to enable installation source management.
Windows Source management enables an MSI represented by this deployment type to be automatically updated or repaired from content source files on an available distribution point.

```yaml
Type: String
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TriggerVpn
@{Text=}

```yaml
Type: Boolean
Parameter Sets: SetByValuePropertyWindows8Installer, SetByNamePropertyWindows8Installer
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
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UninstallStartIn
Specifies the folder that contains the uninstall program for the deployment type.
This folder can be an absolute path on the client, or a path that is relative to the distribution point folder that contains the package.

```yaml
Type: String
Parameter Sets: SetByValuePropertyMsiConfigureRule, SetByNamePropertyMsiConfigureRule
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebAppInstaller
@{Text=}

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

### -Windows8AppInstaller
Indicates that the deployment type detects application information and deployment types from a Windows app package (.appx) file.

```yaml
Type: SwitchParameter
Parameter Sets: SetByValuePropertyWindows8Installer, SetByNamePropertyWindows8Installer
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMDeploymentType](./Add-CMDeploymentType.md)

[Get-CMDeploymentType](./Get-CMDeploymentType.md)

[Remove-CMDeploymentType](./Remove-CMDeploymentType.md)


