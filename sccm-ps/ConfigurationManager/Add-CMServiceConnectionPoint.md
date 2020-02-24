---
author: aczechowski
description: Adds a service connection point to a site system server.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Add-CMServiceConnectionPoint
titleSuffix: Configuration Manager
---

# Add-CMServiceConnectionPoint

## SYNOPSIS
Adds a service connection point to a site system server.

## SYNTAX

### ByValue (Default)
```
Add-CMServiceConnectionPoint -Mode <ServiceConnectionPointMode> -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMServiceConnectionPoint -Mode <ServiceConnectionPointMode> [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMServiceconnectionPoint** cmdlet adds a service connection point role to a site system server.
This connects Microsoft System Center Configuration Manager to Microsoft cloud services and enables you to add a Microsoft Intune subscription and to update your Configuration Manager installation.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a service connection point
```
PS XYZ:\> Add-CMServiceConnectionPoint -SiteSystemServerName "TestServer01.Contoso.com" -SiteCode PS1 -Mode Online
```

This command adds the service connection point site system role to the site system server named TestServer01.Contoso.com and the site code PS1.
The command sets the mode to online.

### Example 2: Add a service connection point by using a variable
```
PS XYZ:\> $Server = Get-CMSiteSystemServer -SiteCode PS1 -SiteSystemServerName "TestServer02.Contoso.com"
PS XYZ:\> Add-CMServiceConnectionPoint -InputObject $Server -Mode Online
```

The first command gets the site system server object named TestServer02.Contoso.com with the site code PS1 and stores the object in the $Server variable.

The second command adds the service connection point site system role to the site system server stored in $server and sets the mode to online.

### Example 3: Add a service connection point by using the pipeline
```
PS XYZ:\> Get-CMSiteSystemServer -SiteCode PS1 -SiteSystemServerName "TestServer03.Contoso.com" | Add-CMServiceConnectionPoint -Mode Online
```

This command gets the site system server object named TestServer03.Contoso.com with the site code PS1 and uses the pipeline operator to pass the object to **Add-CMServiceConnectionPoint**, which adds the service connection point site system role to the site system server object and sets the mode to online.

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
Specifies a service connection point object.
To obtain a service connection point object, use the Get-CMServiceConnectionPoint cmdlet.

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

### -Mode
Specifies a mode for the service connection point.
Valid values are:

- Online
- Offline

```yaml
Type: ServiceConnectionPointMode
Parameter Sets: (All)
Aliases:
Accepted values: Online, Offline

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Specifies the name of a site system server to host the service connection point role.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Get-CMServiceConnectionPoint](Get-CMServiceConnectionPoint.md)

[Remove-CMServiceConnectionPoint](Remove-CMServiceConnectionPoint.md)

[Set-CMServiceConnectionPoint](Set-CMServiceConnectionPoint.md)


