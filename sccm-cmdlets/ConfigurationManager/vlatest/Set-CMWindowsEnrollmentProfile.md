---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834160
schema: 2.0.0
ms.assetid: 58B6147D-EBD6-4145-88F6-64210E915EE4
---

# Set-CMWindowsEnrollmentProfile

## SYNOPSIS

## SYNTAX

### ByName
```
Set-CMWindowsEnrollmentProfile [-Name] <String> [-Authority <ManagementAuthority>] [-NewName <String>]
 [-Description <String>] [-SiteCode <String>] [-CertificateProfile <IResultObject[]>]
 [-WifiProfile <IResultObject[]>] [-EnrollmentProxyPoint <IResultObject[]>] [-ProxyServerUrl <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValue
```
Set-CMWindowsEnrollmentProfile [-InputObject] <IResultObject> [-Authority <ManagementAuthority>]
 [-NewName <String>] [-Description <String>] [-SiteCode <String>] [-CertificateProfile <IResultObject[]>]
 [-WifiProfile <IResultObject[]>] [-EnrollmentProxyPoint <IResultObject[]>] [-ProxyServerUrl <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

### -Authority
```yaml
Type: ManagementAuthority
Parameter Sets: (All)
Aliases: 
Accepted values: Cloud, OnPremises

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateProfile
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: CertificateProfiles

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
```yaml
Type: String
Parameter Sets: (All)
Aliases: ProfileDescription

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

### -EnrollmentProxyPoint
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: EnrollmentProxyPoints

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

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: ByName
Aliases: ProfileName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
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

### -ProxyServerUrl
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

### -WifiProfile
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: WifiProfiles

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


