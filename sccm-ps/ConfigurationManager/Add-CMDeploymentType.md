---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: D23CE672-3835-40FA-8907-5C2DB50D1C62
online version: https://go.microsoft.com/fwlink/?linkid=833626
schema: 2.0.0
---

# Add-CMDeploymentType

## SYNOPSIS
Adds a deployment type for a Configuration Manager deployment application. This cmdlet is deprecated.

## SYNTAX

### AddDeploymentTypeByMsiInstallerAuto (Default)
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>]
 [-EnableContentLocationFallback <Boolean>] [-InputObject <IResultObject>] [-ApplicationName <String>]
 [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>] [-ForceForUnknownPublisher <Boolean>]
 [-InstallationBehaviorType <InstallationBehaviorType>] -ContentLocation <String>
 [-InstallationProgram <String>] [-Language <String[]>] [-MsiInstaller]
 [-OnSlowNetworkMode <ContentHandlingMode>] [-Force32BitInstaller <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByAndroidInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-AndroidInstaller]
 [-InputObject <IResultObject>] [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile]
 [-DeploymentTypeName <String>] [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String>
 [-Language <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AddDeploymentTypeByAppV5xInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>]
 [-EnableContentLocationFallback <Boolean>] [-AppV5xInstaller] [-InputObject <IResultObject>]
 [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String> [-Language <String[]>]
 [-OnFastNetworkMode <OnFastNetworkMode>] [-OnSlowNetworkMode <ContentHandlingMode>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByAppvInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>]
 [-EnableContentLocationFallback <Boolean>] [-InputObject <IResultObject>] [-ApplicationName <String>]
 [-AppvInstaller] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String> [-Language <String[]>]
 [-OnFastNetworkMode <OnFastNetworkMode>] [-OnSlowNetworkMode <ContentHandlingMode>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByIosAppStoreInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String> [-IosAppStoreInstaller] [-Language <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByIosInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String> [-IosInstaller] [-Language <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByMacInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String> [-Language <String[]>] [-MacInstaller]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByScriptInstallerManual
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-EnableBranchCache <Boolean>]
 [-EnableContentLocationFallback <Boolean>] [-InputObject <IResultObject>] [-ApplicationName <String>]
 -DeploymentTypeName <String> [-DetectDeploymentTypeByCustomScript] [-EstimatedInstallationTimeMins <Int32>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-ContentLocation <String>]
 -InstallationProgram <String> [-InstallationProgramVisibility <UserInteractionMode>]
 [-InstallationStartIn <String>] [-Language <String[]>] [-LogonRequirementType <LogonRequirementType>]
 [-ManualSpecifyDeploymentType] [-MaximumAllowedRunTimeMins <Int32>] [-OnSlowNetworkMode <ContentHandlingMode>]
 [-PersistContentInClientCache <Boolean>] [-RequireUserInteraction <Boolean>] [-Force32BitInstaller <Boolean>]
 [-Force32BitDetectionScript <Boolean>] -ScriptContent <String> [-ScriptInstaller] -ScriptType <ScriptLanguage>
 [-UninstallProgram <String>] [-UninstallStartIn <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByWebAppInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 -ContentLocation <String> [-Language <String[]>] [-WebAppInstaller] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByWindows8AppInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>]
 [-EnableContentLocationFallback <Boolean>] [-InputObject <IResultObject>] [-ApplicationName <String>]
 [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>] [-ForceForUnknownPublisher <Boolean>]
 -ContentLocation <String> [-Language <String[]>] [-OnSlowNetworkMode <ContentHandlingMode>]
 [-TriggerVpn <Boolean>] [-Windows8AppInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByWindowsStoreInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] -ApplicationNameInWindowsStore <String> [-AutoIdentifyFromInstallationFile]
 [-DeploymentTypeName <String>] [-ForceForUnknownPublisher <Boolean>] [-Language <String[]>]
 -RemoteComputerName <String> [-WindowsStoreInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByWinPhone8InstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String> [-Language <String[]>]
 [-WindowsPhone8Installer] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AddDeploymentTypeByWinPhoneStoreInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String> [-Language <String[]>]
 [-WindowsPhoneStoreInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AddDeploymentTypeByWMInstaller
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>]
 [-EnableUserUninstall <Boolean>] [-InputObject <IResultObject>] [-ApplicationName <String>]
 [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>] [-ForceForUnknownPublisher <Boolean>]
 -ContentLocation <String> [-Language <String[]>] [-ManualSpecifyDeploymentType] [-PfxFileLocation <String>]
 [-PfxFilePassword <SecureString>] [-SignContentFile <Boolean>] [-SignedContentFileLocation <String>]
 [-WMInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByMobileMsiInstallerAuto
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile] [-DeploymentTypeName <String>]
 [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String> [-InstallationCommandLine <String>]
 [-Language <String[]>] [-MobileMsiInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByMobileMsiInstallerManual
```
Add-CMDeploymentType [-AddRequirement <Rule[]>] [-AdministratorComment <String>] [-InputObject <IResultObject>]
 [-ApplicationName <String>] -DeploymentTypeName <String> [-ContentLocation <String>] [-Language <String[]>]
 [-ManualSpecifyDeploymentType] [-MobileMsiInstaller] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeploymentTypeByAndroidGooglePlayInstallerAuto
```
Add-CMDeploymentType [-AdministratorComment <String>] [-AndroidGooglePlayInstaller]
 [-InputObject <IResultObject>] [-ApplicationName <String>] [-AutoIdentifyFromInstallationFile]
 [-DeploymentTypeName <String>] [-ForceForUnknownPublisher <Boolean>] -ContentLocation <String>
 [-Language <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is deprecated.
Use one of the following cmdlets:  [Add-CMAndroidDeploymentType](Add-CMAndroidDeploymentType.md),  [Add-CMAppv5XDeploymentType](Add-CMAppv5XDeploymentType.md),  [Add-CMAppvDeploymentType](Add-CMAppvDeploymentType.md),  [Add-CMGooglePlayDeploymentType](Add-CMGooglePlayDeploymentType.md),  [Add-CMIosAppStoreDeploymentType](Add-CMIosAppStoreDeploymentType.md),  [Add-CMIosDeploymentType](Add-CMIosDeploymentType.md),  [Add-CMMacDeploymentType](Add-CMMacDeploymentType.md),  [Add-CMMobileMsiDeploymentType](Add-CMMobileMsiDeploymentType.md),  [Add-CMMsiDeploymentType](Add-CMMsiDeploymentType.md),  [Add-CMNokiaDeploymentType](Add-CMNokiaDeploymentType.md),  [Add-CMScriptDeploymentType](Add-CMScriptDeploymentType.md),  [Add-CMWebApplicationDeploymentType](Add-CMWebApplicationDeploymentType.md),  [Add-CMWindowsAppxDeploymentType](Add-CMWindowsAppxDeploymentType.md),  [Add-CMWindowsMobileDeploymentType](Add-CMWindowsMobileDeploymentType.md),  [Add-CMWindowsPhoneDeploymentType](Add-CMWindowsPhoneDeploymentType.md),  [Add-CMWindowsPhoneStoreDeploymentType](Add-CMWindowsPhoneStoreDeploymentType.md), or  [Add-CMWindowsStoreDeploymentType](Add-CMWindowsStoreDeploymentType.md).

The **Add-CMDeploymentType** cmdlet adds a deployment type for an application.
A deployment type is contained within an application and contains the information that Microsoft System Center Configuration Manager requires to install software.
A deployment type also contains rules that specify if and how the software is deployed.

## EXAMPLES

### Example 1: Add an Windows Installer deployment type to an application
```
PS C:\>Add-CMDeploymentType -MsiInstaller -ApplicationName "App01d2012" -AutoIdentifyFromIntallationFile -InstallationFileLocation "\\CMCEN\D02\Software\RDCMan.msi" -ForceForUnknownPublisher $True
```

This command adds a Windows Installer deployment type for the application named App01d2012.
The command uses the *AutoIdentifyFromIntallationFile* parameter to extract information about the deployment type from the content file, and specifies the path of the installation package.
The command uses the *ForceForUnknownPublisher* parameter to specify that the deployment type verifies the signature of the content file.

### Example 2: Add a deployment type that uses a script
```
PS C:\>Add-CMDeploymentType -ApplicationName "App02d2012" -MsiInstaller -DeploymentTypeName "Type01" -AdministratorComment "Div A script" -Language Afrikaans,Arabic -InstallationProgram 'msiexec /i "\\atd-dist01\Public\CM\DTeam\FeatureData\OSD\Tbreck\Setup1.msi"' -DetectDeploymentTypeByCustomScript -ScriptType VBScript -ScriptContent "1231231" -RunScriptAs32bitProcessOn64bitClient $True
```

This command adds a Windows Installer deployment type for the application named App02d2012.
The command specifies the name Type01 for the deployment type.
The command adds a description for the deployment type, and specifies that the deployment type supports Afrikaans and Arabic.
The command uses the *InstallationProgram* to specify the command line for the Windows Installer.

The command specifies that the deployment type uses a custom script to detect the presence of this deployment type.
The command specifies that the script type is VBScript and specifies the script language that you will use to detect the deployment type.
The command specifies that the deployment type uses Microsoft Windows-32-on-Windows-64 (WOW64) subsystem to run a script on a 64-bit client computer.

## PARAMETERS

### -AddRequirement
```yaml
Type: Rule[]
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByAndroidInstallerAuto, AddDeploymentTypeByAppV5xInstallerAuto, AddDeploymentTypeByAppvInstallerAuto, AddDeploymentTypeByIosAppStoreInstallerAuto, AddDeploymentTypeByIosInstallerAuto, AddDeploymentTypeByMacInstallerAuto, AddDeploymentTypeByScriptInstallerManual, AddDeploymentTypeByWebAppInstallerAuto, AddDeploymentTypeByWindows8AppInstallerAuto, AddDeploymentTypeByWindowsStoreInstallerAuto, AddDeploymentTypeByWinPhone8InstallerAuto, AddDeploymentTypeByWinPhoneStoreInstallerAuto, AddDeploymentTypeByWMInstaller, AddDeploymentTypeByMobileMsiInstallerAuto, AddDeploymentTypeByMobileMsiInstallerManual
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
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AndroidGooglePlayInstaller
```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByAndroidGooglePlayInstallerAuto
Aliases: AndroidDeepLinkInstaller

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AndroidInstaller
Indicates that the deployment type detects application information and deployment types from an app package for Android (.apk) file.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByAndroidInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppV5xInstaller
Indicates that the deployment type detects application information and deployment types from a Application Virtualization (App-V) 5.0  .appv package file.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByAppV5xInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies the name of the application that is associated with the deployment type.

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

### -ApplicationNameInWindowsStore
Specifies the name of the application in the Windows Store.

```yaml
Type: String
Parameter Sets: AddDeploymentTypeByWindowsStoreInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppvInstaller
Indicates that the deployment detects application information and deployment types from an App-V 4.0 manifest .xml file.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByAppvInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoIdentifyFromInstallationFile
Indicates that the deployment type extracts information from the content file.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByAndroidInstallerAuto, AddDeploymentTypeByAppV5xInstallerAuto, AddDeploymentTypeByAppvInstallerAuto, AddDeploymentTypeByIosAppStoreInstallerAuto, AddDeploymentTypeByIosInstallerAuto, AddDeploymentTypeByMacInstallerAuto, AddDeploymentTypeByWebAppInstallerAuto, AddDeploymentTypeByWindows8AppInstallerAuto, AddDeploymentTypeByWindowsStoreInstallerAuto, AddDeploymentTypeByWinPhone8InstallerAuto, AddDeploymentTypeByWinPhoneStoreInstallerAuto, AddDeploymentTypeByWMInstaller, AddDeploymentTypeByMobileMsiInstallerAuto, AddDeploymentTypeByAndroidGooglePlayInstallerAuto
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
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByAndroidInstallerAuto, AddDeploymentTypeByAppV5xInstallerAuto, AddDeploymentTypeByAppvInstallerAuto, AddDeploymentTypeByIosAppStoreInstallerAuto, AddDeploymentTypeByIosInstallerAuto, AddDeploymentTypeByMacInstallerAuto, AddDeploymentTypeByWebAppInstallerAuto, AddDeploymentTypeByWindows8AppInstallerAuto, AddDeploymentTypeByWinPhone8InstallerAuto, AddDeploymentTypeByWinPhoneStoreInstallerAuto, AddDeploymentTypeByWMInstaller, AddDeploymentTypeByMobileMsiInstallerAuto, AddDeploymentTypeByAndroidGooglePlayInstallerAuto
Aliases: InstallationFileLocation, WebAppUrl

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AddDeploymentTypeByScriptInstallerManual, AddDeploymentTypeByMobileMsiInstallerManual
Aliases: InstallationFileLocation, WebAppUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeName
Specifies the name of a deployment type.

```yaml
Type: String
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByAndroidInstallerAuto, AddDeploymentTypeByAppV5xInstallerAuto, AddDeploymentTypeByAppvInstallerAuto, AddDeploymentTypeByIosAppStoreInstallerAuto, AddDeploymentTypeByIosInstallerAuto, AddDeploymentTypeByMacInstallerAuto, AddDeploymentTypeByWebAppInstallerAuto, AddDeploymentTypeByWindows8AppInstallerAuto, AddDeploymentTypeByWindowsStoreInstallerAuto, AddDeploymentTypeByWinPhone8InstallerAuto, AddDeploymentTypeByWinPhoneStoreInstallerAuto, AddDeploymentTypeByWMInstaller, AddDeploymentTypeByMobileMsiInstallerAuto, AddDeploymentTypeByAndroidGooglePlayInstallerAuto
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AddDeploymentTypeByScriptInstallerManual, AddDeploymentTypeByMobileMsiInstallerManual
Aliases: 

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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
Aliases: 

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
```yaml
Type: Boolean
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByAppV5xInstallerAuto, AddDeploymentTypeByAppvInstallerAuto, AddDeploymentTypeByScriptInstallerManual, AddDeploymentTypeByWindows8AppInstallerAuto
Aliases: AllowClientsToUseFallbackSourceLocationForContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUserUninstall
```yaml
Type: Boolean
Parameter Sets: AddDeploymentTypeByWMInstaller
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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByScriptInstallerManual
Aliases: RunInstallationProgramAs32BitProcessOn64BitClient

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceForUnknownPublisher
Indicates whether the deployment type requires file signature verification.

```yaml
Type: Boolean
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByAndroidInstallerAuto, AddDeploymentTypeByAppV5xInstallerAuto, AddDeploymentTypeByAppvInstallerAuto, AddDeploymentTypeByIosAppStoreInstallerAuto, AddDeploymentTypeByIosInstallerAuto, AddDeploymentTypeByMacInstallerAuto, AddDeploymentTypeByWindows8AppInstallerAuto, AddDeploymentTypeByWindowsStoreInstallerAuto, AddDeploymentTypeByWinPhone8InstallerAuto, AddDeploymentTypeByWinPhoneStoreInstallerAuto, AddDeploymentTypeByWMInstaller, AddDeploymentTypeByMobileMsiInstallerAuto, AddDeploymentTypeByAndroidGooglePlayInstallerAuto
Aliases: 

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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: Application

Required: False
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
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByMobileMsiInstallerAuto
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationProgram
Specifies the command line for the Windows Installer package.

```yaml
Type: String
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
Aliases: 

Required: True
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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IosAppStoreInstaller
```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByIosAppStoreInstallerAuto
Aliases: IosDeepLinkInstaller

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IosInstaller
Indicates that the deployment type detects application information and deployment types from an app package for iOS (.ipa) file.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByIosInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Language
Specifies an array of languages that the deployment type supports.

```yaml
Type: String[]
Parameter Sets: (All)
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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByMacInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManualSpecifyDeploymentType
Do not use.
Configuration Manager does not currently use this parameter.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByScriptInstallerManual, AddDeploymentTypeByWMInstaller, AddDeploymentTypeByMobileMsiInstallerManual
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumAllowedRunTimeMins
```yaml
Type: Int32
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByMobileMsiInstallerAuto, AddDeploymentTypeByMobileMsiInstallerManual
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MsiInstaller
Indicates that the deployment type detects application information and deployment types from a Windows Installer (.msi) file.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnFastNetworkMode
Specifies the installation behavior of the deployment type on a fast network.
The acceptable values for this parameter are:

- RunFromNetwork
- RunLocal

```yaml
Type: OnFastNetworkMode
Parameter Sets: AddDeploymentTypeByAppV5xInstallerAuto, AddDeploymentTypeByAppvInstallerAuto
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
Parameter Sets: AddDeploymentTypeByMsiInstallerAuto, AddDeploymentTypeByAppV5xInstallerAuto, AddDeploymentTypeByAppvInstallerAuto, AddDeploymentTypeByScriptInstallerManual, AddDeploymentTypeByWindows8AppInstallerAuto
Aliases: 
Accepted values: DoNothing, Download, DownloadContentForStreaming

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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfxFileLocation
Specifies the path of the Personal Information Exchange (PFX) file.

```yaml
Type: String
Parameter Sets: AddDeploymentTypeByWMInstaller
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfxFilePassword
Specifies the password, as a secure string, for the PFX file.

```yaml
Type: SecureString
Parameter Sets: AddDeploymentTypeByWMInstaller
Aliases: 

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
Parameter Sets: AddDeploymentTypeByWindowsStoreInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireUserInteraction
```yaml
Type: Boolean
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptInstaller
Indicates that the deployment type uses a script to detect the presence of this deployment type.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptType
Specifies the script language that you want to use to detect the deployment type.

```yaml
Type: ScriptLanguage
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
Aliases: 
Accepted values: PowerShell, VBScript, JavaScript

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignContentFile
Indicates whether the deployment type requires a signed content file.

```yaml
Type: Boolean
Parameter Sets: AddDeploymentTypeByWMInstaller
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignedContentFileLocation
Specifies the path of the signed content file.

```yaml
Type: String
Parameter Sets: AddDeploymentTypeByWMInstaller
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
Parameter Sets: AddDeploymentTypeByWindows8AppInstallerAuto
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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
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
Parameter Sets: AddDeploymentTypeByScriptInstallerManual
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WMInstaller
Indicates that the deployment type detects application information and deployment types from a Windows Mobile cabinet (.cab) file.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByWMInstaller
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebAppInstaller
Indicates that this cmdlet uses a web application installer for the deployment.

```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByWebAppInstallerAuto
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
Parameter Sets: AddDeploymentTypeByWindows8AppInstallerAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsPhone8Installer
```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByWinPhone8InstallerAuto
Aliases: WinPhone8Installer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsPhoneStoreInstaller
```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByWinPhoneStoreInstallerAuto
Aliases: WinPhone8DeeplinkInstaller, WindowsPhone8StoreInstaller

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsStoreInstaller
```yaml
Type: SwitchParameter
Parameter Sets: AddDeploymentTypeByWindowsStoreInstallerAuto
Aliases: DeeplinkInstaller

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

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Remove-CMDeploymentType](Remove-CMDeploymentType.md)

[Set-CMDeploymentType](Set-CMDeploymentType.md)
