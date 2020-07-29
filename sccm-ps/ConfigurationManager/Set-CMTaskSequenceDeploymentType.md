---
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMTaskSequenceDeploymentType

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByAppName (Default)
```
Set-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 [-AddDetectionClause <DetectionClause[]>] [-RemoveDetectionClause <String[]>]
 [-GroupDetectionClauses <String[]>] [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-UserInteractionMode <UserInteractionMode>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction <Boolean>]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-ProductCode <String>] [-ScriptText <String>]
 [-ScriptFile <String>] [-ForceScriptDetection32Bit <Boolean>] [-ScriptLanguage <ScriptLanguage>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-AddRequirement <Rule[]>] -ApplicationName <String> -DeploymentTypeName <String> [-NewName <String>]
 [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru] [-AddLanguage <String[]>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByAppId
```
Set-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 [-AddDetectionClause <DetectionClause[]>] [-RemoveDetectionClause <String[]>]
 [-GroupDetectionClauses <String[]>] [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-UserInteractionMode <UserInteractionMode>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction <Boolean>]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-ProductCode <String>] [-ScriptText <String>]
 [-ScriptFile <String>] [-ForceScriptDetection32Bit <Boolean>] [-ScriptLanguage <ScriptLanguage>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-AddRequirement <Rule[]>] -ApplicationId <Int32> -DeploymentTypeName <String> [-NewName <String>]
 [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru] [-AddLanguage <String[]>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByAppValue
```
Set-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 [-AddDetectionClause <DetectionClause[]>] [-RemoveDetectionClause <String[]>]
 [-GroupDetectionClauses <String[]>] [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-UserInteractionMode <UserInteractionMode>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction <Boolean>]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-ProductCode <String>] [-ScriptText <String>]
 [-ScriptFile <String>] [-ForceScriptDetection32Bit <Boolean>] [-ScriptLanguage <ScriptLanguage>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-AddRequirement <Rule[]>] -DeploymentTypeName <String> -Application <IResultObject> [-NewName <String>]
 [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru] [-AddLanguage <String[]>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDTValue
```
Set-CMTaskSequenceDeploymentType -InstallTaskSequenceId <String> [-UninstallTaskSequenceId <String>]
 [-AddDetectionClause <DetectionClause[]>] [-RemoveDetectionClause <String[]>]
 [-GroupDetectionClauses <String[]>] [-DetectionClauseConnector <Hashtable[]>] [-EstimatedRuntimeMins <Int32>]
 [-UserInteractionMode <UserInteractionMode>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-RequireUserInteraction <Boolean>]
 [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-ProductCode <String>] [-ScriptText <String>]
 [-ScriptFile <String>] [-ForceScriptDetection32Bit <Boolean>] [-ScriptLanguage <ScriptLanguage>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-RebootBehavior <PostExecutionBehavior>]
 [-AddRequirement <Rule[]>] -InputObject <IResultObject> [-NewName <String>] [-RemoveRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
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
Parameter Sets: (All)
Aliases: AddDetectionClauses

Required: False
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

### -Application
{{ Fill Application Description }}

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
{{ Fill ApplicationId Description }}

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
{{ Fill ApplicationName Description }}

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
{{ Fill InputObject Description }}

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

### -NewName
{{ Fill NewName Description }}

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
{{ Fill ProductCode Description }}

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
{{ Fill ScriptFile Description }}

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
{{ Fill ScriptLanguage Description }}

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
{{ Fill ScriptText Description }}

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
Aliases: ContentLocation, UninstallId

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
