---
external help file: AdminUI.PS.ClientStatus.dll-Help.xml
ms.assetid: C12D4C9E-15A3-44EB-9090-6E80B95045E3
online version: https://go.microsoft.com/fwlink/?linkid=834197
schema: 2.0.0
---

# Get-CMClientStatusSetting

## SYNOPSIS
Gets client status settings.

## SYNTAX

```
Get-CMClientStatusSetting [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientStatusSetting** cmdlet gets client status settings for the local computer.
These settings determine the data collection intervals for individual client monitoring activities.

For more information about client settings, see [About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226) on TechNet.

## EXAMPLES

### Example 1: Get client status settings for the local computer
```
PS C:\> Get-CMClientStatusSetting
ADRetrieving Schedule  : 
CleanUpInterval        : 7
DDRInactiveInterval    : 3
HWInactiveInterval     : 4
NeedADLastLogonTime    : 
PolicyInactiveInterval : 3
SettingsID             : 1
StatusInactiveInterval : 6
SWInactiveInterval     : 5
```

This command gets client status settings for the local computer.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226)

[Set-CMClientStatusSetting](Set-CMClientStatusSetting.md)

[Update-CMClientStatus](Update-CMClientStatus.md)


