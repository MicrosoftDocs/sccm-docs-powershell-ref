---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-CMAadConditionalAccessPolicy

## SYNOPSIS
Sets an aad conditional access policy

## SYNTAX

```
Set-CMAadConditionalAccessPolicy [-ClientType <AadServicePrincipalClientType>]
 [-TargetedDevicePlatform <AadServicePrincipalDevicePlatform[]>]
 [-WindowsDeviceState <AadServicePrincipalDeviceState>] -Enabled <Boolean> [-ExcludedSecurityGroup <String[]>]
 -IncludedSecurityGroup <String[]> [-PassThru] -ServicePrincipalType <AadServicePrincipalType>
 [-AccountId <String>] [-AuthorityId <String>] [-IntuneClientId <String>] [-IntuneResourceId <String>]
 [-UserCredential <PSCredential>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
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

### -AccountId
{{Fill AccountId Description}}

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

### -AuthorityId
{{Fill AuthorityId Description}}

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

### -ClientType
{{Fill ClientType Description}}

```yaml
Type: AadServicePrincipalClientType
Parameter Sets: (All)
Aliases: 
Accepted values: NativeApps, BrowsersAndNativeApps

Required: False
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

### -Enabled
{{Fill Enabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedSecurityGroup
{{Fill ExcludedSecurityGroup Description}}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ExcludedSecurityGroups

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

### -IncludedSecurityGroup
{{Fill IncludedSecurityGroup Description}}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: IncludedSecurityGroups

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IntuneClientId
{{Fill IntuneClientId Description}}

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

### -IntuneResourceId
{{Fill IntuneResourceId Description}}

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

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -ServicePrincipalType
{{Fill ServicePrincipalType Description}}

```yaml
Type: AadServicePrincipalType
Parameter Sets: (All)
Aliases: 
Accepted values: ExchangeOnline, SharepointOnline, SkypeForBusiness, CrmOnline

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetedDevicePlatform
{{Fill TargetedDevicePlatform Description}}

```yaml
Type: AadServicePrincipalDevicePlatform[]
Parameter Sets: (All)
Aliases: TargetedDevicePlatforms
Accepted values: Ios, Android, WindowsPhone, Windows, EasSupported, EasUnsupported, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserCredential
{{Fill UserCredential Description}}

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Credentials, Credential

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsDeviceState
{{Fill WindowsDeviceState Description}}

```yaml
Type: AadServicePrincipalDeviceState
Parameter Sets: (All)
Aliases: 
Accepted values: CompliantOrDomainJoined, DomainJoined, Compliant

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

### System.Object

## NOTES

## RELATED LINKS

