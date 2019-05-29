---
title: Remove-CMFallbackStatusPoint
titleSuffix: Configuration Manager
description: Removes a Configuration Manager fallback status point.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Remove-CMFallbackStatusPoint

## SYNOPSIS
Removes a Configuration Manager fallback status point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMFallbackStatusPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMFallbackStatusPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMFallbackStatusPoint** cmdlet removes a specified fallback status point site system role.
You can specify the site system name and site code for a fallback status point or use the **Get-CMFallbackStatusPoint** cmdlet to obtain a fallback status point object.

Microsoft System Center Configuration Manager can use one or more fallback status points to collect state messages for a site and send them on to Configuration Manager.
After you remove a fallback status point, that system no longer forwards state messages.

The use of a fallback status point is optional.
You can use this cmdlet to remove redundant fallback status points or to remove the last fallback status point from a site if you do not want to use that role.

## EXAMPLES

### Example 1: Remove a specified fallback status point
```
PS C:\> Remove-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "Server21.West01.Contoso.com"
```

This command removes the fallback status point for the site with the site code CM1 and the system name Server21.West01.Contoso.com.

### Example 2: Remove a fallback status point object
```
PS C:\> $CMFSP = Get-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "Server21.West01.Contoso.com"
PS C:\> Remove-CMFallbackStatusPoint -InputObject $CMFSP
```

The first command gets a fallback status point for the site with the site code CM1 and the system name Server21.West01.Contoso.com and stores that object in the $CMFSP variable.

The second command removes the object stored in $CMFSP.

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
Specifies a fallback status point role.
To get a fallback status point role, use the Get-CMFallbackStatusPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: FallbackStatusPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a fallback status point.

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
Specifies the site system name for a fallback status point.

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

[Add-CMFallbackStatusPoint](Add-CMFallbackStatusPoint.md)

[Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md)

[Set-CMFallbackStatusPoint](Set-CMFallbackStatusPoint.md)


