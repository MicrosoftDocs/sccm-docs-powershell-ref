---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: 8E5ACA39-459C-4767-9577-5C14F1A680E7
online version: https://go.microsoft.com/fwlink/?linkid=834180
schema: 2.0.0
---

# Set-CMWindowsStoreDeploymentType

## SYNOPSIS
Sets a Windows app package (in the Windows Store) deployment type.

## SYNTAX

### ByAppName (Default)
```
Set-CMWindowsStoreDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -ApplicationName <String>
 -DeploymentTypeName <String> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Set-CMWindowsStoreDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -ApplicationId <Int32>
 -DeploymentTypeName <String> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Set-CMWindowsStoreDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -DeploymentTypeName <String>
 -Application <IResultObject> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDTValue
```
Set-CMWindowsStoreDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -InputObject <IResultObject>
 [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMWindowsStoreDeploymentType** cmdlet changes the settings for a Windows app package (in the Windows Store) deployment type.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Change the display name of a deployment type by using the pipeline
```
PS XYZ:\> Get-CMDeploymentType -ApplicationName "Application01" -DeploymentTypeName "DT1" | Set-CMWindowsStoreDeploymentType -NewName "DT1_New" -AddLanguage "en-US","zh-CN" -Comment "Deployment Type updated"
```

This command gets the Windows app package deployment type object named DT1 for the application named Application01 and uses the pipeline operator to pass the object to **Set-CMWindowsStoreDeploymentType**.
**Set-CMWindowsStoreDeploymentType** changes the name of the deployment to DT1_New and adds English and Chinese as supported languages.

### Example 2: Rename a deployment type
```
PS XYZ:\> Set-CMWindowsStoreDeploymentType -ApplicationName "Application01" -DeploymentTypeName "DT1" -NewName "DT1_New" -AddLanguage "en-US","zh-CN" -Comment "Deployment Type updated"
```

This command changes the name of the Windows app package deployment type named DT1 for the application named Application01 to DT1_New, and adds English and Chinese as supported languages.

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
To obtain an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

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
Specifies a deployment type object.
To obtain a deployment type object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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
Returns the current working object.
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
Specifies the URL of an application in the Windows Store.

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

[Add-CMWindowsStoreDeploymentType](Add-CMWindowsStoreDeploymentType.md)

[Get-CMApplication](Get-CMApplication.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)
