---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834224
schema: 2.0.0
ms.assetid: F1ED4151-C15F-48B0-9C1C-1636136C1C57
---

# New-CMADGroupDiscoveryScope

## SYNOPSIS

## SYNTAX

### NewGroup (Default)
```
New-CMADGroupDiscoveryScope [-DiscoveryAccountUserName <String>] [-DomainControllerServerName <String>]
 -GroupDN <String[]> [-Name] <String> [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### NewLocation
```
New-CMADGroupDiscoveryScope [-DiscoveryAccountUserName <String>] -LdapLocation <String> [-Name] <String>
 [-RecursiveSearch <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

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

### -DiscoveryAccountUserName
```yaml
Type: String
Parameter Sets: (All)
Aliases: UserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainControllerServerName
```yaml
Type: String
Parameter Sets: NewGroup
Aliases: DCName

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

### -GroupDN
```yaml
Type: String[]
Parameter Sets: NewGroup
Aliases: GroupDNs

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapLocation
```yaml
Type: String
Parameter Sets: NewLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecursiveSearch
```yaml
Type: Boolean
Parameter Sets: NewLocation
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


