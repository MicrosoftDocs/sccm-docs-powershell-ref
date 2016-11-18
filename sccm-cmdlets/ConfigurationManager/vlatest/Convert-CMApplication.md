---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 96352910-63E7-438F-896E-D2C249A62FA8
---

# Convert-CMApplication

## SYNOPSIS
Converts an application object.

## SYNTAX

```
Convert-CMApplication -InputObject <PSObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Convert-CMApplication** cmdlet converts an application object to an application SDK object or an application SDK object to an application object.

## EXAMPLES

### Example 1: Get an application object and convert it
```
PS C:\> Get-CMApplication -ApplicationName "Application01" | Convert-CMApplication
```

This command gets the application object named Applicaton01 and uses the pipeline operator to pass the object to **Convert-CMApplication**, which converts the application object to an application SDK object.

### Example 2: Get an SDK application object and convert it
```
PS C:\> $SdkApp = ConvertTo-CMApplication -InputObject (Get-CMApplication -ApplicationName "Application01")
PS C:\> Convert-CMApplication -InputObject $SdkApp
```

The first command converts the application named Application01 to an application SDK object and stores the object in the $SdkApp variable.

The second command converts the SDK application object in $SdkApp to an application object.

## PARAMETERS

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

### -InputObject
Specifies an application object or application SDK object.
To obtain an application object, use the Get-CMApplication cmdlet.
To obtain an application SDK object, use the ConvertTo-CMApplication cmdlet.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: IResultObject, Application, ProviderApplicationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[ConvertFrom-CMApplication](./ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](./ConvertTo-CMApplication.md)

[Get-CMApplication](./Get-CMApplication.md)

[Export-CMApplication](./Export-CMApplication.md)

[Import-CMApplication](./Import-CMApplication.md)

[New-CMApplication](./New-CMApplication.md)

[Remove-CMApplication](./Remove-CMApplication.md)

[Resume-CMApplication](./Resume-CMApplication.md)

[Set-CMApplication](./Set-CMApplication.md)

[Suspend-CMApplication](./Suspend-CMApplication.md)


