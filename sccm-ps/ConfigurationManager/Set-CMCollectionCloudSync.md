---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/01/2022
schema: 2.0.0
title: Set-CMCollectionCloudSync
---

# Set-CMCollectionCloudSync

## SYNOPSIS

Configure collection membership synchronization to Microsoft Entra groups for a device or user collection. For more information, see [How to synchronize collection members to Microsoft Entra groups](/mem/configmgr/core/clients/manage/collections/synchronize-collections-aad-group)

## SYNTAX

### SetByValue (Default)
```
Set-CMCollectionCloudSync -InputObject <IResultObject#SMS_Collection> [-AddGroupName <string[]>]
[-EnableAssignEndpointSecurityPolicy <bool>] [-RemoveGroupName <string[]>] [-TenantId <string>]
[-TenantName <string>] [-TenantObject <IResultObject#SMS_AAD_Tenant_Ex>] [-DisableWildcardHandling] [-ForceWildcardHandling]
[-WhatIf] [-Confirm]  [<CommonParameters>]
```

### SetById
```
Set-CMCollectionCloudSync -Id <string> [-AddGroupName <string[]>] [-EnableAssignEndpointSecurityPolicy <bool>]
[-RemoveGroupName <string[]>] [-TenantId <string>] [-TenantName <string>] [-TenantObject <IResultObject#SMS_AAD_Tenant_Ex>]
[-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
[<CommonParameters>]
```

### SetByName
```
Set-CMCollectionCloudSync -Name <string> [-AddGroupName <string[]>] [-EnableAssignEndpointSecurityPolicy <bool>]
[-RemoveGroupName <string[]>] [-TenantId <string>] [-TenantName <string>] [-TenantObject <IResultObject#SMS_AAD_Tenant_Ex>]
[-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
[<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure collection membership synchronization to Microsoft Entra groups for a device or user collection.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Enable a collection to synchronize members to Microsoft Entra group

The first command gets the collection object named **testUserCollection** and stores it in the **$userCollection** variable.
The second command gets the Microsoft Entra tenant named **contoso** and stores it in the **$AADTenant** variable.
The third command enables the synchronization of the collection with Microsoft Entra group named **testUserGroup** belonging to tenant name "contoso"

```powershell
$userCollection = Get-CMCollection -Name "testUserCollection"
$AADTenant = Get-CMAADTenant -Name "contoso"
Set-CMCollectionCloudSync -InputObject $userCollection -AddGroupName "testUserGroup" -EnableAssignEndpointSecurityPolicy $true -TenantObject $AADTenant

```

### Example 2: Remove collection synchronization with Microsoft Entra group

The first command gets the collection object named **testUserCollection** and stores it in the **$userCollection** variable.
The second command removes the synchronization of the collection with Microsoft Entra group named **testUserGroup** belonging to tenant name "contoso", which is passed as value for -TenantName parameter. Alternatively -TenantId parameter can also be used.

```powershell
$userCollection = Get-CMCollection -Name "testUserCollection"
Set-CMCollectionCloudSync -InputObject $userCollection -RemoveGroupName "testUserGroup" -EnableAssignEndpointSecurityPolicy $true -TenantName "contoso"

```

## PARAMETERS

### -AADGroupName

Specify target Microsoft Entra group name with which the collection's members needs to be synchronized.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

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

### -EnableAssignEndpointSecurityPolicy

Use this parameter enable or disable the collection to show up in Intune portal to assign endpoint security policies in Tenant Attach scenario.

```yaml
Type: Boolean
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

Specify the ID of the collection to configure. This value is the **CollectionID** property, for example, `XYZ00012`.

```yaml
Type: String
Parameter Sets: SetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a collection object to configure. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a collection to configure.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveGroupName

Use this parameter to remove synchronization with the specified Microsoft Entra group. 

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId

Specify the ID of the Microsoft Entra tenant. This value is the **TenantId** property, for example, `72f988bf-00ab-11cd-22ef-2d7cd011db00`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantName

Specify the name of the Microsoft Entra tenant, for example, `contoso`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantObject

Specify an object for the Microsoft Entra tenant. To get this object, use the [Get-CMAADTenant](Get-CMAADTenant.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)
[Get-CMAADTenant](Get-CMAADTenant.md)
[How to synchronize collection members to Microsoft Entra groups](/mem/configmgr/core/clients/manage/collections/synchronize-collections-aad-group)
