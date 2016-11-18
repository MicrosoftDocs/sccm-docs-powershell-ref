---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 8DADA85C-4A7E-4495-8A2F-26F6E7E0D47F
---

# Set-CMMsiDeploymentType

## SYNOPSIS
Sets a Windows Installer deployment type.

## SYNTAX

### ByAppName (Default)
```
Set-CMMsiDeploymentType [-ContentLocation <String>] [-EnableBranchCache <Boolean>]
 [-EstimatedRuntimeMins <Int32>] [-InstallCommand <String>] [-UninstallCommand <String>]
 [-UserInteractionMode <UserInteractionMode>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-CacheContent <Boolean>] [-RequireUserInteraction <Boolean>]
 [-ContentFallback <Boolean>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-InstallWorkingDirectory <String>] [-UninstallWorkingDirectory <String>] [-Force32Bit <Boolean>]
 [-ProductCode <String>] [-ScriptText <String>] [-ForceScriptDetection32Bit <Boolean>]
 [-ScriptLanguage <ScriptLanguage>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-AddRequirement <Rule[]>] -ApplicationName <String>
 -DeploymentTypeName <String> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Set-CMMsiDeploymentType [-ContentLocation <String>] [-EnableBranchCache <Boolean>]
 [-EstimatedRuntimeMins <Int32>] [-InstallCommand <String>] [-UninstallCommand <String>]
 [-UserInteractionMode <UserInteractionMode>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-CacheContent <Boolean>] [-RequireUserInteraction <Boolean>]
 [-ContentFallback <Boolean>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-InstallWorkingDirectory <String>] [-UninstallWorkingDirectory <String>] [-Force32Bit <Boolean>]
 [-ProductCode <String>] [-ScriptText <String>] [-ForceScriptDetection32Bit <Boolean>]
 [-ScriptLanguage <ScriptLanguage>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-AddRequirement <Rule[]>] -ApplicationId <Int32>
 -DeploymentTypeName <String> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Set-CMMsiDeploymentType [-ContentLocation <String>] [-EnableBranchCache <Boolean>]
 [-EstimatedRuntimeMins <Int32>] [-InstallCommand <String>] [-UninstallCommand <String>]
 [-UserInteractionMode <UserInteractionMode>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-CacheContent <Boolean>] [-RequireUserInteraction <Boolean>]
 [-ContentFallback <Boolean>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-InstallWorkingDirectory <String>] [-UninstallWorkingDirectory <String>] [-Force32Bit <Boolean>]
 [-ProductCode <String>] [-ScriptText <String>] [-ForceScriptDetection32Bit <Boolean>]
 [-ScriptLanguage <ScriptLanguage>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-AddRequirement <Rule[]>] -DeploymentTypeName <String>
 -Application <IResultObject> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDTValue
```
Set-CMMsiDeploymentType [-ContentLocation <String>] [-EnableBranchCache <Boolean>]
 [-EstimatedRuntimeMins <Int32>] [-InstallCommand <String>] [-UninstallCommand <String>]
 [-UserInteractionMode <UserInteractionMode>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-CacheContent <Boolean>] [-RequireUserInteraction <Boolean>]
 [-ContentFallback <Boolean>] [-SlowNetworkDeploymentMode <ContentHandlingMode>]
 [-InstallWorkingDirectory <String>] [-UninstallWorkingDirectory <String>] [-Force32Bit <Boolean>]
 [-ProductCode <String>] [-ScriptText <String>] [-ForceScriptDetection32Bit <Boolean>]
 [-ScriptLanguage <ScriptLanguage>] [-SourceUpdateProductCode <String>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-AddRequirement <Rule[]>] -InputObject <IResultObject>
 [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMMsiDeploymentType** cmdlet changes the settings for a Windows Installer deployment type.

## EXAMPLES

### Example 1: Modify a Windows Installer deployment type
```
PS C:\>Set-CMMSiDeploymentType -ApplicationName "testMsi" -DeploymentTypeName "DTMsi" -NewName "DTMsi_Updated" -AddLanguage "en-US","zh-CN" -Comment "New Deployment Type-updated" -EstimatedRuntimeMins 14 -LogonRequirementType OnlyWhenNoUserLoggedOn
```

This command changes the name of the Windows Installer deployment type named DTMsi for the application named testMsi to DTMsi_Updated, adds English and Chinese as supported languages, and adds a description.
This command specifies that the installation will take approximately 14 minutes to complete, and will run when no users are logged on.

### Example 2: Modify a Windows Installer deployment type by using the pipeline
```
PS C:\>Get-CMDeploymentType -ApplicationName "testMsi" -DeploymentTypeName "DTMsi_Updated" | Set-CMMsiDeploymentType -NewName "DTMsi" -AddLanguage "en-US","zh-CN" -Comment "New Deployment Type-updated" -EstimatedRuntimeMins 14 -LogonRequirementType OnlyWhenNoUserLoggedOn
```

This command gets the Windows Installer deployment type object named DTMsi_Updated for the application named testMsi and uses the pipeline operator to pass the object to **Set-CMMsiDeploymentType**.
**Set-CMMsiDeploymentType** changes the name of the deployment type to DTMsi, adds English and Chinese as supported languages, and adds a description.
This command specifies that the installation will take approximately 14 minutes to complete, and will run when no users are logged on.

## PARAMETERS

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

### -Application
Specifies an application object that is associated with this deployment type.
To obtain an application object, use the Get-CMApplication cmdlet.

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
Specifies the ID of the application that is associated with this deployment type.

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
Specifies the name of the application that is associated with this deployment type.

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

### -CacheContent
Indicates that the deployment type saves content indefinitely in the cache on the client computer.

```yaml
Type: Boolean
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
Type: Boolean
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
Parameter Sets: (All)
Aliases: 

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

Required: True
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
Indicates that clients that use Windows BranchCache are allowed to download content from an on-premises distribution point.
Content downloads from cloud-based distribution points can always be shared by clients that use Windows BranchCache.

```yaml
Type: Boolean
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
Type: Boolean
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
Specifies a deployment type object.
To obtain a deployment type object, use the Get-CMDeploymentType cmdlet.

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

### -InstallCommand
Specifies the command to use to install the Windows Installer package from the command line.

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstallationProgram

Required: False
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

### -NewName
Specifies a new name for this deployment type.

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
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -ScriptLanguage
Specifies the script language that detects the deployment type.
The acceptable values for this parameter are:

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMMobileMsiDeploymentType](./Add-CMMobileMsiDeploymentType.md)

[Get-CMApplication](./Get-CMApplication.md)

[Get-CMDeploymentType](./Get-CMDeploymentType.md)


