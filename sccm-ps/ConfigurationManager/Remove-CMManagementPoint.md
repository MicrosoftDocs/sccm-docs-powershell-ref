<<<<<<< HEAD
---
title: Remove-CMManagementPoint
titleSuffix: Configuration Manager
description: Removes a management point.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 2EC18943-84E5-4291-BCD9-0EB15C9D31FA
online version: https://go.microsoft.com/fwlink/?linkid=834131
schema: 2.0.0
>>>>>>> master
---

# Remove-CMManagementPoint

## SYNOPSIS
Removes a management point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMManagementPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMManagementPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMManagementPoint** cmdlet removes a management point.
A management point is a site system role that provides policy and service location information to clients and receives configuration data from clients.

When you remove a management point, Microsoft System Center Configuration Manager disables communication between the site server and the clients that you assigned to the site server.
System Center Configuration Manager cannot provide these clients with installation prerequisites, client installation files, configuration details, advertisements, and software distribution package source file locations.
Additionally, System Center Configuration Manager cannot receive inventory data, software metering information, and status and state messages from the clients.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove a management point
```
PS XYZ:\> Remove-CMManagementPoint -SiteSystemServerName "cmcen-dist02.tsqa.contoso.com" -SiteCode "CM1"
```

This command removes the management point from the Configuration Manager site that has the site code CM1 on the site system named cmcen-dist02.tsqa.contoso.com.

### Example 2: Remove a management point by using an object variable
```
PS XYZ:\> $Mp = Get-CMManagementPoint -SiteSystemServerName "dist02.tsqa.contoso.com" -SiteCode "CM1"
PS XYZ:\> Remove-CMManagementPoint -InputObject $Mp
```

The first command gets the management point from the Configuration Manager site that has the site code CM1 on the site system named dist02.tsqa.contoso.com.
The command stores the results in the $Mp variable.

The second command removes the management point stored in the $Mp variable.

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
Specifies a **CMManagementPoint** object.
To obtain a **CMManagementPoint** object, use the [Get-CMManagementPoint](Get-CMManagementPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ManagementPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

[Add-CMManagementPoint](Add-CMManagementPoint.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Get-CMManagementPointComponent](Get-CMManagementPointComponent.md)


