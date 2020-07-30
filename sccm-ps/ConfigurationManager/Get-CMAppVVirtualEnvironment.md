---
description: Gets an App-V virtual environment.
external help file: AdminUI.PS.AppModel.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMAppVVirtualEnvironment
---

# Get-CMAppVVirtualEnvironment

## SYNOPSIS
Gets an App-V virtual environment.

## SYNTAX

### SearchByName (Default)
```
Get-CMAppVVirtualEnvironment [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMAppVVirtualEnvironment -Id <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAppVVirtualEnvironment** cmdlet gets one or more Microsoft Application Virtualization (App-V) virtual environment objects from Microsoft System Center Configuration Manager.
You can specify App-V environments by name or ID.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get all virtual environments
```
PS XYZ:\> Get-CMAppVVirtualEnvironment
```

This command gets all App-V virtual environments.

### Example 2: Get virtual environments by using a wildcard
```
PS XYZ:\> Get-CMAppVVirtualEnvironment -Name "T*"
```

This command gets all App-V virtual environments that have names that begin with the letter T.

### Example 3: Get virtual environment by an ID
```
PS XYZ:\> Get-CMAppVVirtualEnvironment -Id "16781806"
```

This command gets an App-V virtual environment that has the ID 16781806.

## PARAMETERS

### -DisableWildcardHandling
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
Specifies an array of IDs of virtual environments.

```yaml
Type: Int32[]
Parameter Sets: SearchById
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of App-V virtual environment objects.
You can use a wildcard.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_VirtualEnvironment

### IResultObject#SMS_VirtualEnvironment

## NOTES

## RELATED LINKS

[New-CMAppVVirtualEnvironment](New-CMAppVVirtualEnvironment.md)

[Remove-CMAppVVirtualEnvironment](Remove-CMAppVVirtualEnvironment.md)

[Set-CMAppVVirtualEnvironment](Set-CMAppVVirtualEnvironment.md)


