---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Get-CMCollectionMember
---

# Get-CMCollectionMember

## SYNOPSIS

Get members of a device or user collection.

## SYNTAX

### ByCollectionName (Default)
```
Get-CMCollectionMember -CollectionName <String> [-Name <String>] [-ResourceId <Int32>] [-SmsId <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionId
```
Get-CMCollectionMember -CollectionId <String> [-Name <String>] [-ResourceId <Int32>] [-SmsId <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollection
```
Get-CMCollectionMember -InputObject <IResultObject> [-Name <String>] [-ResourceId <Int32>] [-SmsId <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get members of a collection. Collections can include devices or users, but not both. When you query a collection, this cmdlet returns objects for all members.

For more information, see [Introduction to collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a member of a collection by using the pipeline operator

This command first uses the **Get-CMCollection** cmdlet to get the collection object named **UserCol1**. It then uses the pipeline operator to pass the object to **Get-CMCollectionMember**, which gets all members in the collection. Finally, this example uses the **Select-Object** cmdlet to only display the member names.

```powershell
Get-CMCollection -Name "UserCol1" | Get-CMCollectionMember | Select-Object Name
```

### Example 2: Get a member of a collection by name

This command queries the collection **DeviceCol1** for members that have a name beginning with `domain`. The asterisk (`*`) wildcard matches multiple characters. So results can include names such as "domain1" or "domain-controller".

```powershell
Get-CMCollectionMember -CollectionName "DeviceCol1" -Name "domain*"
```

### Example 3: Export collection details to a CSV

This example queries the **XYZ0004B** device collection for a set of properties and stores that in the variable, **$collMem**. The second line converts that data into comma-separated value (CSV) format, and outputs to a file.

```powershell
$collMem = Get-CMCollectionMember -CollectionId "XYZ0004B" | Select-Object Name,Domain,LastLogonUser,DeviceOS,DeviceOSBuild,MACAddress,SerialNumber
$collMem | ConvertTo-Csv -NoTypeInformation | Out-File -FilePath "C:\output\XYZ0004B.csv"
```

## PARAMETERS

### -CollectionId

Specify the ID of a collection to query. For example, `"XYZ0004B"`.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of a collection to query.

```yaml
Type: String
Parameter Sets: ByCollectionName
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

Specify a collection object to query. To get a collection object, use one of the following cmdlets:

- [Get-CMCollection](Get-CMCollection.md)
- [Get-CMDeviceCollection](Get-CMDeviceCollection.md)
- [Get-CMUserCollection](Get-CMUserCollection.md)

You can also use the pipeline operator (`|`) to pass a collection object to **Get-CMCollectionMemeber** on the command line.

```yaml
Type: IResultObject
Parameter Sets: ByCollection
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

To filter the results, specify the name of a resource in the collection. This filter isn't case-sensitive.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ResourceId

To filter the results, specify a resource ID. For example, `16777242`. The cmdlet only returns a record for that resource in the targeted collection.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SmsId

To filter the results, specify the SMSID of a resource. For example, `"GUID:7a186367-7372-4841-889e-ba2e3aad1e85"`. This filter isn't case-sensitive.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Copy-CMCollection](Copy-CMCollection.md)
[Export-CMCollection](Export-CMCollection.md)
[Get-CMCollection](Get-CMCollection.md)
[Get-CMCollectionSetting](Get-CMCollectionSetting.md)
[Import-CMCollection](Import-CMCollection.md)
[Invoke-CMCollectionUpdate](Invoke-CMCollectionUpdate.md)
[New-CMCollection](New-CMCollection.md)
[Remove-CMCollection](Remove-CMCollection.md)
[Set-CMCollection](Set-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)

[Introduction to collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections)
