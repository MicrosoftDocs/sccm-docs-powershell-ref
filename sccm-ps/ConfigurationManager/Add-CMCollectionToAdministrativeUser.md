---
description: Adds a collection to administrative user.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/27/2019
schema: 2.0.0
title: Add-CMCollectionToAdministrativeUser
---

# Add-CMCollectionToAdministrativeUser

## SYNOPSIS
Adds a collection to administrative user

## SYNTAX

### AddCollectionToAdminByObject_Object (Default)
```
Add-CMCollectionToAdministrativeUser -InputObject <IResultObject> -User <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminById_Id
```
Add-CMCollectionToAdministrativeUser -CollectionId <String> -UserId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminById_Name
```
Add-CMCollectionToAdministrativeUser -CollectionId <String> -UserName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminById_Object
```
Add-CMCollectionToAdministrativeUser -CollectionId <String> -User <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminByName_Id
```
Add-CMCollectionToAdministrativeUser -CollectionName <String> -UserId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminByName_Name
```
Add-CMCollectionToAdministrativeUser -CollectionName <String> -UserName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminByName_Object
```
Add-CMCollectionToAdministrativeUser -CollectionName <String> -User <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminByObject_Id
```
Add-CMCollectionToAdministrativeUser -InputObject <IResultObject> -UserId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminByObject_Name
```
Add-CMCollectionToAdministrativeUser -InputObject <IResultObject> -UserName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -CollectionId
```yaml
Type: String
Parameter Sets: AddCollectionToAdminById_Id, AddCollectionToAdminById_Name, AddCollectionToAdminById_Object
Aliases: UserCollectionId, DeviceCollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
```yaml
Type: String
Parameter Sets: AddCollectionToAdminByName_Id, AddCollectionToAdminByName_Name, AddCollectionToAdminByName_Object
Aliases: UserCollectionName, DeviceCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
```yaml
Type: IResultObject
Parameter Sets: AddCollectionToAdminByObject_Object, AddCollectionToAdminByObject_Id, AddCollectionToAdminByObject_Name
Aliases: Collection, UserCollection, DeviceCollection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -User
```yaml
Type: IResultObject
Parameter Sets: AddCollectionToAdminByObject_Object, AddCollectionToAdminById_Object, AddCollectionToAdminByName_Object
Aliases: AdministrativeUser

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -UserId
```yaml
Type: Int32
Parameter Sets: AddCollectionToAdminById_Id, AddCollectionToAdminByName_Id, AddCollectionToAdminByObject_Id
Aliases: AdministrativeUserId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
```yaml
Type: String
Parameter Sets: AddCollectionToAdminById_Name, AddCollectionToAdminByName_Name, AddCollectionToAdminByObject_Name
Aliases: AdministrativeUserName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
