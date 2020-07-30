---
description: Removes a collection from administrative user.
external help file: AdminUI.PS.Rba.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMCollectionFromAdministrativeUser
---

# Remove-CMCollectionFromAdministrativeUser

## SYNOPSIS
Removes a collection from administrative user.

## SYNTAX

### RemoveCollectionFromAdminByName_Name (Default)
```
Remove-CMCollectionFromAdministrativeUser -CollectionName <String> -UserName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveCollectionFromAdminById_Id
```
Remove-CMCollectionFromAdministrativeUser -CollectionId <String> -UserId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveCollectionFromAdminById_Name
```
Remove-CMCollectionFromAdministrativeUser -CollectionId <String> -UserName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveCollectionFromAdminById_Object
```
Remove-CMCollectionFromAdministrativeUser -CollectionId <String> -User <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveCollectionFromAdminByName_Id
```
Remove-CMCollectionFromAdministrativeUser -CollectionName <String> -UserId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveCollectionFromAdminByName_Object
```
Remove-CMCollectionFromAdministrativeUser -CollectionName <String> -User <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveCollectionFromAdminByObject_Id
```
Remove-CMCollectionFromAdministrativeUser -InputObject <IResultObject> -UserId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveCollectionFromAdminByObject_Name
```
Remove-CMCollectionFromAdministrativeUser -InputObject <IResultObject> -UserName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveCollectionFromAdminByObject_Object
```
Remove-CMCollectionFromAdministrativeUser -InputObject <IResultObject> -User <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -CollectionId
```yaml
Type: String
Parameter Sets: RemoveCollectionFromAdminById_Id, RemoveCollectionFromAdminById_Name, RemoveCollectionFromAdminById_Object
Aliases: DeviceCollectionId, UserCollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
```yaml
Type: String
Parameter Sets: RemoveCollectionFromAdminByName_Name, RemoveCollectionFromAdminByName_Id, RemoveCollectionFromAdminByName_Object
Aliases: DeviceCollectionName, UserCollectionName

Required: True
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

### -Force
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
```yaml
Type: IResultObject
Parameter Sets: RemoveCollectionFromAdminByObject_Id, RemoveCollectionFromAdminByObject_Name, RemoveCollectionFromAdminByObject_Object
Aliases: DeviceCollection, UserCollection, Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -User
```yaml
Type: IResultObject
Parameter Sets: RemoveCollectionFromAdminById_Object, RemoveCollectionFromAdminByName_Object, RemoveCollectionFromAdminByObject_Object
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
Parameter Sets: RemoveCollectionFromAdminById_Id, RemoveCollectionFromAdminByName_Id, RemoveCollectionFromAdminByObject_Id
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
Parameter Sets: RemoveCollectionFromAdminByName_Name, RemoveCollectionFromAdminById_Name, RemoveCollectionFromAdminByObject_Name
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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
