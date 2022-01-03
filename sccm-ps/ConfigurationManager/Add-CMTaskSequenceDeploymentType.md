---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/02/2021
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

Specify an array of detection method clauses for this deployment type. To create a detection clause, use one of the following cmdlets:

- [New-CMDetectionClauseDirectory](New-CMDetectionClauseDirectory.md)
- [New-CMDetectionClauseFile](New-CMDetectionClauseFile.md)
- [New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md)
- [New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md)
- [New-CMDetectionClauseWindowsInstaller](New-CMDetectionClauseWindowsInstaller.md)

Save the output of these cmdlets into a variable. Then specify those variables as an array for this parameter. For example, `-AddDetectionClause $clauseFile1,$clauseFile2,$clauseFile3`.

You can also use [Get-CMDeploymentTypeDetectionClause](Get-CMDeploymentTypeDetectionClause.md) to get an existing detection clause from another application.

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

Specify an array of language tags that the deployment type supports. For example, to add **Russian (Russia)**, specify the tag `ru-RU`.

For more information and a list of language tags, see [Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

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

Specify an array of requirement objects for the deployment type. To create a requirement rule object, use one of the following cmdlets:

- [New-CMRequirementRuleActiveDirectorySiteValue](New-CMRequirementRuleActiveDirectorySiteValue.md)
- [New-CMRequirementRuleBooleanValue](New-CMRequirementRuleBooleanValue.md)
- [New-CMRequirementRuleCMSiteValue](New-CMRequirementRuleCMSiteValue.md)
- [New-CMRequirementRuleCommonValue](New-CMRequirementRuleCommonValue.md)
- [New-CMRequirementRuleDeviceOwnershipValue](New-CMRequirementRuleDeviceOwnershipValue.md)
- [New-CMRequirementRuleExistential](New-CMRequirementRuleExistential.md)
- [New-CMRequirementRuleExpression](New-CMRequirementRuleExpression.md)
- [New-CMRequirementRuleFileAttributeValue](New-CMRequirementRuleFileAttributeValue.md)
- [New-CMRequirementRuleFilePermissionValue](New-CMRequirementRuleFilePermissionValue.md)
- [New-CMRequirementRuleFreeDiskSpaceValue](New-CMRequirementRuleFreeDiskSpaceValue.md)
- [New-CMRequirementRuleInputTypeValue](New-CMRequirementRuleInputTypeValue.md)
- [New-CMRequirementRuleOperatingSystemLanguageValue](New-CMRequirementRuleOperatingSystemLanguageValue.md)
- [New-CMRequirementRuleOperatingSystemValue](New-CMRequirementRuleOperatingSystemValue.md)
- [New-CMRequirementRuleOUValue](New-CMRequirementRuleOUValue.md)
- [New-CMRequirementRuleRegistryKeyPermissionValue](New-CMRequirementRuleRegistryKeyPermissionValue.md)
- [New-CMRequirementRuleScreenResolutionValue](New-CMRequirementRuleScreenResolutionValue.md)

Starting in version 2111, you can use the [Get-CMDeploymentTypeRequirement](Get-CMDeploymentTypeRequirement.md) cmdlet to copy rules from another deployment type.

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

Specify the ID of the application for this deployment type.

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

Specify the name of the application for this deployment type.

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

Specify an optional description for the deployment type.

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

Specify a display name for this deployment type.

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

When you use the **GroupDetectionClauses** parameter to group detection clauses, use this parameter to specify the connector.

The following example defines the **OR** connector: `@{"LogicalName"=$clauseFile3.Setting.LogicalName;"Connector"="OR"}`

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

Specify the estimated installation time, in minutes, of this deployment type for the application. Software Center displays this estimate to the user before the application installs.

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

If you use a custom script to detect the presence of this deployment type, set this parameter to `$true` to run the script as a 32-bit process on 64-bit clients.

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

When you configure rules to detect the presence of this deployment type, use this parameter to group clauses. To create a detection clause, use one of the following cmdlets:

- [New-CMDetectionClauseDirectory](New-CMDetectionClauseDirectory.md)
- [New-CMDetectionClauseFile](New-CMDetectionClauseFile.md)
- [New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md)
- [New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md)
- [New-CMDetectionClauseWindowsInstaller](New-CMDetectionClauseWindowsInstaller.md)

Save the output of these cmdlets into a variable. Then use the following format to group clauses: `$clause2.Setting.LogicalName, $clause3.Setting.LogicalName`.

> [!TIP]
> In the Configuration Manager console, when you select the **Group** action, the clauses show parentheses before and after the grouped clauses.

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

Specify an application object to configure. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

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

Specify the installation behavior for this deployment type:

- `InstallForUser`: The client only installs the application for the user to whom you deploy the application.
- `InstallForSystem`: The client installs the application only once. It's available to all users.
- `InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser`: If you deploy the application to a device, the client installs it for all users. If you deploy the application to a user, the client only installs it for that user.

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

The ID of the task sequence to install the app.

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

Specify the requirement for a signed-in user:

- `OnlyWhenNoUserLoggedOn`: Only when no user is signed into Windows.
- `OnlyWhenUserLoggedOn`: Only when a user is signed in. This option is the default.
- `WhetherOrNotUserLoggedOn`: Whether or not a user is signed in.

    > [!NOTE]
    > The value `WhereOrNotUserLoggedOn` is deprecated. It's replaced by `WhetherOrNotUserLoggedOn`.

If you set **InstallationBehaviorType** to `InstallForUser`, then you can't set this parameter.

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

Specify the maximum allowed run time of the deployment program for this application. Set an integer value in minutes.

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

If the application uses Windows Installer technology, specify an MSI product code to set as the detection method. When you use this parameter, it overwrites any existing detection methods.

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

Specify the post-installation behavior:

- `BasedOnExitCode`: Determine behavior based on return codes.

- `NoAction`: No specific action.

- `ProgramReboot`: The software install program might force a device restart.

- `ForceReboot`: Configuration Manager client will force a mandatory device restart.

For more information on these behaviors, see [Create applications in Configuration Manager](/mem/configmgr/apps/deploy-use/create-applications#deployment-type-properties-user-experience-options).

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

Specify an array of supported languages to remove from this deployment type.

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

Specify an array of requirement rules to remove from this deployment type.

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

Set this parameter to `$true` to allow users to view and interact with the deployment type installation.

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

Specify the script file to use to detect this deployment type. Also use the **ScriptLanguage** parameter.

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

If you use the **ScriptFile** or **ScriptText** parameters, use this parameter to specify the script language.

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

Specify the text of a script to detect this deployment type. Also use the **ScriptLanguage** parameter.

For more information, see [About custom script detection methods](/mem/configmgr/apps/deploy-use/create-applications#about-custom-script-detection-methods).

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

When a client uses a distribution point from a neighbor boundary group or the default site boundary group, specify the deployment option:

- `DoNothing`: Don't download content
- `Download`: Download content from the distribution point and run locally

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

Specify the installation program visibility:

- `Normal`: The deployment type runs in the normal mode based on system and program defaults. This mode is the default.
- `Minimized`: The deployment type runs minimized on client devices. Users might see the installation activity in the notification area or taskbar.
- `Maximized`: The deployment type runs maximized on client devices. Users see all installation activity.
- `Hidden`: The deployment type runs hidden on client devices. Users see no installation activity.

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

[Set-CMTaskSequenceDeploymentType](Set-CMTaskSequenceDeploymentType.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Remove-CMDeploymentType](Remove-CMDeploymentType.md)

[Get-CMApplication](Get-CMApplication.md)

[Task sequence deployment type](/mem/configmgr/apps/get-started/creating-windows-applications#bkmk_tsdt)
