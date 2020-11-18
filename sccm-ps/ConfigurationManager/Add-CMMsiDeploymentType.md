---
description: Adds a Windows Installer deployment type.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMMsiDeploymentType
---

# Add-CMMsiDeploymentType

## SYNOPSIS
Adds a Windows Installer deployment type.

## SYNTAX

### ByAppName (Default)
```
Add-CMMsiDeploymentType -ApplicationName <String> [-CacheContent] [-ContentFallback] -ContentLocation <String>
 [-DeploymentTypeName <String>] [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallCommand <String>]
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>]
 [-RepairCommand <String>] [-RepairWorkingDirectory <String>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppIdDetectionClause
```
Add-CMMsiDeploymentType -AddDetectionClause <DetectionClause[]> -ApplicationId <Int32> [-CacheContent]
 [-ContentFallback] [-ContentLocation <String>] -DeploymentTypeName <String>
 [-DetectionClauseConnector <Hashtable[]>] [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit]
 [-GroupDetectionClauses <String[]>] [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallCommand <String> [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RebootBehavior <PostExecutionBehavior>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppNameDetectionClause
```
Add-CMMsiDeploymentType -AddDetectionClause <DetectionClause[]> -ApplicationName <String> [-CacheContent]
 [-ContentFallback] [-ContentLocation <String>] -DeploymentTypeName <String>
 [-DetectionClauseConnector <Hashtable[]>] [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit]
 [-GroupDetectionClauses <String[]>] [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallCommand <String> [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RebootBehavior <PostExecutionBehavior>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValueDetectionClause
```
Add-CMMsiDeploymentType -AddDetectionClause <DetectionClause[]> [-CacheContent] [-ContentFallback]
 [-ContentLocation <String>] -DeploymentTypeName <String> [-DetectionClauseConnector <Hashtable[]>]
 [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-GroupDetectionClauses <String[]>]
 -InputObject <IResultObject> [-InstallationBehaviorType <InstallationBehaviorType>] -InstallCommand <String>
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RebootBehavior <PostExecutionBehavior>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppIdScript
```
Add-CMMsiDeploymentType -ApplicationId <Int32> [-CacheContent] [-ContentFallback] [-ContentLocation <String>]
 -DeploymentTypeName <String> [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit]
 [-ForceScriptDetection32Bit] [-InstallationBehaviorType <InstallationBehaviorType>] -InstallCommand <String>
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RebootBehavior <PostExecutionBehavior>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-RequireUserInteraction] [-ScriptFile <String>]
 -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-SourceUpdateProductCode <String>] [-UninstallCommand <String>] [-UninstallContentLocation <String>]
 [-UninstallOption <UninstallContentSetting>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Add-CMMsiDeploymentType -ApplicationId <Int32> [-CacheContent] [-ContentFallback] -ContentLocation <String>
 [-DeploymentTypeName <String>] [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallCommand <String>]
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>]
 [-RepairCommand <String>] [-RepairWorkingDirectory <String>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppNameScript
```
Add-CMMsiDeploymentType -ApplicationName <String> [-CacheContent] [-ContentFallback]
 [-ContentLocation <String>] -DeploymentTypeName <String> [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>]
 [-Force32Bit] [-ForceScriptDetection32Bit] [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallCommand <String> [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RebootBehavior <PostExecutionBehavior>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-RequireUserInteraction] [-ScriptFile <String>]
 -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-SourceUpdateProductCode <String>] [-UninstallCommand <String>] [-UninstallContentLocation <String>]
 [-UninstallOption <UninstallContentSetting>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValueScript
```
Add-CMMsiDeploymentType [-CacheContent] [-ContentFallback] [-ContentLocation <String>]
 -DeploymentTypeName <String> [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit]
 [-ForceScriptDetection32Bit] -InputObject <IResultObject>
 [-InstallationBehaviorType <InstallationBehaviorType>] -InstallCommand <String>
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RebootBehavior <PostExecutionBehavior>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-RequireUserInteraction] [-ScriptFile <String>]
 -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-SourceUpdateProductCode <String>] [-UninstallCommand <String>] [-UninstallContentLocation <String>]
 [-UninstallOption <UninstallContentSetting>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Add-CMMsiDeploymentType [-CacheContent] [-ContentFallback] -ContentLocation <String>
 [-DeploymentTypeName <String>] [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit]
 -InputObject <IResultObject> [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallCommand <String>]
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>]
 [-RepairCommand <String>] [-RepairWorkingDirectory <String>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMMsiDeploymentType** cmdlet adds a Windows Installer deployment type to an application.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a deployment type
```
PS XYZ:\>Add-CMMSiDeploymentType -ApplicationName "testMsi" -DeploymentTypeName "DTMsi" -ContentLocation "\\Server1\Applications\MSI\32BitSDK\32BitCompat.msi" -AddLanguage "en-US","zh-CN" -Comment "New Deployment Type"
```

This command adds the Windows Installer deployment type named DTMsi from the specified location to the application named testMsi in English and Chinese.

### Example 2: Add a deployment type by using the pipeline
```
PS XYZ:\> Get-CMApplication -Name "testMsi" | Add-CMMsiDeploymentType -DeploymentTypeName "DTMsiTest" -ContentLocation "\\Server1\Applications\MSI\32BitSDK\32BitCompat.msi" -AddLanguage "en-US","zh-CN" -Comment "New Deployment Type"
```

This command gets the application object named testMsi and uses the pipeline operator to pass the object to **Add-CMMsiDeploymentType**.
**Add-CMMsiDeploymentType** adds a Windows Installer deployment type named DTMsiTest from the specified location in English and Chinese.

## PARAMETERS

### -AddDetectionClause
```yaml
Type: DetectionClause[]
Parameter Sets: ByAppIdDetectionClause, ByAppNameDetectionClause, ByAppValueDetectionClause
Aliases: AddDetectionClauses

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguage
Adds an array of languages that this deployment type supports.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddLanguages, Languages, Language

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRequirement
Adds an array of requirements for this deployment type.

```yaml
Type: Rule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
Specifies the ID of the application that is associated with this deployment type.

```yaml
Type: Int32
Parameter Sets: ByAppIdDetectionClause, ByAppIdScript, ByAppId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies the name of the application that is associated with this deployment type.

```yaml
Type: String
Parameter Sets: ByAppName, ByAppNameDetectionClause, ByAppNameScript
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CacheContent
Indicates that the deployment type saves content indefinitely in the cache on the client computer.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PersistContentInClientCache

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
Specifies a description for this deployment type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdministratorComment

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

### -ContentFallback
Indicates that a client can use a fallback location provided by a management point.
A fallback location point provides an alternate location for source content when the content for the deployment type is not available on any of the preferred distribution points.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableContentLocationFallback, AllowClientsToUseFallbackSourceLocationForContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentLocation
Specifies the path to an msi file.
The site system server requires permissions to read the content files.

```yaml
Type: String
Parameter Sets: ByAppName, ByAppId, ByAppValue
Aliases: InstallationFileLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAppIdDetectionClause, ByAppNameDetectionClause, ByAppValueDetectionClause, ByAppIdScript, ByAppNameScript, ByAppValueScript
Aliases: InstallationFileLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeName
Specifies a display name for this deployment type.

```yaml
Type: String
Parameter Sets: ByAppName, ByAppId, ByAppValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAppIdDetectionClause, ByAppNameDetectionClause, ByAppValueDetectionClause, ByAppIdScript, ByAppNameScript, ByAppValueScript
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DetectionClauseConnector
{{ Fill DetectionClauseConnector Description }}

```yaml
Type: Hashtable[]
Parameter Sets: ByAppIdDetectionClause, ByAppNameDetectionClause, ByAppValueDetectionClause
Aliases: DetectionClauseConnectors

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

### -EnableBranchCache
Indicates that clients that use Windows BranchCache are allowed to download content from an on-premises distribution point.
Content downloads from cloud-based distribution points can always be shared by clients that use Windows BranchCache.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AllowClientsToShareContentOnSameSubnet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EstimatedRuntimeMins
Specifies the estimated installation time, in minutes, of the deployment program for the application.
This estimate is displayed to the user before the application installs.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: EstimatedInstallationTimeMinutes, EstimatedInstallationTimeMins, EstimatedRunTimeMinutes

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
Aliases: ForceForUnknownPublisher

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force32Bit
Indicates that the deployment type uses the Microsoft Windows-32-on-Windows-64 (WOW64) subsystem to run the installation on a 64-bit client computer.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: Force32BitInstaller

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceScriptDetection32Bit
Indicates that the deployment type uses the Microsoft Windows-32-on-Windows-64 (WOW64) subsystem to run a script on a 64-bit client computer.

```yaml
Type: SwitchParameter
Parameter Sets: ByAppIdScript, ByAppNameScript, ByAppValueScript
Aliases: Force32BitDetectionScript

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

### -GroupDetectionClauses
{{ Fill GroupDetectionClauses Description }}

```yaml
Type: String[]
Parameter Sets: ByAppIdDetectionClause, ByAppNameDetectionClause, ByAppValueDetectionClause
Aliases: GroupDetectionClausesByLogicalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an application object.
To obtain an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByAppValueDetectionClause, ByAppValueScript, ByAppValue
Aliases: Application

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallCommand
Specifies the command to use to install the Windows Installer package from the command line.

```yaml
Type: String
Parameter Sets: ByAppName, ByAppId, ByAppValue
Aliases: InstallationProgram

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAppIdDetectionClause, ByAppNameDetectionClause, ByAppValueDetectionClause, ByAppIdScript, ByAppNameScript, ByAppValueScript
Aliases: InstallationProgram

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallWorkingDirectory
Specifies the folder that contains the installation program for the deployment type.
This folder can be an absolute path on the client, or a path to the distribution point folder that contains the installation files.

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstallationStartIn, InstallFolder

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationBehaviorType
Specifies the installation behavior of the deployment type.
Valid values are:

- InstallForUser
- InstallForSystem
- InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser

```yaml
Type: InstallationBehaviorType
Parameter Sets: (All)
Aliases:
Accepted values: InstallForUser, InstallForSystem, InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser

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
- WhetherOrNotUserLoggedOn

```yaml
Type: LogonRequirementType
Parameter Sets: (All)
Aliases:
Accepted values: OnlyWhenUserLoggedOn, WhereOrNotUserLoggedOn, WhetherOrNotUserLoggedOn, OnlyWhenNoUserLoggedOn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumRuntimeMins
Specifies the maximum run time, in minutes, of the deployment program for this application.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumAllowedRunTimeMinutes, MaximumAllowedRunTimeMins, MaximumRunTimeMinutes

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
Parameter Sets: ByAppName, ByAppId, ByAppValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RebootBehavior

Specifies the reboot behavior.

```yaml
Type: PostExecutionBehavior
Parameter Sets: (All)
Aliases:
Accepted values: BasedOnExitCode, NoAction, ForceReboot, ProgramReboot

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLanguage

Removes the existing supported languages from this deployment type.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveLanguages

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
Parameter Sets: (All)
Aliases: RemoveRequirements

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RepairCommand
Starting in version 2002, use this parameter to configure the repair command and directory options when creating deployment type. Also configure the RepairWorkingDirectory parameter.


```yaml
Type: String
Parameter Sets: (All)
Aliases: RepairProgram

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RepairWorkingDirectory
Starting in version 2002, use this parameter to configure the repair command and directory options when creating deployment type. Also configure the RepairCommand parameter.


```yaml
Type: String
Parameter Sets: (All)
Aliases: RepairStartIn, RepairFolder

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireUserInteraction
Indicates whether a user can interact with the deployment type installation to configure the installation options.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: RequiresUserInteraction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptFile
```yaml
Type: String
Parameter Sets: ByAppIdScript, ByAppNameScript, ByAppValueScript
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptLanguage
Specifies the script language that you want to use to detect this deployment type.
Valid values are:

- PowerShell
- VBScript
- JavaScript

```yaml
Type: ScriptLanguage
Parameter Sets: ByAppIdScript, ByAppNameScript, ByAppValueScript
Aliases: ScriptType
Accepted values: PowerShell, VBScript, JavaScript

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptText
Specifies the script to use to detect this deployment type.

```yaml
Type: String
Parameter Sets: ByAppIdScript, ByAppNameScript, ByAppValueScript
Aliases: ScriptContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SlowNetworkDeploymentMode
Specifies the installation behavior of the deployment type on a slow network.
Valid values are:

- DoNothing
- Download
- DownloadContentForStreaming

```yaml
Type: ContentHandlingMode
Parameter Sets: (All)
Aliases:
Accepted values: DoNothing, Download

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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UninstallCommand
Specifies the command to use to uninstall the Windows Installer package from the command line.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UninstallationProgram

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UninstallContentLocation
{{ Fill UninstallContentLocation Description }}

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

### -UninstallOption
{{ Fill UninstallOption Description }}

```yaml
Type: UninstallContentSetting
Parameter Sets: (All)
Aliases:
Accepted values: SameAsInstall, NoneRequired, Different

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UninstallWorkingDirectory
Specifies the folder that contains the uninstall program for the deployment type.
This folder can be an absolute path on the client, or a path that is relative to the distribution point folder that contains the package.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UninstallationStartIn, UninstallFolder

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserInteractionMode
Specifies the mode in which the deployment type runs on client devices.
Valid values are:

- Normal
- Minimized
- Maximized
- Hidden

```yaml
Type: UserInteractionMode
Parameter Sets: (All)
Aliases: InstallationProgramVisibility
Accepted values: Normal, Minimized, Maximized, Hidden

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Set-CMMsiDeploymentType](Set-CMMsiDeploymentType.md)


