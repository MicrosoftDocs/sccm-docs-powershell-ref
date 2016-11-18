---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 4045C110-CCEF-4E12-B774-0A61D0E62A1B
---

# Add-CMCollectionToAdministrativeUser

## SYNOPSIS

## SYNTAX

### AddCollectionToAdminById_Name
```
Add-CMCollectionToAdministrativeUser -CollectionId <String> -UserName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminById_Id
```
Add-CMCollectionToAdministrativeUser -CollectionId <String> -UserId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminById_Object
```
Add-CMCollectionToAdministrativeUser -CollectionId <String> -User <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminByName_Name
```
Add-CMCollectionToAdministrativeUser -CollectionName <String> -UserName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddCollectionToAdminByName_Id
```
Add-CMCollectionToAdministrativeUser -CollectionName <String> -UserId <Int32> [-DisableWildcardHandling]
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

### AddCollectionToAdminByObject_Object
```
Add-CMCollectionToAdministrativeUser -InputObject <IResultObject> -User <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

### -CollectionId
```yaml
Type: String
Parameter Sets: AddCollectionToAdminById_Name, AddCollectionToAdminById_Id, AddCollectionToAdminById_Object
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
Parameter Sets: AddCollectionToAdminByName_Name, AddCollectionToAdminByName_Id, AddCollectionToAdminByName_Object
Aliases: UserCollectionName, DeviceCollectionName

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
```yaml
Type: IResultObject
Parameter Sets: AddCollectionToAdminByObject_Id, AddCollectionToAdminByObject_Name, AddCollectionToAdminByObject_Object
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
Parameter Sets: AddCollectionToAdminById_Object, AddCollectionToAdminByName_Object, AddCollectionToAdminByObject_Object
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


