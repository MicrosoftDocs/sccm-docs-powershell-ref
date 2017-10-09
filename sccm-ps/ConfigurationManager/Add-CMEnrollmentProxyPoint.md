---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: A4563737-1BF4-4AD1-A9D3-CFD2F5564586
online version: https://go.microsoft.com/fwlink/?linkid=833676
schema: 2.0.0
---

# Add-CMEnrollmentProxyPoint

## SYNOPSIS
Adds an enrollment proxy point to Configuration Manager.

## SYNTAX

### EnrollmentProxyPointByValue (Default)
```
Add-CMEnrollmentProxyPoint [-WebsiteName <String>] [-PortNumber <Int32>] [-ServiceHost <IResultObject>]
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### EnrollmentProxyPoint
```
Add-CMEnrollmentProxyPoint [-WebsiteName <String>] [-PortNumber <Int32>] [-ServiceHost <IResultObject>]
 [-SiteSystemServerName] <String> [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMEnrollmentProxyPoint** cmdlet adds an enrollment proxy point to a Microsoft System Center Configuration Manager site.
An enrollment proxy point is a site system role.

When Configuration Manager enrolls a mobile device, it installs a Configuration Manager client.
The client provides management capabilities that include hardware inventory, software deployment, settings, and remote wipe.
To enroll mobile devices, use Microsoft Certificate Services with an enterprise certification authority (CA).
You need a Configuration Manager enrollment proxy point site system role, as well as an enrollment point site system role.
For more information about site system roles, see [Install and Configure Site System Roles for Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=262649) on TechNet.

## EXAMPLES

### Example 1: Add an enrollment proxy point
```
PS C:\>Add-CMEnrollmentProxyPoint -SiteCode "CM1" -SiteSystemServerName "CMEnrollmentProxyPoint.Western.Contoso.com"
```

This command adds an enrollment proxy point for the Configuration Manager site that has the site code CM1.
The specified computer hosts the role.

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: EnrollmentProxyPointByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PortNumber
Specifies the port that client computers use to connect with an enrollment proxy point.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Port

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceHost
{{Fill ServiceHost Description}}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: EnrollmentPoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: EnrollmentProxyPoint
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
Parameter Sets: EnrollmentProxyPoint
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebsiteName
```yaml
Type: String
Parameter Sets: (All)
Aliases: IISWebsite

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

[Add-CMEnrollmentPoint](Add-CMEnrollmentPoint.md)

[Get-CMEnrollmentProxyPoint](Get-CMEnrollmentProxyPoint.md)

[Remove-CMEnrollmentProxyPoint](Remove-CMEnrollmentProxyPoint.md)


