---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834243
schema: 2.0.0
ms.assetid: 1E63FED9-D574-44F1-B056-7AB5BACFEA24
---

# Suspend-CMApplication

## SYNOPSIS
Suspends an application.

## SYNTAX

### SearchByValueMandatory (Default)
```
Suspend-CMApplication [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Suspend-CMApplication [-Name] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Suspend-CMApplication [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Suspend-CMApplication** cmdlet suspends an application.
Until the application is resumed, users cannot modify or deploy the application.
This action does not affect existing deployments.
When you suspend an application, its status shows as "Retired" in the Configuration Manager console.
To resume an application, use the Resume-CMApplication cmdlet.

## EXAMPLES

### Example 1: Suspend an application by its name
```
PS C:\>Suspend-CMApplication -Name "Application01"
```

This command suspends the application named Application01.

### Example 2: Get an application and suspend it
```
PS C:\>Get-CMApplication -Name "Application01" | Suspend-CMApplication
```

This command gets the application object named Application01 and uses the pipeline operator to pass the object to **Suspend-CMApplication**, which suspends the application.

## PARAMETERS

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

### -Id
Specifies the CI_ID and ModelID properties (the same value) of an application.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an application object.
To obtain an application object, use the Get-CMApplication cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Application

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of the application.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName, ApplicationName

Required: True
Position: 0
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

[Convert-CMApplication](./Convert-CMApplication.md)

[ConvertFrom-CMApplication](./ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](./ConvertTo-CMApplication.md)

[Export-CMApplication](./Export-CMApplication.md)

[Get-CMApplication](./Get-CMApplication.md)

[Import-CMApplication](./Import-CMApplication.md)

[New-CMApplication](./New-CMApplication.md)

[Remove-CMApplication](./Remove-CMApplication.md)

[Resume-CMApplication](./Resume-CMApplication.md)

[Set-CMApplication](./Set-CMApplication.md)


