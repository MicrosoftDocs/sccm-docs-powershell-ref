---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833792
schema: 2.0.0
ms.assetid: 2DB4F947-E8B1-4D2A-A7D0-0DCDA1D8ED53
---

# Add-CMWindowsMobileDeploymentType

## SYNOPSIS
Adds a Windows Mobile cabinet deployment type.

## SYNTAX

### ByAppName (Default)
```
Add-CMWindowsMobileDeploymentType [-EnableUninstall] [-DeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 -ApplicationName <String> [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>]
 [-Comment <String>] -ContentLocation <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Add-CMWindowsMobileDeploymentType [-EnableUninstall] [-DeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 -ApplicationId <Int32> [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>]
 [-Comment <String>] -ContentLocation <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Add-CMWindowsMobileDeploymentType [-EnableUninstall] [-DeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 -InputObject <IResultObject> [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>]
 [-AddLanguage <String[]>] [-Comment <String>] -ContentLocation <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMWindowsMobileDeploymentType** cmdlet adds a Windows mobile cabinet deployment type to an application.

## EXAMPLES

### Example 1: Add a deployment type using the pipeline
```
PS C:\> Get-CMApplication -Name "Application1" | Add-CMWindowsMobileDeploymentType -DeploymentTypeName "DT4" -ContentLocation "\\Machine\Applications\Cab\CMConfigExplorer\ConfigExplorerSetup.cab" -EnableUninstall -AddLanguage "en-US","zh-CN" -Comment "New Deployment Type"
```

This command gets the application object named Application1 and uses the pipeline operator to pass the object to **Add-CMWindowsMobileDeploymentType**.
**Add-CMWindowsMobileDeploymentType** adds a Windows Mobile cabinet deployment type named DT4 from the specified location in English and Chinese.
Specifying the *EnableUninstall* parameter indicates that the user can uninstall this application.

### Example 2: Add a Windows Mobile cabinet deployment type
```
PS C:\> Add-CMWindowsMobileDeploymentType -ApplicationName "Application1" -DeploymentTypeName "DT4" -ContentLocation "\\Machine\Resources\Applications\Cab\CMConfigExplorer\ConfigExplorerSetup.cab" -EnableUninstall -AddLanguage "en-US","zh-CN" -Comment "New Deployment Type"
```

This command adds the Windows Mobile cabinet deployment type named DT4 from the specified location to the application named Application1 in English and Chinese.
Specifying the *EnableUninstall* parameter indicates that the user can uninstall this application.

## PARAMETERS

### -AddLanguage
Adds an array of languages that this deployment type supports.
Provide the languages in the "languagecode2-country" or "languagecode2" format, for example: en, en-US, ja-JP, zh-CN.

For more information about the CultureInfo.Name Property, see [https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.name.aspx](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.name.aspx).

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

### -ContentLocation
Specifies the path of the content.
The site system server requires permissions to read the content files.

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstallationFileLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeName
Specifies a display name for the deployment type.

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

### -EnableUninstall
Indicates that the user is allowed to uninstall this application.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AllowUserToUninstall, AllowsUsersToUninstallThisContent, EnableUserUninstall

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
Specifies an application object.
To obtain an application object, use the [Get-CMApplication](./Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByAppValue
Aliases: Application

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoveLanguage
Removes an array of existing languages from this deployment type.
Provide the languages in the "languagecode2-country" or "languagecode2" format, for example: en, en-US, ja-JP, zh-CN.

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

[Get-CMApplication](./Get-CMApplication.md)

[Set-CMWindowsMobileDeploymentType](./Set-CMWindowsMobileDeploymentType.md)


