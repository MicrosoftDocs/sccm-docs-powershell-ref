---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: CE342BBE-34D9-4CA6-8BAF-FFC302C10282
online version: https://go.microsoft.com/fwlink/?linkid=833700
schema: 2.0.0
---

# Add-CMMacDeploymentType

## SYNOPSIS
Adds a Mac deployment type.

## SYNTAX

### ByAppName (Default)
```
Add-CMMacDeploymentType [-AddDetectionClause <DetectionClause[]>] [-DeploymentTypeName <String>]
 [-AddRequirement <Rule[]>] -ApplicationName <String> [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] -ContentLocation <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Add-CMMacDeploymentType [-AddDetectionClause <DetectionClause[]>] [-DeploymentTypeName <String>]
 [-AddRequirement <Rule[]>] -ApplicationId <Int32> [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>]
 [-AddLanguage <String[]>] [-Comment <String>] -ContentLocation <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Add-CMMacDeploymentType [-AddDetectionClause <DetectionClause[]>] [-DeploymentTypeName <String>]
 [-AddRequirement <Rule[]>] -InputObject <IResultObject> [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] -ContentLocation <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMMacDeploymentType** cmdlet adds a Mac deployment type to an application.

## EXAMPLES

### Example 1: Add a Mac deployment type
```
PS C:\>Add-CMMacDeploymentType -ApplicationName "testMac" -DeploymentTypeName "DTMac" -ContentLocation "\\Server01\Resources\Applications\Mac\Bean.app\Bean.app.cmmac" -Confirm -Comment "create a mac DT" -AddLanguage "en-US","zh-CN"
```

This command adds the Mac deployment type named DTMac from the specified URL to the application named testMac in English and Chinese.
By using the *Confirm* parameter, the user is prompted for confirmation before the cmdlet runs.

### Example 2: Add a Mac deployment type by using the pipeline
```
PS C:\> Get-CMApplication -Name "testMac" | Add-CMMacDeploymentType -DeploymentTypeName "DTMac01" -ContentLocation "\\Server01\Resources\Applications\Mac\Skype.app\Skype.app.cmmac" -WhatIf -Comment "create a mac DT" -AddLanguage "zh-CN"
```

This command gets the application object named testMAC and uses the pipeline operator to pass the object to **Add-CMMacDeploymentType**.
**Add-CMMacDeploymentType** adds a deployment type named DTMac01 from the specified URL in Chinese.
Using the *WhatIf* parameter returns a description of what would happen if you executed the command but does not actually execute the command.

## PARAMETERS

### -AddDetectionClause
 

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

### -ApplicationId
Specifies the ID of the application that is associated with the deployment type.

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
Specifies the name of the application that is associated with the deployment type.

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

[Set-CMMacDeploymentType](Set-CMMacDeploymentType.md)


