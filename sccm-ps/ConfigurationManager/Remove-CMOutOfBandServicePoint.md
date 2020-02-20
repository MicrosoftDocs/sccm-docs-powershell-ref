---
title: Remove-CMOutOfBandServicePoint
titleSuffix: Configuration Manager
description: Removes an out of band service point.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Remove-CMOutOfBandServicePoint

## SYNOPSIS
Removes an out of band service point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMOutOfBandServicePoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMOutOfBandServicePoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMOutOfBandServicePoint** cmdlet removes an out of band service point from Microsoft System Center Configuration Manager.
An out of band service point is a site system role that provisions and configures Intel Active Management Technology (AMT)-based computers for System Center Configuration Manager.

After you remove an out of band service point, administrative users cannot provision and configure the Intel AMT-based computers that are associated with the out of band service point.

## EXAMPLES

### Example 1: Remove an out of band service point
```
PS XYZ:\> Remove-CMOutOfBandServicePoint -SiteSystemServerName "cmcen-dist02.tsqa.contoso.com" -SiteCode "CM1"
```

This command removes the out of band service point from the Configuration Manager site that has the site code CM1 on the site system server named cmcen-dist02.tsqa.contoso.com.

### Example 2: Remove an out of band service point by using an object variable
```
PS XYZ:\> $Osp = Get-CMOutOfBandServicePoint -SiteSystemServerName "cmcen-dist02.tsqa.contoso.com" -SiteCode "CM1"
PS XYZ:\> Remove-CMOutOfBandServicePoint -InputObject $Osp
```

The first command gets the out of band service point from the Configuration Manager site that has the site code CM1 on the site system server named cmcen-dist02.tsqa.contoso.com.
The command stores the results in the $Osp variable.

The second command removes the out of band service point stored in $Osp.

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
Specifies a **CMOutOfBandServicePoint** object.
To obtain a **CMOutOfBandServicePoint** object, use the Get-CMOutOfBandServicePoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: OutOfBandServicePoint
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMOutOfBandServicePoint](Get-CMOutOfBandServicePoint.md)

[Set-CMOutOfBandServicePoint](Set-CMOutOfBandServicePoint.md)

[Add-CMOutOfBandServicePoint](Add-CMOutOfBandServicePoint.md)


