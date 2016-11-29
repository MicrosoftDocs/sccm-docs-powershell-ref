---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833824
schema: 2.0.0
ms.assetid: 93167F73-1CDD-4866-BD0B-42126A40807B
---

# New-CMVpnProfileConfigurationItem

## SYNOPSIS
Creates a VPN profile.

## SYNTAX

```
New-CMVpnProfileConfigurationItem -DesiredConfigurationDigestPath <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMVpnProfileConfigurationItem** cmdlet creates a virtual private network (VPN) profile.
Client computers use VPN profiles to remotely connect to a company network over the Internet.

## EXAMPLES

### Example 1: Create a VPN profile configuration item
```
PS C:\>New-CMVpnProfileConfigurationItem -DesiredConfigurationDigestPath "C:\Digests\Vpn.xml"
```

This command creates a VPN profile configuration item by using the digest file C:\Digests\Vpn.xml.

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

### -DesiredConfigurationDigestPath
Specifies a path to the configuration data stored as a digest.

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

[Set-CMVpnProfileConfigurationItem](./Set-CMVpnProfileConfigurationItem.md)


