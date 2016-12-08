---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834278
schema: 2.0.0
ms.assetid: 66E1A4FB-1FF6-4DA5-8710-1A5AC6BEE641
---

# Unlock-CMObject

## SYNOPSIS
Releases locks to global objects in Configuration Manager.

## SYNTAX

```
Unlock-CMObject [-InputObject] <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Unlock-CMObject** cmdlet releases locks of one or more objects in Microsoft System Center Configuration Manager.
You can use the *InputObject* parameter to specify the input to this cmdlet, or you can pipe the input to this cmdlet.

Serialized Editing of Distributed Objects (SEDO) in System Center Configuration Manager provide a mechanism for assigning and unassigning locks to global System Center Configuration Manager objects in the context of a site, computer and user.
If you want to edit and save a SEDO-enabled object, you must lock the object.
When you obtain the lock, the lock is assigned to you, your computer and the site in which the computer resides.
While the lock is assigned to you, no other user or computer can edit the object until you release the lock.

## EXAMPLES

### Example 1: Unlock a global object
```
PS C:\> $CIObj = Get-CMDriverPackage -Id "CM100042"
PS C:\> Unlock-CMObject $CIObj
```

The first command gets the driver package object that has the ID CM100042, and stores the object in the $CIObj variable.

The second command releases the lock the object in $CIObj.

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

### -InputObject
Specifies an array of Configuration Manager objects output from another cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

[Lock-CMObject](./Lock-CMObject.md)

[Move-CMObject](./Move-CMObject.md)


