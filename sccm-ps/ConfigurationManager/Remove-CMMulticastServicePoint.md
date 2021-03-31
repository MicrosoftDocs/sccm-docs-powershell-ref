---
description: Removes a multicast service point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMMulticastServicePoint
---

# Remove-CMMulticastServicePoint

## SYNOPSIS
Removes a multicast service point.

## SYNTAX

### ByValue (Default)
```
Remove-CMMulticastServicePoint [-Force] -InputObject <IResultObject> [-RemoveWds] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMMulticastServicePoint [-Force] [-RemoveWds] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMMulticastServicePoint** cmdlet removes the multicast service point and disables multicast for the distribution point.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a multicast service point by using the pipeline
```
PS XYZ:\> Get-CMMulticastServicePoint -SiteSystemServerName "server1.contoso.com" -SiteCode "PS1" | Remove-CMMulticastServicePoint -RemoveWds -Force
```

This command gets the multicast service point object with the site system server name of server1.contoso.com and site code PS1 and uses the pipeline operator to pass the object to **Remove-CMMulticastServicePoint**, which removes the multicast service point and WDS.
Using the *Force* parameter indicates that the user is not prompted for confirmation before the command runs.

### Example 2: Remove a multicast service point
```
PS XYZ:\> Remove-CMMulticastServicePoint -SiteSystemServerName "server1.contoso.com" -SiteCode "PS1" -RemoveWds -Force
```

This command removes the multicast service point with the site system server name of server1.contoso.com and site code PS1.
The command removes WDS, and by specifying the *Force* parameter, does not prompt the user for confirmation before the command runs.

## PARAMETERS

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### 

## NOTES

## RELATED LINKS

[Add-CMMulticastServicePoint](Add-CMMulticastServicePoint.md)

[Get-CMMulticastServicePoint](Get-CMMulticastServicePoint.md)

[Set-CMMulticastServicePoint](Set-CMMulticastServicePoint.md)


