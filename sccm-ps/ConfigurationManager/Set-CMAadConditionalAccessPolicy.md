---
author: aczechowski
description: Sets an aad conditional access policy.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMAadConditionalAccessPolicy
titleSuffix: Configuration Manager
---

# Set-CMAadConditionalAccessPolicy

## SYNOPSIS
Sets an aad conditional access policy.

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

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -AccountId
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
