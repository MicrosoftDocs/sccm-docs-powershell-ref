---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833680
schema: 2.0.0
ms.assetid: 787B327A-1694-4942-852C-268301003B5D
---

# Add-CMFallbackStatusPoint

## SYNOPSIS
Adds a fallback status point to a Configuration Manager site.

## SYNTAX

### ByValue (Default)
```
Add-CMFallbackStatusPoint [-StateMessageNum <Int32>] [-ThrottleSec <Int32>] [-ThrottleMins <Int32>]
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Add-CMFallbackStatusPoint [-SiteSystemServerName] <String> [-SiteCode <String>] [-StateMessageNum <Int32>]
 [-ThrottleSec <Int32>] [-ThrottleMins <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMFallbackStatusPoint** cmdlet adds a fallback status point to a Microsoft System Center Configuration Manager site.
To add this site system role, specify the site code for the Configuration Manager site and the name of the computer that hosts the role.
You also need to specify a throttle interval and the number of messages for that throttle window.

Configuration Manager can use one or more fallback status points to collect state messages for a site and send them to Configuration Manager.
Throttling prevents the fallback status point from sending too many messages together, which can affect performance.
For more information about site system roles, see [Install and Configure Site System Roles for Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=262649) on TechNet.

## EXAMPLES

### Example 1: Add a fallback status point
```
PS C:\>Add-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "CMFSPPoint.Western.Contoso.com" -StateMessageNum 10000 -ThrottleInterval 60
```

This command adds a fallback status point for the site that has the site code CM1.
The specified computer hosts the role.
The command also specifies number of messages and throttle time period for the fallback status point.

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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server that hosts a site system role.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name, ServerName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StateMessageNum
Specifies the number of state messages that a fallback status point can send to Configuration Manager within a throttle interval.

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

### -ThrottleMins


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

### -ThrottleSec


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ThrottleIntervalSeconds, ThrottleInterval
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

[Get-CMFallbackStatusPoint](./Get-CMFallbackStatusPoint.md)

[Remove-CMFallbackStatusPoint](./Remove-CMFallbackStatusPoint.md)

[Set-CMFallbackStatusPoint](./Set-CMFallbackStatusPoint.md)


