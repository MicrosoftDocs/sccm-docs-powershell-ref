---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: 9FD6BC0A-60BE-43DA-9BA2-8555725281EF
online version: https://go.microsoft.com/fwlink/?linkid=833804
schema: 2.0.0
---

# Add-CMWindowsStoreDeploymentType

## SYNOPSIS
Adds a Windows app package (in the Windows Store) deployment type.

## SYNTAX

### ByAppName (Default)
```
Add-CMWindowsStoreDeploymentType -Url <String> [-DeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 -ApplicationName <String> [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByAppId
```
Add-CMWindowsStoreDeploymentType -Url <String> [-DeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 -ApplicationId <Int32> [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByAppValue
```
Add-CMWindowsStoreDeploymentType -Url <String> [-DeploymentTypeName <String>] [-AddRequirement <Rule[]>]
 -InputObject <IResultObject> [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMWindowsStoreDeploymentType** cmdlet adds a Windows app package (in the Windows Store) deployment type to an application.

## EXAMPLES

### Example 1: Add a deployment type by using the pipeline
```
PS C:\> Get-CMApplication -Name "Application1" | Add-CMWindowsStoreDeploymentType -DeploymentTypeName "DT1" -Url "https://www.microsoft.com/store/apps/9wzdncrfjb9s" -Comment "Windows Store Deployment Type" -AddLanguage "en-US","zh-CN"
```

This command gets the application object named Application1 and uses the pipeline operator to pass the object to **Add-CMWindowsStoreDeploymentType**.
**Add-CMWindowsStoreDeploymentType** adds a Windows app package from the specified URL in English and Chinese.

### Example 2: Add a Windows app package deployment type
```
PS C:\> Add-CMWindowsStoreDeploymentType -ApplicationName "Application1" -DeploymentTypeName "DT2" -Url "https://www.microsoft.com/store/apps/9wzdncrfjb9s" -Comment "Windows Store Deployment Type" -AddLanguage "en-US","zh-CN"
```

This command adds the Windows app package deployment type named DT2 from the specified URL to the application named Application1 in English and Chinese.

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
Parameter Sets: (All)
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
Specifies an application object.
To obtain an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

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

### -Url
Specifies the URL of an application in the Windows Store.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContentLocation

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Set-CMWindowsStoreDeploymentType](Set-CMWindowsStoreDeploymentType.md)


