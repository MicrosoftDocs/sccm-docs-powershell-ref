---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833921
schema: 2.0.0
ms.assetid: A0E3C123-0943-4185-A255-37CE17B6D7F7
---

# Get-CMSoftwareUpdatePoint

## SYNOPSIS
Gets a Configuration Manager software update point.

## SYNTAX

### SearchByName
```
Get-CMSoftwareUpdatePoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMSoftwareUpdatePoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdatePoint** cmdlet gets a software update point site system role for Microsoft System Center Configuration Manager.

A software update point is a site server role that hosts software updates.
System Center Configuration Manager clients connect to a software update point to get available updates.
The software update point interacts with Windows Server Update Services (WSUS) to configure update settings, request synchronization to the update source, and to synchronize software updates from the WSUS database.

You can specify a software update point by site code or by the name of the computer that hosts the site system role.

## EXAMPLES

### Example 1: Get a software update point
```
PS C:\>Get-CMSoftwareUpdatePoint -SiteSystemServerName "UpdateSystem.Western.Contoso.com"
```

The command gets a software update point that UpdateSystem.Western.Contoso.com hosts.

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
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a computer that hosts the software update point site system role.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName
Required: False
Position: 0
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

[Add-CMSoftwareUpdatePoint](./Add-CMSoftwareUpdatePoint.md)

[Remove-CMSoftwareUpdatePoint](./Remove-CMSoftwareUpdatePoint.md)

[Set-CMSoftwareUpdatePoint](./Set-CMSoftwareUpdatePoint.md)


