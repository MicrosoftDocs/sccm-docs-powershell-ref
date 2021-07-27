---
description: Run a WMI query.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2020
schema: 2.0.0
title: Invoke-CMWmiQuery
---

# Invoke-CMWmiQuery

## SYNOPSIS

Run a WMI query.

## SYNTAX

### ByWql (Default)
```
Invoke-CMWmiQuery [-Context <Hashtable>] [-Option <QueryOptions>] [-Query] <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySearch
```
Invoke-CMWmiQuery -ClassName <String> [-Context <Hashtable>] [-Option <QueryOptions>]
 -Search <SmsProviderSearch> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **Invoke-CMWmiQuery** cmdlet runs a Windows Management Instrumentation (WMI) query. Unlike other query cmdlets or tools, with this cmdlet the connection and namespace is already set up for you.

You can also use this cmdlet to create a query with WMI Query Language (WQL). Configuration Manager uses WQL for queries in collections. WQL is similar to SQL, but still uses the SMS Provider, thus abides by role-based access controls.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Run a WQL query

The first command creates a WQL query and stores it in the **$WQL** variable. The second command runs the query stored in the variable.

```powershell
$WQL = @"
SELECT app.* FROM SMS_ApplicationLatest AS app
INNER JOIN SMS_CIContentPackage AS con ON app.CI_ID=con.CI_ID
INNER JOIN SMS_DistributionPoint AS srv ON con.PackageID=srv.PackageID
WHERE app.IsHidden = 0
"@

Invoke-CMWmiQuery -Query $WQL -Option Lazy
```

### Example 2: Run a WMI query for device collections

The first command creates a search object and stores the object in the **$Search** variable.

The second command specifies that the search order is ascending by **CollectionID**.

The third command adds search parameters to the **$Search** object. In this case, the query searches for device collections.

The last command runs the query stored in **$Search**. It specifies **SMS_Collection** as the class that contains the **CollectionID** property.

```powershell
$Search = [Microsoft.ConfigurationManagement.PowerShell.Provider.SmsProviderSearch]::new()
$Search.AddOrder("CollectionID", [Microsoft.ConfigurationManagement.PowerShell.Provider.SearchParameterOrderBy]::Asc)
$Search.Add("Name","DeviceCol*", $True)

Invoke-CMWmiQuery -Search $Search -ClassName "SMS_Collection" -Option Lazy
```

### Example 3: Run a WMI query for sites by status

The first command clears the search parameters from any existing search object.

The second command adds search parameters to the **$Search** object. In this case, the query searches for sites.

The last command runs the query stored in **$Search**. It specifies **SMS_Site** as the class that contains the site **Status** property.

```powershell
$Search.Clear()
$Search.Add("Status", $True)

Invoke-CMWmiQuery -ClassName "SMS_Site" -Search $Search
```

### Example 4: Run a WMI query for sites by name

The first command clears the search parameters from any existing search object.

The second command adds search parameters to the **$Search** object. In this case, the query searches for sites.

The last command runs the query stored in **$Search**. It specifies **SMS_Site** as the class that contains the **SiteName** property.

```powershell
$Search.Clear()
$Search.Add("SiteName", $null, [Microsoft.ConfigurationManagement.PowerShell.Provider.SearchParameterOperator]::NotEquals)

Invoke-CMWmiQuery -ClassName "SMS_Site" -Search $Search
```

### Example 5: Run a WMI query for applications

The first command clears the search parameters from any existing search object.

The second command adds search parameters to the **$Search** object. In this case, the query searches for applications.

The last command runs the query stored in **$Search**. It specifies **SMS_Site** as the class that contains the site **CI_ID** property.

```powershell
$Search.Clear()
$Search.AddAdhoc("CI_ID > 0")

Invoke-CMWmiQuery -ClassName "SMS_Application" -Search $Search -Option Lazy
```

## PARAMETERS

### -ClassName

Specifies the Configuration Manager WMI class that you want to query.

```yaml
Type: String
Parameter Sets: BySearch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context

Specify the WMI context as a hash table. It's a list of name/value pairs that are passed to a WMI provider that supports context information for a customized operation.

```yaml
Type: Hashtable
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

### -Option

The most common option is `Fast`.

Specify a query option:

- `None`: Default
- `Lazy`: By default, the cmdlet loads lazy properties.
- `Fast`: Use this option to not load lazy properties. This option can return results more quickly for some classes.
- `ExpectResults` & `ExpectResultsThrowException`: If the query returns no results, throw an exception. This exception typically ends a script.
- `FastExpectResults` & `LazyExpectResults`: These options combine `Fast` and `Lazy` with `ExpectResults`.
- `ExpectResultsSoftFail`: If the query returns no results, output an error, but don't end the script.

For more information about lazy properties, see [Configuration Manager lazy properties](/mem/configmgr/develop/core/understand/configuration-manager-lazy-properties).

The following values are for internal use only:

- Clone
- NoMask
- NoRefresh
- IgnoreNoResults

```yaml
Type: QueryOptions
Parameter Sets: (All)
Aliases: Options
Accepted values: None, NoRefresh, Lazy, Fast, ExpectResults, FastExpectResults, LazyExpectResults, Clone, ExpectResultsSoftFail, ExpectResultsThrowException, NoMask, IgnoreNoResults

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query

Specifies a WMI Query Language (WQL) statement.

```yaml
Type: String
Parameter Sets: ByWql
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Search

Specifies an **SMSProviderSearch** object.

```yaml
Type: SmsProviderSearch
Parameter Sets: BySearch
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

### None
## OUTPUTS

### IResultObject[]
### IResultObject
## NOTES

## RELATED LINKS

[Invoke-CMWmiMethod](Invoke-CMWmiMethod.md)
