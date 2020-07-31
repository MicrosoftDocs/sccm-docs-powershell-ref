---
description: Adds a script installer deployment type.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/15/2018
schema: 2.0.0
title: Add-CMScriptDeploymentType
---

# Add-CMScriptDeploymentType

## SYNOPSIS

Adds a script installer deployment type.

## SYNTAX

### ByAppNameScript (Default)
```
Add-CMScriptDeploymentType [-ContentLocation <String>] -DeploymentTypeName <String> -InstallCommand <String>
 -ApplicationName <String> [-CacheContent] [-ContentFallback] [-EnableBranchCache]
 [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-ForceScriptDetection32Bit] [-InstallWorkingDirectory <String>]
 [-RepairCommand <String>] [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] -ScriptLanguage <ScriptLanguage>
 [-ScriptText <String>] [-ScriptFile <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Add-CMScriptDeploymentType -ProductCode <String> [-ContentLocation <String>] -DeploymentTypeName <String>
 -InstallCommand <String> -ApplicationId <Int32> [-CacheContent] [-ContentFallback] [-EnableBranchCache]
 [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-InstallWorkingDirectory <String>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppName
```
Add-CMScriptDeploymentType -ProductCode <String> [-ContentLocation <String>] -DeploymentTypeName <String>
 -InstallCommand <String> -ApplicationName <String> [-CacheContent] [-ContentFallback] [-EnableBranchCache]
 [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-InstallWorkingDirectory <String>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Add-CMScriptDeploymentType -ProductCode <String> [-ContentLocation <String>] -DeploymentTypeName <String>
 -InstallCommand <String> -InputObject <IResultObject> [-CacheContent] [-ContentFallback] [-EnableBranchCache]
 [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-InstallWorkingDirectory <String>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppIdDetectionClause
```
Add-CMScriptDeploymentType [-ContentLocation <String>] -DeploymentTypeName <String> -InstallCommand <String>
 -AddDetectionClause <DetectionClause[]> [-GroupDetectionClauses <String[]>]
 [-DetectionClauseConnector <Hashtable[]>] -ApplicationId <Int32> [-CacheContent] [-ContentFallback]
 [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-InstallWorkingDirectory <String>]
 [-RepairCommand <String>] [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppNameDetectionClause
```
Add-CMScriptDeploymentType [-ContentLocation <String>] -DeploymentTypeName <String> -InstallCommand <String>
 -AddDetectionClause <DetectionClause[]> [-GroupDetectionClauses <String[]>]
 [-DetectionClauseConnector <Hashtable[]>] -ApplicationName <String> [-CacheContent] [-ContentFallback]
 [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-InstallWorkingDirectory <String>]
 [-RepairCommand <String>] [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValueDetectionClause
```
Add-CMScriptDeploymentType [-ContentLocation <String>] -DeploymentTypeName <String> -InstallCommand <String>
 -AddDetectionClause <DetectionClause[]> [-GroupDetectionClauses <String[]>]
 [-DetectionClauseConnector <Hashtable[]>] -InputObject <IResultObject> [-CacheContent] [-ContentFallback]
 [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-InstallWorkingDirectory <String>]
 [-RepairCommand <String>] [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppIdScript
```
Add-CMScriptDeploymentType [-ContentLocation <String>] -DeploymentTypeName <String> -InstallCommand <String>
 -ApplicationId <Int32> [-CacheContent] [-ContentFallback] [-EnableBranchCache] [-EstimatedRuntimeMins <Int32>]
 [-Force32Bit] [-ForceScriptDetection32Bit] [-InstallWorkingDirectory <String>] [-RepairCommand <String>]
 [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] -ScriptLanguage <ScriptLanguage>
 [-ScriptText <String>] [-ScriptFile <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValueScript
```
Add-CMScriptDeploymentType [-ContentLocation <String>] -DeploymentTypeName <String> -InstallCommand <String>
 -InputObject <IResultObject> [-CacheContent] [-ContentFallback] [-EnableBranchCache]
 [-EstimatedRuntimeMins <Int32>] [-Force32Bit] [-ForceScriptDetection32Bit] [-InstallWorkingDirectory <String>]
 [-RepairCommand <String>] [-RepairWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction] -ScriptLanguage <ScriptLanguage>
 [-ScriptText <String>] [-ScriptFile <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallCommand <String>] [-UninstallWorkingDirectory <String>]
 [-UserInteractionMode <UserInteractionMode>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Add-CMScriptDeploymentType** cmdlet adds a script installer deployment type to an application. Configuration Manager has an integrated ability to run Powershell scripts. The scripts simplify building custom tools to administer software and let you accomplish mundane tasks quickly, allowing you to get large jobs done more easily and more consistently. For more information, see [Create and run PowerShell scripts from the Configuration Manager console](/sccm/apps/deploy-use/create-deploy-scripts).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a script deployment type to an application

```powershell
PS XYZ:\>Add-CMScriptDeploymentType -ApplicationName "Application01" -DeploymentTypeName "ScriptDT01" -Comment "Div A script" -InstallCommand 'msiexec /i ""\\Machine01\Resources\Applications\MSI\AdvertMSI\AdvertMSI.msi"' -ScriptLanguage VBScript -ScriptContent "1231231" -ForceScriptDetection32Bit
```

This command adds the script deployment type named ScriptDT01 to the application named Application 01, providing the installation command, specifying the script language as VBScript, and providing the text of the script.
Specifying the *ForceScriptDetection32Bit* indicates that the deployment type will use the WOW64 subsystem to run the script on a 64-bit computer.

### Example 2: Add a script deployment type to an application by using the pipeline

```powershell
PS XYZ:\> Get-CMApplication -Name "Application01" | Add-CMScriptDeploymentType  -DeploymentTypeName "ScriptDT02" -Comment "Div A script" -InstallCommand 'msiexec /i ""\\Machine01\Resources\Applications\MSI\AdvertMSI\AdvertMSI.msi"' -ScriptLanguage VBScript -ScriptContent "1231231" -ForceScriptDetection32Bit
```

This command gets the application object named Application 01 and uses the pipeline operator to pass the object to **Add-CMScriptDeploymentType**.
**Add-CMScriptDeploymentType** adds a script deployment type named ScriptDT02, providing the installation command, specifying the script language as VBScript, and providing the text of the script.
Specifying the *ForceScriptDetection32Bit* indicates that the deployment type will use the WOW64 subsystem to run the script on a 64-bit computer.

## PARAMETERS

### -AddDetectionClause

Specifies an array of detection method clauses that this deployment type supports.

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
Parameter Sets: ByAppId, ByAppIdDetectionClause, ByAppIdScript
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
Parameter Sets: ByAppNameScript, ByAppName, ByAppNameDetectionClause
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

Specifies the path of the content.
The site system server requires permissions to read the content files.

```yaml
Type: String
Parameter Sets: (All)
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
Parameter Sets: (All)
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
This estimate is displayed before the application installs.

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
Parameter Sets: ByAppNameScript, ByAppIdScript, ByAppValueScript
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
Parameter Sets: ByAppValue, ByAppValueDetectionClause, ByAppValueScript
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
Parameter Sets: (All)
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
Parameter Sets: ByAppId, ByAppName, ByAppValue
Aliases:

Required: True
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

Specifies the script file that you want to use to detect this deployment type.

```yaml
Type: String
Parameter Sets: ByAppNameScript, ByAppIdScript, ByAppValueScript
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
- Jscript
- ScriptText

```yaml
Type: ScriptLanguage
Parameter Sets: ByAppNameScript, ByAppIdScript, ByAppValueScript
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
Parameter Sets: ByAppNameScript, ByAppIdScript, ByAppValueScript
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

[Approve-CMScript](Approve-CMScript.md)

[Deny-CMScript](Deny-CMScript.md)

[Invoke-CMScript](Invoke-CMScript.md)

[Remove-CMScript](Remove-CMScript.md)

[Set-CMScriptDeploymentType](Set-CMScriptDeploymentType.md)

[Get-CMApplication](Get-CMApplication.md)

[New-CMApplication](New-CMApplication.md)
