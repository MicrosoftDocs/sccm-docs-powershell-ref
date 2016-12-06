---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834014
schema: 2.0.0
ms.assetid: 449CA735-B682-4AF9-A35C-6FBBD1D0EE09
---

# Set-CMScriptDeploymentType

## SYNOPSIS
Sets a script installer deployment type.

## SYNTAX

### ByAppName (Default)
```
Set-CMScriptDeploymentType [-ContentLocation <String>] [-EnableBranchCache <Boolean>]
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
Set-CMScriptDeploymentType [-ContentLocation <String>] [-EnableBranchCache <Boolean>]
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
Set-CMScriptDeploymentType [-ContentLocation <String>] [-EnableBranchCache <Boolean>]
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
Set-CMScriptDeploymentType [-ContentLocation <String>] [-EnableBranchCache <Boolean>]
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
The **Set-CMScriptDeploymentType** cmdlet changes the settings for a script installer deployment type.

## EXAMPLES

### Example 1: Modify a script installer deployment type
```
PS C:\> Set-CMScriptDeploymentType -ApplicationName "application01" -DeploymentTypeName "ScriptDT01" -Comment "Script updated to uninstall" -UninstallCommand 'msiexec /x ""\\Machine01\Resources\Applications\MSI\AdvertMSI\AdvertMSI.msi" /q' -ScriptLanguage Powershell -ScriptText "update script text"
```

This command adds an uninstall command to the script installer deployment type named ScriptDT01 for the application named application01.
The command also specifies the language of the script used to detect this deployment type as PowerShell.

### Example 2: Modify a script installer deployment type by using the pipeline
```
PS C:\>Get-CMDeploymentType -ApplicationName "application01" -DeploymentTypeName "ScriptDT02" | Set-CMScriptDeploymentType -Comment "Script updated to uninstall" -UninstallCommand 'msiexec /x ""\\Machine01\Resources\Applications\MSI\AdvertMSI\AdvertMSI.msi" /q' -ScriptLanguage PowerShell -ScriptText "update script text"
```

This command gets the script installer deployment type object named ScriptDT02 for the application named application01 and uses the pipeline operator to pass the object to **Set-CMScriptDeploymentType**.
**Set-CMScriptDeploymentType** adds an uninstall command, and specifies the language of the script used to detect this deployment type as PowerShell.

## PARAMETERS

### -AddLanguage
Specifies an array of languages that the deployment type supports.

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
Specifies an array of requirements for the deployment type.

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
Indicates whether the deployment type saves content in cache indefinitely on the client computer.

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
Specifies a description for the deployment type.

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
Indicates whether clients can use a fallback location provided by a management point.
A fallback location point provides an alternate location for source content when the content for the deployment type is not available on any preferred distribution points.

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
Specifies the path of the content.
The site system server requires permission to read the content files.

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
Specifies the install command line for the Windows Installer package.

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
Specifies the installation behavior of the deployment type.
Valid values are: 

- InstallForSystem
- InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser
- InstallForUser

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

[Add-CMScriptDeploymentType](./Add-CMScriptDeploymentType.md)

[Get-CMApplication](./Get-CMApplication.md)

[Get-CMDeploymentType](./Get-CMDeploymentType.md)


