---
author: aczechowski
description: Removes an Endpoint Protection point.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Remove-CMEndpointProtectionPoint
titleSuffix: Configuration Manager
---

# Remove-CMEndpointProtectionPoint

## SYNOPSIS
Removes an Endpoint Protection point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMEndpointProtectionPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMEndpointProtectionPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMEndpointProtectionPoint** cmdlet removes a System Center 2016 Endpoint Protection point from Microsoft System Center Configuration Manager.
For more information about Endpoint Protection in Configuration Manager, see [Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427) on TechNet.

## EXAMPLES

### Example 1: Remove an Endpoint Protection point
```
PS XYZ:\> Remove-CMEndpointProtectionPoint -SiteSystemServerName "CMServer01.Contoso.com" -SiteCode "CM1"
```

This command removes an Endpoint Protection point.

### Example 2: Remove an Endpoint Protection point by using an input object
```
PS XYZ:\> $EPP = Get-CMEndpointProtectionPoint -SiteCode "CM1" -SiteSystemServerName "CMServer01.Contoso.com" 
PS XYZ:\> Remove-CMEndpointProtectionPoint -InputObject $EPP
```

The first command uses the **Get-CMEndpointProtectionPoint** cmdlet to get an Endpoint Protection point object and assign it to the variable $EPP.

The second command removes the Endpoint Protection point object that is assigned to the variable $EPP.

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
Specifies the input to this cmdlet.
To obtain an input object, use the Get-CMEndpointProtectionPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: EndpointProtectionPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code.

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
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427)

[Add-CMEndpointProtectionPoint](Add-CMEndpointProtectionPoint.md)

[Get-CMEndpointProtectionPoint](Get-CMEndpointProtectionPoint.md)

[Set-CMEndpointProtectionPoint](Set-CMEndpointProtectionPoint.md)


