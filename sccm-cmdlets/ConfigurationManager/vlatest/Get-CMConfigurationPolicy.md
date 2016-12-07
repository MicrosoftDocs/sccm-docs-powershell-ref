---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834279
schema: 2.0.0
ms.assetid: 3A8B20A1-F35D-483F-BF47-1ECDC5109034
---

# Get-CMConfigurationPolicy

## SYNOPSIS
Gets a configuration policy.

## SYNTAX

### SearchByName (Default)
```
Get-CMConfigurationPolicy [[-Name] <String>] [-AsXml] [-CategoryInstanceType <String[]>] [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMConfigurationPolicy [-Id] <Int32> [-AsXml] [-CategoryInstanceType <String[]>] [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMConfigurationPolicy [-AsXml] [[-InputObject] <IResultObject>] [-CategoryInstanceType <String[]>] [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConfigurationPolicy** cmdlet gets a configuration policy.

## EXAMPLES

### Example 1: Get a configuration policy by name
```
PS C:\> Get-CMConfigurationPolicy -Name "TrustedCACert01" -AsXml
```

This command gets the configuration policy named TrustedCACert01 and displays the output in XML format.

### Example 2: Get a configuration policy by ID
```
PS C:\> Get-CMConfigurationPolicy -Id 16777454 -Fast
```

This command gets the configuration policy with the ID of 16777454 and does not display lazy properties.

## PARAMETERS

### -AsXml
Specifies that the configuration policy is returned in XML format.

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

### -CategoryInstanceType
Specifies an array of category instance types.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CategoryInstanceTypes
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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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

### -Id
Specifies the CI__ID of a configuration policy.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CIId, CI_ID
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a configuration policy object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a configuration policy.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName
Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject[]#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Copy-CMConfigurationPolicy](./Copy-CMConfigurationPolicy.md)

[Remove-CMConfigurationPolicy](./Remove-CMConfigurationPolicy.md)


