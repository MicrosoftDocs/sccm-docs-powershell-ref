---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMADGroupDiscoveryScope

## SYNOPSIS
Creates an a d group discovery scope

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
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

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

### -DiscoveryAccountUserName
{{Fill DiscoveryAccountUserName Description}}

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
{{Fill DomainControllerServerName Description}}

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

### -GroupDN
{{Fill GroupDN Description}}

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
{{Fill LdapLocation Description}}

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
{{Fill Name Description}}

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
{{Fill RecursiveSearch Description}}

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
{{Fill SiteCode Description}}

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

### None

## OUTPUTS

### ADGroupDiscoveryScope
ADGroupGroupDiscoveryScope
ADGroupLocationDiscoveryScope

## NOTES

## RELATED LINKS

