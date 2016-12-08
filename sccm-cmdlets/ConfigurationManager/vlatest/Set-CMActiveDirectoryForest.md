---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833609
schema: 2.0.0
ms.assetid: 4AE8D747-EDC2-486B-ADB3-0CF426C047F1
---

# Set-CMActiveDirectoryForest

## SYNOPSIS
Changes Active Directory forest properties in Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMActiveDirectoryForest -InputObject <IResultObject> [-Description <String>] [-EnableDiscovery <Boolean>]
 [-PublishingPath <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByFQDN
```
Set-CMActiveDirectoryForest -ForestFqdn <String> [-Description <String>] [-EnableDiscovery <Boolean>]
 [-PublishingPath <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMActiveDirectoryForest -Id <UInt32> [-Description <String>] [-EnableDiscovery <Boolean>]
 [-PublishingPath <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMActiveDirectoryForest** cmdlet changes values for an Active Directory forest object in Microsoft System Center Configuration Manager.
You can edit the description, enable or disable discovery, and specify a fully qualified domain name (FQDN) and publishing path.
You can specify an Active Directory forest object by ID or FQDN, or you can supply the Active Directory forest object itself.

Active Directory Forest Discovery requires a global account to discover or publish to untrusted forests.

## EXAMPLES

### Example 1: Change the description of an Active Directory forest
```
PS C:\> Set-CMActiveDirectoryForest -Id "16777217" -Description "AD Forest 01"
```

This command changes the description of an Active Directory forest that has the ID 16777217 to AD Forest 01.

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

### -Description
Specifies a description for an Active Directory forest object.

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

### -EnableDiscovery
Specifies whether to discover Active Directory sites and subnets.
You must configure an Active Directory Forest Discovery method before you use this parameter.
The default value is $False.

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

### -ForestFqdn
Specifies the FQDN of a Configuration Manager object.

```yaml
Type: String
Parameter Sets: SetByFQDN
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies an array of IDs of Configuration Manager objects.
You can find the identifier value in the **ForestID** property of an Active Directory forest.

```yaml
Type: UInt32
Parameter Sets: SetById
Aliases: ForestId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an Active Directory forest object in Configuration Manager.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -PublishingPath
Specifies one or more Configuration Manager sites that publish site information to an Active Directory forest.
You can use a comma-separated list in quotation marks to specify more than one site.

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

[New-CMActiveDirectoryForest](./New-CMActiveDirectoryForest.md)

[Get-CMActiveDirectoryForest](./Get-CMActiveDirectoryForest.md)

[Remove-CMActiveDirectoryForest](./Remove-CMActiveDirectoryForest.md)

[Get-CMActiveDirectorySite](./Get-CMActiveDirectorySite.md)
