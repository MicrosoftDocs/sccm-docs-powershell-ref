---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833866
schema: 2.0.0
ms.assetid: 7B3F75FB-24E0-47DD-A58A-34C028DC76B4
---

# Set-CMGooglePlayDeploymentType

## SYNOPSIS
Sets a Google Play deployment type.

## SYNTAX

### ByAppName (Default)
```
Set-CMGooglePlayDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -ApplicationName <String>
 -DeploymentTypeName <String> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Set-CMGooglePlayDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -ApplicationId <Int32>
 -DeploymentTypeName <String> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Set-CMGooglePlayDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -DeploymentTypeName <String>
 -Application <IResultObject> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDTValue
```
Set-CMGooglePlayDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -InputObject <IResultObject>
 [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMGooglePlayDeploymentType** changes the settings for a Google Play deployment type.

## EXAMPLES

### Example 1: Change the name and remove a language of the deployment type
```
PS C:\>Set-CMGooglePlayDeploymentType -ApplicationName "TestGooglePlay02" -DeploymentTypeName "DTGooglePlay02" -Url "https://play.google.com/store/apps/details?id=com.microsoft.office.word" -NewName "DTGooglePlay_Updated" -RemoveLanguage "zh-CN" -PassThru -Confirm
```

This command removes Chinese from the deployment type named DTGooglePlay02 for the application named TestGooglePlay02.
The command also renames the deployment type to DTGooglePlay_Updated.
The *PassThru* parameter indicates that an object is returned from this command.

### Example 2: Change the name and remove a language of the deployment type by using the pipeline
```
PS C:\>Get-CMDeploymentType -ApplicationName "TestGooglePlay01" -DeploymentTypeName "DTGooglePlay01" | Set-CMGooglePlayDeploymentType -Url "https://play.google.com/store/apps/details?id=com.microsoft.office.word" -NewName "DTGooglePlay" -RemoveLanguage "zh-CN" -PassThru -Confirm
```

This command gets the deployment type object named DTGooglePlay01 for the application named TestGooglePlay01 and uses the pipeline operator to pass the object to **Set-CMGooglePlayDeploymentType**.
**Set-CMGooglePlayDeployment** type changes the name of the deployment type to DTGooglePlay and removes Chinese from the list of supported languages.
Additionally, the cmdlet sets the URL.
The *PassThru* parameter indicates that an object is returned from this command.

## PARAMETERS

### -AddLanguage
Adds an array of languages that this deployment type supports.
Provide the languages in the "languagecode2-country" or "languagecode2" format, for example: en, en-US, ja-JP, zh-CN.

For more information about the **CultureInfo.Name** property, see [https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.name.aspx](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.name.aspx).

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
To obtain an application object, use the [Get-CMApplication](./Get-CMApplication.md) cmdlet.

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
Specifies a Google Play deployment type object.
To obtain a deployment type object, use the [Get-CMDeploymentType](./Get-CMDeploymentType.md) cmdlet.

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

### -Url
Specifies the URL of an application in Google Play.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContentLocation
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

[Add-CMGooglePlayDeploymentType](./Add-CMGooglePlayDeploymentType.md)

[Get-CMApplication](./Get-CMApplication.md)

[Get-CMDeploymentType](./Get-CMDeploymentType.md)
