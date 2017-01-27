---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834190
schema: 2.0.0
ms.assetid: 020CF218-583F-4419-8AFB-09C8CD67D755
---

# Invoke-CMWmiQuery

## SYNOPSIS
Runs a WMI query.

## SYNTAX

### ByWql (Default)
```
Invoke-CMWmiQuery [-Option <QueryOptions>] [-Query] <String> [-Context <Hashtable>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySearch
```
Invoke-CMWmiQuery -Search <SmsProviderSearch> -ClassName <String> [-Option <QueryOptions>]
 [-Context <Hashtable>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMWmiQuery** cmdlet runs a Windows Management Instrumentation (WMI) query.

## EXAMPLES

### Example 1: Run a WQL query
```
PS C:\> $WQL = @"
SELECT app.* FROM SMS_ApplicationLatest AS app
INNER JOIN SMS_CIContentPackage AS con ON app.CI_ID=con.CI_ID
INNER JOIN SMS_DistributionPoint AS srv ON con.PackageID=srv.PackageID
WHERE app.IsHidden = 0
"@
PS C:\> Invoke-CMWmiQuery -Query $WQL -Option Lazy
```

The first command creates a WQL query and stores it in the $WQL variable.

The second command runs the query stored in $WQL.

### Example 2: Run a WMI query for device collections
```
PS C:\> $Search = [Microsoft.ConfigurationManagement.PowerShell.Provider.SmsProviderSearch]::new()
PS C:\> $Search.AddOrder("CollectionID", [Microsoft.ConfigurationManagement.PowerShell.Provider.SearchParameterOrderBy]::Asc)
PS C:\> $Search.Add("Name","DeviceCol*", $True)
PS C:\> Invoke-CMWmiQuery -Search $Search -ClassName "SMS_Collection" -Option Lazy
```

The first command creates a search object and stores the object in the $Search variable.

The second command specifies that the search order is by CollectionID.

The third command adds search parameters to the $Search object.
In this case, the query searches for device collections.

The last command runs the query stored in $Search, specifying SMS_Collection as the class that contains  the CollectionID property.

### Example 3: Run a WMI query for sites by status
```
PS C:\> $Search.Clear()
PS C:\> $Search.Add("Status", $True)
PS C:\> Invoke-CMWmiQuery -ClassName "SMS_Site" -Search $Search
```

The first command clears the search parameters from the search object created in example 2.

The second command adds search parameters to the $Search object.
In this case, the query searches for sites.

The last command runs the query stored in $Search, specifying SMS_Site as the class that contains the site Status property.

### Example 4: Run a WMI query for sites by name
```
PS C:\> $Search.Clear()
PS C:\> $Search.Add("SiteName", $null, [Microsoft.ConfigurationManagement.PowerShell.Provider.SearchParameterOperator]::NotEquals)
PS C:\> Invoke-CMWmiQuery -ClassName "SMS_Site" -Search $Search
```

The first command clears the search parameters from the search object created in example 2.

The second command adds search parameters to the $Search object.
In this case, the query searches for sites.

The last command runs the query stored in $Search, specifying SMS_Site as the class that contains the SiteName property.

### Example 5: Run a WMI query for applications
```
PS C:\> $Search.Clear()
PS C:\>  $Search.AddAdhoc("CI_ID > 0")
PS C:\>  Invoke-CMWmiQuery -ClassName "SMS_Application" -Search $Search -Option Lazy
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

### IResultObject[]

## NOTES

## RELATED LINKS

[Invoke-CMWmiMethod](./Invoke-CMWmiMethod.md)
