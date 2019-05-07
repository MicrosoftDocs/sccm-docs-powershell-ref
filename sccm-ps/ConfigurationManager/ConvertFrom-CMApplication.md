---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: 29E31091-FF04-446F-82EC-FD3FFF90B526
online version: https://go.microsoft.com/fwlink/?linkid=833872
schema: 2.0.0
---

# ConvertFrom-CMApplication

## SYNOPSIS
Converts an application SDK object to an application object.

## SYNTAX

```
ConvertFrom-CMApplication -InputObject <Application> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **ConvertFrom-CMApplication** cmdlet converts an application SDK object to an application object.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Convert an application object
```
PS XYZ:\> $SdkApp = Get-CMApplication -Name "Application01" | ConvertTo-CMApplication
PS XYZ:\> $SdkApp | ConvertFrom-CMApplication
```

The first command gets the application object named Application01 and uses the pipeline operator to pass the object to **ConvertTo-CMApplication**, which converts the application object into an application SDK object.
The command then stores the object in the $SdkApp variable.

The second command converts the application SDK object stored in $SdkApp to an application object.

### Example 2: Convert an application object
```
PS XYZ:\> $SdkApp = Get-CMApplication -Name "Application02" | ConvertTo-CMApplication
PS XYZ:\> ConvertFrom-CMApplication -InputObject $SdkApp
```

The first command gets the application object named Application02 and uses the pipeline operator to pass the object to **ConvertTo-CMApplication**, which converts the application object into an application SDK object.
The command then stores the object in the $SdkApp variable.

The second command converts the application SDK object stored in $SdkApp to an application object.

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
Specifies an application SDK object.
To obtain an application object, use the [ConvertTo-CMApplication](ConvertTo-CMApplication.md) cmdlet or the [Convert-CMApplication](Convert-CMApplication.md) cmdlet.

```yaml
Type: Application
Parameter Sets: (All)
Aliases: Application

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

[Convert-CMApplication](Convert-CMApplication.md)

[ConvertTo-CMApplication](ConvertTo-CMApplication.md)

[Get-CMApplication](Get-CMApplication.md)

[Export-CMApplication](Export-CMApplication.md)

[Get-CMApplication](Get-CMApplication.md)

[Import-CMApplication](Import-CMApplication.md)

[Remove-CMApplication](Remove-CMApplication.md)

[Resume-CMApplication](Resume-CMApplication.md)

[Set-CMApplication](Set-CMApplication.md)

[Suspend-CMApplication](Suspend-CMApplication.md)


