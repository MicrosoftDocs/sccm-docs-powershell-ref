---
description: Changes Active Directory forest properties in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMActiveDirectoryForest
---

# Set-CMActiveDirectoryForest

## SYNOPSIS
Changes Active Directory forest properties in Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMActiveDirectoryForest [-AddPublishingSite <IResultObject[]>] [-Description <String>]
 [-EnableDiscovery <Boolean>] -InputObject <IResultObject> [-PassThru] [-Password <SecureString>]
 [-PublishingPath <String>] [-RemovePublishingSite <IResultObject[]>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByFQDN
```
Set-CMActiveDirectoryForest [-AddPublishingSite <IResultObject[]>] [-Description <String>]
 [-EnableDiscovery <Boolean>] -ForestFqdn <String> [-PassThru] [-Password <SecureString>]
 [-PublishingPath <String>] [-RemovePublishingSite <IResultObject[]>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMActiveDirectoryForest [-AddPublishingSite <IResultObject[]>] [-Description <String>]
 [-EnableDiscovery <Boolean>] -Id <UInt32> [-PassThru] [-Password <SecureString>] [-PublishingPath <String>]
 [-RemovePublishingSite <IResultObject[]>] [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMActiveDirectoryForest** cmdlet changes values for an Active Directory forest object in Configuration Manager.
You can edit the description, enable or disable discovery, and specify a fully qualified domain name (FQDN) and publishing path.
You can specify an Active Directory forest object by ID or FQDN, or you can supply the Active Directory forest object itself.

Active Directory Forest Discovery requires a global account to discover or publish to untrusted forests.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the description of an Active Directory forest
```
PS XYZ:\> Set-CMActiveDirectoryForest -Id "16777217" -Description "AD Forest 01"
```

This command changes the description of an Active Directory forest that has the ID 16777217 to AD Forest 01.

## PARAMETERS

### -AddPublishingSite
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddPublishingSites

Required: False
Position: Named
Default value: None
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

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -Password
{{ Fill Password Description }}

```yaml
Type: SecureString
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

### -RemovePublishingSite
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemovePublishingSites

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
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

### IResultObject#SMS_ADForest
## NOTES

## RELATED LINKS

[New-CMActiveDirectoryForest](New-CMActiveDirectoryForest.md)

[Get-CMActiveDirectoryForest](Get-CMActiveDirectoryForest.md)

[Remove-CMActiveDirectoryForest](Remove-CMActiveDirectoryForest.md)

[Get-CMActiveDirectorySite](Get-CMActiveDirectorySite.md)
