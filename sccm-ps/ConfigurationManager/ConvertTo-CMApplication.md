---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: 84CEC68E-3693-4DFD-B853-AC5032E465E6
online version: https://go.microsoft.com/fwlink/?linkid=833884
schema: 2.0.0
---

# ConvertTo-CMApplication

## SYNOPSIS
Converts an application object to an application SDK object.

## SYNTAX

```
ConvertTo-CMApplication -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **ConvertTo-CMApplication** cmdlet converts an application object to an application SDK object.

## EXAMPLES

### Example 1: Get an application and convert it
```
PS C:\> Get-CMApplication -Name "Application01" | ConvertTo-CMApplication
```

This command gets the application object named Application01 and uses the pipeline operator to pass the object to **ConvertTo-CMApplication**, which converts the application object to an application SDK object.

### Example 2: Convert an application
```
PS C:\>ConvertTo-CMApplication -InputObject (Get-CMApplication -Name "Application02")
```

This command gets the application object named Application02 and converts the application object to an application SDK object.

## PARAMETERS

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
To obtain an application object, use the [Get-CMApplication](./Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: Application, DeploymentType

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

[Convert-CMApplication](./Convert-CMApplication.md)

[ConvertFrom-CMApplication](./ConvertFrom-CMApplication.md)

[Get-CMApplication](./Get-CMApplication.md)

[Export-CMApplication](./Export-CMApplication.md)

[Import-CMApplication](./Import-CMApplication.md)

[New-CMApplication](./New-CMApplication.md)

[Remove-CMApplication](./Remove-CMApplication.md)

[Resume-CMApplication](./Resume-CMApplication.md)

[Set-CMApplication](./Set-CMApplication.md)

[Suspend-CMApplication](./Suspend-CMApplication.md)


