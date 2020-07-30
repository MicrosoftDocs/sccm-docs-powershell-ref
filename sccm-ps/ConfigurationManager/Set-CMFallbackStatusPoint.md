---
description: Changes the throttle interval or the message count for a Configuration Manager fallback status point.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMFallbackStatusPoint
---

# Set-CMFallbackStatusPoint

## SYNOPSIS
Changes the throttle interval or the message count for a Configuration Manager fallback status point.

## SYNTAX

### SetByValue (Default)
```
Set-CMFallbackStatusPoint -InputObject <IResultObject> [-StateMessageCount <Int32>] [-ThrottleSec <Int32>]
 [-ThrottleMins <Int32>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMFallbackStatusPoint [-SiteCode <String>] [-SiteSystemServerName] <String> [-StateMessageCount <Int32>]
 [-ThrottleSec <Int32>] [-ThrottleMins <Int32>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMFallbackStatusPoint** cmdlet changes the throttle interval or the message count for a fallback status point.
A fallback status point is a site system role.
You can specify the site system name and site code for a fallback status point or use the [Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md) cmdlet to obtain a fallback status point object.

Microsoft System Center Configuration Manager can use one or more fallback status points to collect state messages for a site and send them to a server that is running Configuration Manager.
Throttling prevents the fallback status point from sending too many messages together, which can affect performance.
You can use the *StateMessagesCount* and *ThrottleMinutesInterval* parameters to limit how many messages a fallback status point sends during a defined period.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Change message and threshold settings for a fallback status point
```
PS XYZ:\> $CMFSP = Get-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "Server21.West01.Contoso.com"
PS XYZ:\> Set-CMFallbackStatusPoint -InputObject $CMFSP -StateMessagesCount 1000 -ThrottleMinutesInterval 60
```

The first command gets a fallback status point for the site that has the site code CM1 and the system name Server21.West01.Contoso.com and stores that object in the $CMFSP variable.

The second command sets the count of state messages to 1,000 and the throttle interval to 60 minutes for the object stored in $CMFSP.

### Example 2: Change message and threshold settings
```
PS XYZ:\> Set-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "Server21.West01.Contoso.com" -StateMessagesCount 1000 -ThrottleMinutesInterval 60
```

This command sets the count of state messages to 1,000 and the throttle interval to 60 minutes for the fallback status point for the site that has the site code CM1 and the system name Server21.West01.Contoso.com.

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

### -InputObject
Specifies a fallback status point role.
To obtain a fallback status point role, use the [Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: FallbackStatusPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -SiteCode
Specifies the site code for a fallback status point.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the site system name for a fallback status point.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StateMessageCount
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StateMessagesCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ThrottleMinutesInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleSec
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Add-CMFallbackStatusPoint](Add-CMFallbackStatusPoint.md)

[Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md)

[Remove-CMFallbackStatusPoint](Remove-CMFallbackStatusPoint.md)
