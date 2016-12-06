---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834209
schema: 2.0.0
ms.assetid: 73480395-F8AB-4F64-84F1-ED4EC157EC02
---

# Remove-CMSiteSystemServer

## SYNOPSIS
Removes a site system server.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMSiteSystemServer [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Remove-CMSiteSystemServer [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSiteSystemServer** cmdlet removes a site system server from Microsoft System Center Configuration Manager.
If the site system server has other site system roles besides the site system role, this cmdlet will fail.

## EXAMPLES

### Example 1: Remove a site system server by using the pipeline
```
PS C:\>Get-CMSiteSystemServer -SiteSystemServerName "Server2.contoso.com" -SiteCode "MP5" | Remove-CMSiteSystemServer -Force
```

This command gets the site system server object named Server2.contoso.com with the site code MP5 and uses the pipeline operator to pass the object to **Remove-CMSiteSystemServer**, which removes the site system server object.

### Example 2: Remove a site system server
```
PS C:\>Remove-CMSiteSystemServer -SiteSystemServerName "Server2.contoso.com" -SiteCode "MP5" -Force
```

This command removes the site system server named Server2.contoso.com with the site code MP5.

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

### -Force
Forces the command to run without asking for user confirmation.

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
Specifies a site system server object.
To obtain a site system server object, use the Get-CMSiteSystemServer cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: SiteSystem, SiteSystemServer
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code of a Configuration Manager site.

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
Specifies a server name for the site system.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName
Required: True
Position: 0
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

[Get-CMSiteSystemServer](./Get-CMSiteSystemServer.md)

[New-CMSiteSystemServer](./New-CMSiteSystemServer.md)

[Set-CMSiteSystemServer](./Set-CMSiteSystemServer.md)


