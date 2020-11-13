---
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
online version:
schema: 2.0.0
---

# Set-CMTaskSequenceDeploymentType

## SYNOPSIS

Configure a task sequence deployment type on an application.

## SYNTAX

### ByAppName (Default)
```
Set-CMTaskSequenceDeploymentType [-AddDetectionClause <DetectionClause[]>]
 [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-ForceScriptDetection32Bit <Boolean>] [-GroupDetectionClauses <String[]>]
 [-InstallationBehaviorType <InstallationBehaviorType>] -InstallTaskSequenceId <String>
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>] [-ProductCode <String>]
 [-RebootBehavior <PostExecutionBehavior>] [-RemoveDetectionClause <String[]>]
 [-RequireUserInteraction <Boolean>] [-ScriptFile <String>] [-ScriptLanguage <ScriptLanguage>]
 [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] -ApplicationName <String>
 -DeploymentTypeName <String> [-NewName <String>] [-PassThru] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Set-CMTaskSequenceDeploymentType [-AddDetectionClause <DetectionClause[]>]
 [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-ForceScriptDetection32Bit <Boolean>] [-GroupDetectionClauses <String[]>]
 [-InstallationBehaviorType <InstallationBehaviorType>] -InstallTaskSequenceId <String>
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>] [-ProductCode <String>]
 [-RebootBehavior <PostExecutionBehavior>] [-RemoveDetectionClause <String[]>]
 [-RequireUserInteraction <Boolean>] [-ScriptFile <String>] [-ScriptLanguage <ScriptLanguage>]
 [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] -Application <IResultObject>
 -DeploymentTypeName <String> [-NewName <String>] [-PassThru] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Set-CMTaskSequenceDeploymentType [-AddDetectionClause <DetectionClause[]>]
 [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-ForceScriptDetection32Bit <Boolean>] [-GroupDetectionClauses <String[]>]
 [-InstallationBehaviorType <InstallationBehaviorType>] -InstallTaskSequenceId <String>
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>] [-ProductCode <String>]
 [-RebootBehavior <PostExecutionBehavior>] [-RemoveDetectionClause <String[]>]
 [-RequireUserInteraction <Boolean>] [-ScriptFile <String>] [-ScriptLanguage <ScriptLanguage>]
 [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] -ApplicationId <Int32>
 -DeploymentTypeName <String> [-NewName <String>] [-PassThru] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDTValue
```
Set-CMTaskSequenceDeploymentType [-AddDetectionClause <DetectionClause[]>]
 [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-ForceScriptDetection32Bit <Boolean>] [-GroupDetectionClauses <String[]>]
 [-InstallationBehaviorType <InstallationBehaviorType>] -InstallTaskSequenceId <String>
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>] [-ProductCode <String>]
 [-RebootBehavior <PostExecutionBehavior>] [-RemoveDetectionClause <String[]>]
 [-RequireUserInteraction <Boolean>] [-ScriptFile <String>] [-ScriptLanguage <ScriptLanguage>]
 [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UninstallTaskSequenceId <String>]
 [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Applies to version 2006 and later. Configure a task sequence deployment type on an application. For more information, see [Task sequence deployment type](/mem/configmgr/apps/get-started/creating-windows-applications#bkmk_tsdt).

This cmdlet has similar syntax as the MSI deployment type cmdlet [Set-CMMsiDeploymentType](Set-CMMsiDeploymentType.md). The primary differences are the following parameters:

- `-InstallTaskSequenceId <string>` (required): the ID of the task sequence to install the app

- `-UninstallTaskSequenceId <string>` (optional): the ID of the task sequence to uninstall the app

These two parameters relate to the deployment type task sequence options. They replace the `-InstallCommand` and `-UninstallCommand` parameters on the MSI cmdlet.

## EXAMPLES

### Example 1

{{ Add example description here }}

```powershell
{{ Add example code here }}
```

## PARAMETERS

### -AddDetectionClause
{{ Fill AddDetectionClause Description }}

```yaml
Type: DetectionClause[]
Parameter Sets: (All)
Aliases: AddDetectionClauses

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguage

Configure an array of languages that this deployment type supports.

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

Configure an array of requirements for this deployment type.

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

### -Application

Specify an object for the application to configure the deployment type.

```yaml
Type: IResultObject
Parameter Sets: ByAppValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Specify the application ID to configure the deployment type.

```yaml
Type: Int32
Parameter Sets: ByAppId
Aliases: CI_ID, CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName

Specify the application name to configure the deployment type.

```yaml
Type: String
Parameter Sets: ByAppName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment

Specifies an optional description for this deployment type.

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

Specify the name of the deployment type to configure.

```yaml
Type: String
Parameter Sets: ByAppName, ByAppValue, ByAppId
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
Parameter Sets: (All)
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
Type: Boolean
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases: GroupDetectionClausesByLogicalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a deployment type object to target.

```yaml
Type: IResultObject
Parameter Sets: ByDTValue
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

### -NewName

Use this parameter to rename the deployment type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewDeploymentTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
{{ Fill PassThru Description }}

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

### -ProductCode

Specifies the product code in the detection method for the deployment type.

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

### -RemoveDetectionClause
{{ Fill RemoveDetectionClause Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveDetectionClauses

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
Type: Boolean
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
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases: ScriptType
Accepted values: PowerShell, VBScript, JavaScript

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptText

Specifies the script to use to detect this deployment type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ScriptContent, Script

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
Aliases: ContentLocation, UninstallId

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
