---
description: Converts an application object.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Convert-CMApplication
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

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an application object and convert it
```
PS XYZ:\> Get-CMApplication -ApplicationName "Application01" | Convert-CMApplication
```

This command gets the application object named Applicaton01 and uses the pipeline operator to pass the object to **Convert-CMApplication**, which converts the application object to an application SDK object.

### Example 2: Get an SDK application object and convert it
```
PS XYZ:\> $SdkApp = ConvertTo-CMApplication -InputObject (Get-CMApplication -ApplicationName "Application01")
PS XYZ:\> Convert-CMApplication -InputObject $SdkApp
```

The first command converts the application named Application01 to an application SDK object and stores the object in the $SdkApp variable.

The second command converts the SDK application object in $SdkApp to an application object.

## PARAMETERS

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

### -InputObject
Specifies an application object or application SDK object.
To obtain an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.
To obtain an application SDK object, use the [ConvertTo-CMApplication](ConvertTo-CMApplication.md) cmdlet.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: IResultObject, Application, ProviderApplicationObject, ApplicationGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Management.Automation.PSObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[ConvertFrom-CMApplication](ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](ConvertTo-CMApplication.md)

[Get-CMApplication](Get-CMApplication.md)

[Export-CMApplication](Export-CMApplication.md)

[Import-CMApplication](Import-CMApplication.md)

[New-CMApplication](New-CMApplication.md)

[Remove-CMApplication](Remove-CMApplication.md)

[Resume-CMApplication](Resume-CMApplication.md)

[Set-CMApplication](Set-CMApplication.md)

[Suspend-CMApplication](Suspend-CMApplication.md)


