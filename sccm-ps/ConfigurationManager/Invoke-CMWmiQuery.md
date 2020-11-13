---
description: Runs a WMI query.
external help file: AdminUI.PS.Common.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Invoke-CMWmiQuery
---

# Invoke-CMWmiQuery

## SYNOPSIS
Runs a WMI query.

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
The **Invoke-CMWmiQuery** cmdlet runs a Windows Management Instrumentation (WMI) query.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Run a WQL query
```
PS XYZ:\> $WQL = @"
SELECT app.* FROM SMS_ApplicationLatest AS app
INNER JOIN SMS_CIContentPackage AS con ON app.CI_ID=con.CI_ID
INNER JOIN SMS_DistributionPoint AS srv ON con.PackageID=srv.PackageID
WHERE app.IsHidden = 0
"@
PS XYZ:\> Invoke-CMWmiQuery -Query $WQL -Option Lazy
```

The first command creates a WQL query and stores it in the $WQL variable.

The second command runs the query stored in $WQL.

### Example 2: Run a WMI query for device collections
```
PS XYZ:\> $Search = [Microsoft.ConfigurationManagement.PowerShell.Provider.SmsProviderSearch]::new()
PS XYZ:\> $Search.AddOrder("CollectionID", [Microsoft.ConfigurationManagement.PowerShell.Provider.SearchParameterOrderBy]::Asc)
PS XYZ:\> $Search.Add("Name","DeviceCol*", $True)
PS XYZ:\> Invoke-CMWmiQuery -Search $Search -ClassName "SMS_Collection" -Option Lazy
```

The first command creates a search object and stores the object in the $Search variable.

The second command specifies that the search order is by CollectionID.

The third command adds search parameters to the $Search object.
In this case, the query searches for device collections.

The last command runs the query stored in $Search, specifying SMS_Collection as the class that contains  the CollectionID property.

### Example 3: Run a WMI query for sites by status
```
PS XYZ:\> $Search.Clear()
PS XYZ:\> $Search.Add("Status", $True)
PS XYZ:\> Invoke-CMWmiQuery -ClassName "SMS_Site" -Search $Search
```

The first command clears the search parameters from the search object created in example 2.

The second command adds search parameters to the $Search object.
In this case, the query searches for sites.

The last command runs the query stored in $Search, specifying SMS_Site as the class that contains the site Status property.

### Example 4: Run a WMI query for sites by name
```
PS XYZ:\> $Search.Clear()
PS XYZ:\> $Search.Add("SiteName", $null, [Microsoft.ConfigurationManagement.PowerShell.Provider.SearchParameterOperator]::NotEquals)
PS XYZ:\> Invoke-CMWmiQuery -ClassName "SMS_Site" -Search $Search
```

The first command clears the search parameters from the search object created in example 2.

The second command adds search parameters to the $Search object.
In this case, the query searches for sites.

The last command runs the query stored in $Search, specifying SMS_Site as the class that contains the SiteName property.

### Example 5: Run a WMI query for applications
```
PS XYZ:\> $Search.Clear()
PS XYZ:\>  $Search.AddAdhoc("CI_ID > 0")
PS XYZ:\>  Invoke-CMWmiQuery -ClassName "SMS_Application" -Search $Search -Option Lazy
```

The first command clears the search parameters from the search object created in example 2.

The second command adds search parameters to the $Search object.
In this case, the query searches for applications.

The last command runs the query stored in $Search, specifying SMS_Site as the class that contains the site CI_ID property.

## PARAMETERS

### -ClassName
Specifies the Configuration Manager WMI class that contains the static method you want to call.

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
Specifies WMI context.
This is a list of name/value pairs that are passed to a WMI provider that supports context information for a customized operation.

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

### -Option
Specifies the query option.
Valid values are:

- None
- NoRefresh
- Lazy
- Fast
- ExpectResults
- FastExpectResults
- LazyExpectResults
- Clone
- ExpectResultsSoftFail
- ExpectResultsThrowException
- NoMask
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]

### IResultObject

## NOTES

## RELATED LINKS

[Invoke-CMWmiMethod](Invoke-CMWmiMethod.md)
