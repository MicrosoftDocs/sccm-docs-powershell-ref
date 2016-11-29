---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833578
schema: 2.0.0
ms.assetid: 4307DB22-0478-43D2-BA84-8CCE3B86A9BA
---

# Resume-CMApplication

## SYNOPSIS
Resumes a suspended application.

## SYNTAX

### SearchByValueMandatory (Default)
```
Resume-CMApplication -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Resume-CMApplication [-Name] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Resume-CMApplication [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Resume-CMApplication** cmdlet resumes an application that was suspended using the Suspend-CMApplication cmdlet.
After a suspended application has been resumed, clients can again download the application.

## EXAMPLES

### Example 1: Get an application and resume it
```
PS C:\> Get-CMApplication -Name "Application01" | Resume-CMApplication
```

This command gets the application object named Application01 and uses the pipeline operator to pass the object to **Resume-CMApplication**, which resumes the application.

### Example 2: Resume an application
```
PS C:\> Resume-CMApplication -Name "Application01"
```

This command resumes the application named Application01.

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
To get an application object, use the Get-CMApplication cmdlet.

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
Specifies the name of the application.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

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

[Set-CMApplication](./Set-CMApplication.md)

[Suspend-CMApplication](./Suspend-CMApplication.md)


