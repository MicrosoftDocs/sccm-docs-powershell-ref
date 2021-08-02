---
description: Gets an App-V virtual environment.
external help file: AdminUI.PS.dll-Help.xml
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
The **Get-CMAppVVirtualEnvironment** cmdlet gets one or more Microsoft Application Virtualization (App-V) virtual environment objects from Configuration Manager.
You can specify App-V environments by name or ID.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

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


