---
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
online version:
schema: 2.0.0
---

# Add-CMTaskSequenceDeploymentType

## SYNOPSIS

Create a task sequence as an app model deployment type.

## SYNTAX

### ByAppName (Default)
```
Add-CMTaskSequenceDeploymentType -ApplicationName <String> [-DeploymentTypeName <String>]
 [-EstimatedRuntimeMins <Int32>] [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallTaskSequenceId <String> [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppIdDetectionClause
```
Add-CMTaskSequenceDeploymentType -AddDetectionClause <DetectionClause[]> -ApplicationId <Int32>
 -DeploymentTypeName <String> [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-GroupDetectionClauses <String[]>] [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallTaskSequenceId <String> [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppNameDetectionClause
```
Add-CMTaskSequenceDeploymentType -AddDetectionClause <DetectionClause[]> -ApplicationName <String>
 -DeploymentTypeName <String> [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-GroupDetectionClauses <String[]>] [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallTaskSequenceId <String> [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValueDetectionClause
```
Add-CMTaskSequenceDeploymentType -AddDetectionClause <DetectionClause[]> -DeploymentTypeName <String>
 [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>] [-GroupDetectionClauses <String[]>]
 -InputObject <IResultObject> [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallTaskSequenceId <String> [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppIdScript
```
Add-CMTaskSequenceDeploymentType -ApplicationId <Int32> -DeploymentTypeName <String>
 [-EstimatedRuntimeMins <Int32>] [-ForceScriptDetection32Bit]
 [-InstallationBehaviorType <InstallationBehaviorType>] -InstallTaskSequenceId <String>
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction] [-ScriptFile <String>]
 -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallTaskSequenceId <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Add-CMTaskSequenceDeploymentType -ApplicationId <Int32> [-DeploymentTypeName <String>]
 [-EstimatedRuntimeMins <Int32>] [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallTaskSequenceId <String> [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppNameScript
```
Add-CMTaskSequenceDeploymentType -ApplicationName <String> -DeploymentTypeName <String>
 [-EstimatedRuntimeMins <Int32>] [-ForceScriptDetection32Bit]
 [-InstallationBehaviorType <InstallationBehaviorType>] -InstallTaskSequenceId <String>
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction] [-ScriptFile <String>]
 -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallTaskSequenceId <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValueScript
```
Add-CMTaskSequenceDeploymentType -DeploymentTypeName <String> [-EstimatedRuntimeMins <Int32>]
 [-ForceScriptDetection32Bit] -InputObject <IResultObject>
 [-InstallationBehaviorType <InstallationBehaviorType>] -InstallTaskSequenceId <String>
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction] [-ScriptFile <String>]
 -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UninstallTaskSequenceId <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Add-CMTaskSequenceDeploymentType [-DeploymentTypeName <String>] [-EstimatedRuntimeMins <Int32>]
 -InputObject <IResultObject> [-InstallationBehaviorType <InstallationBehaviorType>]
 -InstallTaskSequenceId <String> [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>] [-RequireUserInteraction]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Applies to version 2006 and later. Create a task sequence as an app model deployment type. For more information, see [Task sequence deployment type](/mem/configmgr/apps/get-started/creating-windows-applications#bkmk_tsdt).

This cmdlet has similar syntax as the MSI deployment type cmdlet [Add-CMMsiDeploymentType](Add-CMMsiDeploymentType.md). The primary differences are the following parameters:

- `-InstallTaskSequenceId <string>` (required): the ID of the task sequence to install the app

- `-UninstallTaskSequenceId <string>` (optional): the ID of the task sequence to uninstall the app

These two parameters relate to the deployment type task sequence options. They replace the `-InstallCommand` and `-UninstallCommand` parameters on the MSI cmdlet.

## EXAMPLES

### Example 1: Add a task sequence deployment type

This example adds the task sequence ID **ABC001EB** to the app **CBI**. It also adds the uninstall task sequence ID **ABC00378**.

```powershell
Add-CMTaskSequenceDeploymentType -ApplicationName "CBI" -DeploymentTypeName "Complex install" -Comment "New Deployment Type" -InstallTaskSequenceId "ABC001EB" -UninstallTaskSequenceId "ABC00378" -ScriptLanguage "PowerShell" -ScriptText "dir"
```

## PARAMETERS

### -AddDetectionClause
{{ Fill AddDetectionClause Description }}

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

### -EstimatedRuntimeMins

Specifies the estimated installation time, in minutes, of the deployment program for the application. This estimate is displayed to the user before the application installs.

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

Specifies an application object. To get an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

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

### -InstallTaskSequenceId

The ID of the task sequence to install the app

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

### -LogonRequirementType

Specifies the logon requirement for the deployment type. Valid values are:

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

Specifies the maximum run time in minutes of the deployment program for this application.

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

The path to the script to use to detect this deployment type. Use the **-ScriptLanguage** parameter to set the type of script.

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

### -UninstallTaskSequenceId

The ID of the task sequence to uninstall the app.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UninstallId, UninstallTaskSequencePackageId

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

[Task sequence deployment type](/mem/configmgr/apps/get-started/creating-windows-applications#bkmk_tsdt)
