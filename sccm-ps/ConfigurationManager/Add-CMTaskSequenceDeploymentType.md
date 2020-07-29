---
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Add-CMTaskSequenceDeploymentType

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByAppName (Default)
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -ApplicationName <String> [-DeploymentTypeName <String>] [-EstimatedRuntimeMins <Int32>]
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>] [-ProductCode <String>]
 [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UserInteractionMode <UserInteractionMode>] [-InstallationBehaviorType <InstallationBehaviorType>]
 [-RebootBehavior <PostExecutionBehavior>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppIdDetectionClause
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -AddDetectionClause <DetectionClause[]> [-GroupDetectionClauses <String[]>]
 [-DetectionClauseConnector <Hashtable[]>] -ApplicationId <Int32> -DeploymentTypeName <String>
 [-EstimatedRuntimeMins <Int32>] [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UserInteractionMode <UserInteractionMode>] [-InstallationBehaviorType <InstallationBehaviorType>]
 [-RebootBehavior <PostExecutionBehavior>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppNameDetectionClause
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -AddDetectionClause <DetectionClause[]> [-GroupDetectionClauses <String[]>]
 [-DetectionClauseConnector <Hashtable[]>] -ApplicationName <String> -DeploymentTypeName <String>
 [-EstimatedRuntimeMins <Int32>] [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UserInteractionMode <UserInteractionMode>] [-InstallationBehaviorType <InstallationBehaviorType>]
 [-RebootBehavior <PostExecutionBehavior>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValueDetectionClause
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -AddDetectionClause <DetectionClause[]> [-GroupDetectionClauses <String[]>]
 [-DetectionClauseConnector <Hashtable[]>] -InputObject <IResultObject> -DeploymentTypeName <String>
 [-EstimatedRuntimeMins <Int32>] [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UserInteractionMode <UserInteractionMode>] [-InstallationBehaviorType <InstallationBehaviorType>]
 [-RebootBehavior <PostExecutionBehavior>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppIdScript
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -ApplicationId <Int32> -DeploymentTypeName <String> [-EstimatedRuntimeMins <Int32>]
 [-ForceScriptDetection32Bit] [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RequireUserInteraction] -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-ScriptFile <String>]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UserInteractionMode <UserInteractionMode>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -ApplicationId <Int32> [-DeploymentTypeName <String>] [-EstimatedRuntimeMins <Int32>]
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>] [-ProductCode <String>]
 [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UserInteractionMode <UserInteractionMode>] [-InstallationBehaviorType <InstallationBehaviorType>]
 [-RebootBehavior <PostExecutionBehavior>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppNameScript
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -ApplicationName <String> -DeploymentTypeName <String> [-EstimatedRuntimeMins <Int32>]
 [-ForceScriptDetection32Bit] [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RequireUserInteraction] -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-ScriptFile <String>]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UserInteractionMode <UserInteractionMode>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValueScript
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -InputObject <IResultObject> -DeploymentTypeName <String> [-EstimatedRuntimeMins <Int32>]
 [-ForceScriptDetection32Bit] [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>]
 [-RequireUserInteraction] -ScriptLanguage <ScriptLanguage> [-ScriptText <String>] [-ScriptFile <String>]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-UserInteractionMode <UserInteractionMode>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Add-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 -InputObject <IResultObject> [-DeploymentTypeName <String>] [-EstimatedRuntimeMins <Int32>]
 [-LogonRequirementType <LogonRequirementType>] [-MaximumRuntimeMins <Int32>] [-ProductCode <String>]
 [-RequireUserInteraction] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-UserInteractionMode <UserInteractionMode>] [-InstallationBehaviorType <InstallationBehaviorType>]
 [-RebootBehavior <PostExecutionBehavior>] [-AddRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

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
{{ Fill AddLanguage Description }}

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
{{ Fill AddRequirement Description }}

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
{{ Fill ApplicationId Description }}

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
{{ Fill ApplicationName Description }}

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
{{ Fill Comment Description }}

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
{{ Fill DeploymentTypeName Description }}

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
{{ Fill EstimatedRuntimeMins Description }}

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
{{ Fill Force Description }}

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
{{ Fill ForceScriptDetection32Bit Description }}

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
{{ Fill InputObject Description }}

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
{{ Fill InstallationBehaviorType Description }}

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
{{ Fill InstallTaskSequenceId Description }}

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
{{ Fill LogonRequirementType Description }}

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
{{ Fill MaximumRuntimeMins Description }}

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
{{ Fill ProductCode Description }}

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
{{ Fill RebootBehavior Description }}

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
{{ Fill RemoveLanguage Description }}

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
{{ Fill RemoveRequirement Description }}

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
{{ Fill RequireUserInteraction Description }}

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
{{ Fill ScriptFile Description }}

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
{{ Fill ScriptLanguage Description }}

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
{{ Fill ScriptText Description }}

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
{{ Fill SlowNetworkDeploymentMode Description }}

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
{{ Fill UninstallTaskSequenceId Description }}

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
{{ Fill UserInteractionMode Description }}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
