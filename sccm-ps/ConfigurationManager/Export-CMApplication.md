---
description: Exports an application.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Export-CMApplication
---

# Export-CMApplication

## SYNOPSIS
Exports an application.

## SYNTAX

### SearchByValueMandatory (Default)
```
Export-CMApplication [-Comment <String>] [-Force] [-IgnoreRelated] -InputObject <IResultObject> [-OmitContent]
 -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Export-CMApplication [-Comment <String>] [-Force] -Id <Int32> [-IgnoreRelated] [-OmitContent] -Path <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Export-CMApplication [-Comment <String>] [-Force] [-IgnoreRelated] -Name <String> [-OmitContent] -Path <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMApplication** cmdlet exports an application to a file.
Specify a file path to the location where you want to export the application.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an application and export it
```
PS XYZ:\> Get-CMApplication "Application01" | Export-CMApplication -Path "C:\test.zip" -IgnoreRelated -OmitContent -Comment "Application export" -Force
```

This command gets the application object named Applicaton01 and uses the pipeline operator to pass the object to **Export-CMApplicaton**.
**Export-CMApplication** exports the application to the path C:\test.zip, omitting related content from the zip file, and not exporting related objects.
Specifying the *Force* parameter indicates that the application is exported without prompting the user.

### Example 2: Export an application
```
PS XYZ:\>Export-CMApplication -Name "Application01" -Path "C:\test.zip" -IgnoreRelated -OmitContent -Comment "Application export"
```

This command exports the application named Application01 to the path C:\test.zip, omitting related content from the zip file, and not exporting related objects.
Specifying the *Force* parameter indicates that the application is exported without prompting the user.

## PARAMETERS

### -Comment
Specifies a comment for the exported application.

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

### -Force
Performs the action without a confirmation message.

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

### -Id
Specifies the ID of the application to export.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreRelated
Indicates that related objects, such as application dependencies, superseded applications, or related categories and global conditions, are not exported.

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
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of the application to export.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OmitContent
Indicates that the cmdlet exports related content to a separate folder in the same location as the .zip file.

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

### -Path
Specifies a path for the package.
The package file has a .zip extension.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FileName, FilePath, ExportFilePath

Required: True
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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[ConvertFrom-CMApplication](ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](ConvertTo-CMApplication.md)

[Get-CMApplication](Get-CMApplication.md)

[Import-CMApplication](Import-CMApplication.md)

[New-CMApplication](New-CMApplication.md)

[Remove-CMApplication](Remove-CMApplication.md)

[Resume-CMApplication](Resume-CMApplication.md)

[Set-CMApplication](Set-CMApplication.md)

[Suspend-CMApplication](Suspend-CMApplication.md)


