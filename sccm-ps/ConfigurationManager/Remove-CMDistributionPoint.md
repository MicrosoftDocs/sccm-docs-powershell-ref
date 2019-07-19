<<<<<<< HEAD
---
title: Remove-CMDistributionPoint
titleSuffix: Configuration Manager
description: Removes a distribution point.
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
ms.assetid: BD6E2FCF-CFEB-4111-AACB-B817E25915BF
online version: https://go.microsoft.com/fwlink/?linkid=834068
schema: 2.0.0
>>>>>>> master
---

# Remove-CMDistributionPoint

## SYNOPSIS
Removes a distribution point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMDistributionPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMDistributionPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDistributionPoint** cmdlet removes a distribution point.
When you remove a distribution point, you remove the designation of a site system server to function as a distribution center for content files for applications, packages, software updates, and operating system deployment.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove a distribution point by using the pipeline
```
PS XYZ:\> Get-CMDistributionPoint -SiteSystemServerName "MySiteSys_11310.Contoso.com" | Remove-CMDistributionPoint -Force
```

This command gets the distribution point object for the site system server named MySiteSys_11310.Contoso.com and uses the pipeline operator to pass the object to **Remove-CMDistributionPoint**, which removes the distribution point object.
Specifying the *Force* parameter indicates that the user is not prompted before the distribution point is removed.

### Example 2: Remove a distribution point by using an object variable
```
PS XYZ:\> $DP = Get-CMDistributionPoint -SiteSystemServerName "MySiteSys_11310.Contoso.com"
PS XYZ:\> Remove-CMDistributionPoint -InputObject $DP -Force
```

The first command gets the distribution point object for the site system server named MySiteSys_11310.Contoso.com and stores the object in the $DP variable.

The second command removes the distribution point stored in $DP.
Specifying the *Force* parameter indicates that the user is not prompted before the distribution point is removed.

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
Specifies a distribution point object.
To obtain a distribution point object, use the [Get-CMDistributionPoint](Get-CMDistributionPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: DistributionPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for the Configuration Manager site that hosts this site system role.

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
Specifies the FQDN of the server that hosts the site system role.

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

[Add-CMDistributionPoint](Add-CMDistributionPoint.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[New-CMDistributionPointGroup](New-CMDistributionPointGroup.md)

[Set-CMDistributionPoint](Set-CMDistributionPoint.md)

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[Update-CMDistributionPoint](Update-CMDistributionPoint.md)


