---
external help file: AdminUI.PS.CalTracking.dll-Help.xml
ms.assetid: F4A560C6-BF3A-423B-B6FB-F779E2863F4F
online version: https://go.microsoft.com/fwlink/?linkid=834053
schema: 2.0.0
---

# Get-CMAccessLicense

## SYNOPSIS
Gets license usage information.

## SYNTAX

### ByName (Default)
```
Get-CMAccessLicense [-License] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCount
```
Get-CMAccessLicense -LicenseName <String> [-Count] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByValue
```
Get-CMAccessLicense -LicenseName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAccessLicense** cmdlet gets license usage information for the servers and clients in the scope of System Center Configuration Manager.
This cmdlet returns a list of features able to be licensed and a list of unique users and devices per licensable feature.

## EXAMPLES

### Example 1: Get all licensable features for all servers and clients
```
PS C:\> Get-CMAccessLicense -License
```

This command gets all licensable features for all servers and clients within the scope of System Center Configuration Manager.

### Example 2: Get the unique users, devices, and license-specific unique ID for a specified license
```
PS C:\> Get-CMAccessLicense -LicenseName ConfigMgr_2012_EndPointClient
```

This command gets the unique users, devices, and license-specific IDs for the license named ConfigMgr_2012_EndPointClient.

## PARAMETERS

### -Count
Indicates that the cmdlet returns a count of unique users and devices for the specified licensable feature.

```yaml
Type: SwitchParameter
Parameter Sets: ByCount
Aliases: 

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

### -License
Indicates that the cmdlet gets all licensable features for all of the servers and clients within the scope of System Center Configuration Manager.
You can specify the name of the license that is returned for the *LicenseName* parameter to obtain the unique users and devices for that specific license.

```yaml
Type: SwitchParameter
Parameter Sets: ByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseName
Specifies the name of a licensable feature.
If specified, the cmdlet gets only the unique users and devices for the specified license name.
The acceptable values for this parameter are:

- ConfigMgr_2012_CoreServer
- ConfigMgr_2012_CoreClient
- ConfigMgr_2012_EndpointClient

```yaml
Type: String
Parameter Sets: ByCount, ByValue
Aliases: 
Accepted values: ConfigMgr_2012_CoreServer, ConfigMgr_2012_CoreClient, ConfigMgr_2012_EndpointClient

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

