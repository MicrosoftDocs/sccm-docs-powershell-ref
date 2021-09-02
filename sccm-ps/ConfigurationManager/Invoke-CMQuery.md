---
description: Run a Configuration Manager query.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2020
schema: 2.0.0
title: Invoke-CMQuery
---

# Invoke-CMQuery

## SYNOPSIS

Run a Configuration Manager query.

## SYNTAX

### SearchByValueMandatory (Default)
```
Invoke-CMQuery -InputObject <IResultObject> [-LimitToCollectionId <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMQuery -Id <String> [-LimitToCollectionId <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMQuery [-LimitToCollectionId <String>] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to run a query in the Configuration Manager site. Configuration Manager queries define a WMI Query Language (WQL) expression to get information from the site database based on the criteria you provide. WQL is similar to SQL, but still goes through the SMS Provider instead of directly to the database. So WQL still abides by your role-based access configuration.

When you run a query, the site processes the WQL expression, and returns the results in PowerShell. Depending upon the structure of the WQL statement, the format of the results may vary.

Queries can return most types of Configuration Manager objects, which include computers, sites, collections, applications, and inventory data. For more information, see [Introduction to queries in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-queries).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: View and run a default query

This example first shows the **Get-CMQuery** cmdlet to show the properties of the default query, **This Site and its Subsites**.

It then shows the **Invoke-CMQuery** cmdlet to run the same query and show the results.

```powershell
PS XYZ:\> Get-CMQuery -Id "SMS012"

SmsProviderObjectPath          : SMS_Query.QueryID="SMS012"
Comments                       : This site and all its subsites in the ConfigMgr hierarchy
Expression                     : SELECT SiteCode, SiteName, Version, ServerName FROM sms_siteandsubsites
LimitToCollectionID            :
LocalizedCategoryInstanceNames : {}
Name                           : This Site and its Subsites
QueryID                        : SMS012
ResultAliasNames               : {sms_siteandsubsites, sms_siteandsubsites, sms_siteandsubsites, sms_siteandsubsites}
ResultColumnsNames             : {sms_siteandsubsites.SiteCode, sms_siteandsubsites.SiteName,
                                 sms_siteandsubsites.Version, sms_siteandsubsites.ServerName}
TargetClassName                : sms_siteandsubsites

PS XYZ:\> Invoke-CMQuery -Id "SMS012"

SmsProviderObjectPath : SMS_SiteAndSubsites.SiteCode="XYZ"
ServerName            : cmserver.contoso.com
SiteCode              : XYZ
SiteName              : Production primary site
Version               : 5.00.9043.1000
```

Notice in the output of the **Get-CMQuery** cmdlet that the WQL **Expression** is simple. It selects four attributes from a single class.

Then notice how the output of the **Invoke-CMQuery** cmdlet is a simple table.

### Example 2: View and run a complex query

This example first shows the **Get-CMQuery** cmdlet to show the properties of a custom query.

It then shows the **Invoke-CMQuery** cmdlet to run the same query and show the results.

```powershell
PS XYZ:\> Get-CMQuery -Id "XYZ00002"

SmsProviderObjectPath          : SMS_Query.QueryID="XYZ00002"
Comments                       :
Expression                     : select SMS_R_System.Name, SMS_R_System.LastLogonUserName,
                                 SMS_G_System_OPERATING_SYSTEM.Caption from SMS_R_System inner join
                                 SMS_G_System_OPERATING_SYSTEM on SMS_G_System_OPERATING_SYSTEM.ResourceID =
                                 SMS_R_System.ResourceId where SMS_G_System_OPERATING_SYSTEM.Caption like "Microsoft Windows Server 2012%"
LimitToCollectionID            : XYZ0025F
LocalizedCategoryInstanceNames : {}
Name                           : Server 2016
QueryID                        : XYZ00002
ResultAliasNames               : {SMS_R_System, SMS_R_System, SMS_G_System_OPERATING_SYSTEM}
ResultColumnsNames             : {SMS_R_System.Name, SMS_R_System.LastLogonUserName,
                                 SMS_G_System_OPERATING_SYSTEM.Caption}
TargetClassName                : SMS_R_System

PS XYZ:\> Invoke-CMQuery -Id "XYZ00002"


SmsProviderObjectPath         : __GENERIC
SMS_G_System_OPERATING_SYSTEM :
                                instance of SMS_G_System_OPERATING_SYSTEM
                                {
                                        Caption = "Microsoft Windows Server 2012 R2 Datacenter";
                                };

SMS_R_System                  :
                                instance of SMS_R_System
                                {
                                        LastLogonUserName = "jqpublic";
                                        Name = "millcreek01";
                                };
```

This query has a more complex **Expression** that joins two classes. The result of the query is then more complex.

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

Specify the ID of the query to run. For example, `"XYZ00006"`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: QueryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a query object to run. To get this object, use the [Get-CMQuery](Get-CMQuery.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LimitToCollectionId

If the query is configured to prompt for the limiting collection, use this parameter to specify a collection ID. If the query's **LimitToCollectionID** property is `<Prompt>`, and you don't include this parameter when you run the query, the cmdlet fails.

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

### -Name

Specify the name of the query to run.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

[Export-CMQuery](Export-CMQuery.md)
[Get-CMQuery](Get-CMQuery.md)
[Import-CMQuery](Import-CMQuery.md)
[New-CMQuery](New-CMQuery.md)
[Remove-CMQuery](Remove-CMQuery.md)
[Set-CMQuery](Set-CMQuery.md)
[Introduction to queries in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-queries)
