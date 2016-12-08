---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834139
schema: 2.0.0
ms.assetid: 23C2C811-714F-4B4C-A811-8FF6D837AF8B
---

# Remove-CMMulticastServicePoint

## SYNOPSIS
Removes a multicast service point.

## SYNTAX

### ByValue (Default)
```
Remove-CMMulticastServicePoint [-Force] [-RemoveWds] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMMulticastServicePoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String> [-RemoveWds]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMMulticastServicePoint** cmdlet removes the multicast service point and disables multicast for the distribution point.

## EXAMPLES

### Example 1: Remove a multicast service point by using the pipeline
```
PS C:\> Get-CMMulticastServicePoint -SiteSystemServerName "server1.contoso.com" -SiteCode "PS1" | Remove-CMMulticastServicePoint -RemoveWds -Force
```

This command gets the multicast service point object with the site system server name of server1.contoso.com and site code PS1 and uses the pipeline operator to pass the object to **Remove-CMMulticastServicePoint**, which removes the multicast service point and WDS.
Using the *Force* parameter indicates that the user is not prompted for confirmation before the command runs.

### Example 2: Remove a multicast service point
```
PS C:\> Remove-CMMulticastServicePoint -SiteSystemServerName "server1.contoso.com" -SiteCode "PS1" -RemoveWds -Force
```

This command removes the multicast service point with the site system server name of server1.contoso.com and site code PS1.
The command removes WDS, and by specifying the *Force* parameter, does not prompt the user for confirmation before the command runs.

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
Specifies a multicast service point object.
To obtain a multicast service point object, use the Get-CMMulticastServicePoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: MulticastServicePoint
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoveWds
Indicates that Windows Deployment Services (WDS) is removed.
WDS cannot be removed if the PXE role is still present on the distribution point.
The default is to remove WDS.

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
Specifies the site code for the Configuration Manager site that hosts the site system role.

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
Specifies the name of the server that hosts a site system role.

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

[Add-CMMulticastServicePoint](./Add-CMMulticastServicePoint.md)

[Get-CMMulticastServicePoint](./Get-CMMulticastServicePoint.md)

[Set-CMMulticastServicePoint](./Set-CMMulticastServicePoint.md)


