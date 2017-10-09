---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMCloudManagementGateway

## SYNOPSIS
Creates a cloud management gateway

## SYNTAX

```
New-CMCloudManagementGateway -SubscriptionId <String> [-GovernmentSubscription <Boolean>]
 -ManagementCertificatePath <String> [-Description <String>] -ServiceCName <String>
 -ServiceCertificatePath <String> -RootCertificatePath <String> [-TrafficOutGB <Int32>]
 [-TrafficWarningPct <Int32>] [-TrafficCriticalPct <Int32>] [-ManagementCertificatePassword <SecureString>]
 [-ServiceCertificatePassword <SecureString>] -Region <AzureRegion> [-VMInstanceCount <Int32>]
 [-CheckClientCertRevocation <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -CheckClientCertRevocation
{{Fill CheckClientCertRevocation Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

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

### -Description
{{Fill Description Description}}

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

### -GovernmentSubscription
{{Fill GovernmentSubscription Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementCertificatePassword
{{Fill ManagementCertificatePassword Description}}

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementCertificatePath
{{Fill ManagementCertificatePath Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: ManagementCertificate

Required: True
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

### -Region
{{Fill Region Description}}

```yaml
Type: AzureRegion
Parameter Sets: (All)
Aliases: 
Accepted values: AnywhereAsia, AnywhereEurope, AnywhereUS, EastAsia, EastUS, NorthCentralUS, NorthEurope, SouthCentralUS, SoutheastAsia, WestEurope, WestUS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RootCertificatePath
{{Fill RootCertificatePath Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: RootCertificate

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCName
{{Fill ServiceCName Description}}

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

### -ServiceCertificatePassword
{{Fill ServiceCertificatePassword Description}}

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCertificatePath
{{Fill ServiceCertificatePath Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceCertificate

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
{{Fill SubscriptionId Description}}

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

### -TrafficCriticalPct
{{Fill TrafficCriticalPct Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficOutGB
{{Fill TrafficOutGB Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficWarningPct
{{Fill TrafficWarningPct Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMInstanceCount
{{Fill VMInstanceCount Description}}

```yaml
Type: Int32
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_AzureService
IResultObject[]#SMS_SCI_SysResUse
IResultObject[]#SMS_Alert
IResultObject#SMS_Alert

## NOTES

## RELATED LINKS

