---
title: Get-CMGlobalCondition
titleSuffix: Configuration Manager
description: Gets Configuration Manager global condition objects.

ms.date: 01/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Get-CMGlobalCondition

## SYNOPSIS

Gets Configuration Manager global condition objects.

## SYNTAX

### SearchByName (Default)

```powershell
Get-CMGlobalCondition [-Name <String>] [-AsDcmSdkObject] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory

```powershell
Get-CMGlobalCondition -Id <String> [-AsDcmSdkObject] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMGlobalCondition** cmdlet gets global condition objects.
You can pass the results of this cmdlet to the **Set-CMGlobalCondition** cmdlet or the **Remove-CMGlobalCondition** cmdlet.

Microsoft System Center Configuration Manager uses global conditions to represent business or technical conditions.
Global conditions specify how to provide and deploy applications to client devices.

You can get global conditions by name, ID, or security scope.
You can also specify one or more security scope names with either names or IDs.
For instance, you might specify an array of global condition names and specify a security scope to narrow your results.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get a global condition by name

```powershell
PS XYZ:\> Get-CMGlobalCondition -Name "CPU speed"
```

This command gets the global condition named CPU speed.

### Example 2: Get a global condition by id (CI_ID)

```powershell
PS XYZ:\> $test = Get-CMGlobalCondition -Id 16777504
        $test.CI_ID
```

## PARAMETERS

### -AsDcmSdkObject

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

### -Id

Specifies an array of identifiers of global conditions.
This value corresponds to the **CI_ID** property of a global condition object.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies an array of names for global conditions.
This value corresponds to the **LocalizedDisplayName** property of a global condition object.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

- [New-CMGlobalCondition](./Get-CMGlobalCondition.md)
- [Set-CMGlobalCondition](./Set-CMGlobalCondition.md)
- [Remove-CMGlobalCondition](./Remove-CMGlobalCondition.md)
