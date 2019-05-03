---
title: Get-CMScript
titleSuffix: Configuration Manager
description: Gets Configuration Manager PowerShell scripts.
ms.date: 11/15/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Get-CMScript

## SYNOPSIS

Gets Configuration Manager PowerShell scripts.

## SYNTAX

```powershell
Get-CMScript [-Author <String>] [-ScriptName <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling]
```

## DESCRIPTION

The **Get-CMScript** cmdlet gets one or more Microsoft System Center Configuration Manager Powershell scripts. System Center Configuration Manager has an integrated ability to run Powershell scripts. The scripts simplify building custom tools to administer software and let you accomplish mundane tasks quickly, allowing you to get large jobs done more easily and more consistently. For more information, see [Create and run PowerShell scripts from the Configuration Manager console](https://docs.microsoft.com/sccm/apps/deploy-use/create-deploy-scripts).

You can get a specific script by specifying the author or the name of the script.

## EXAMPLES

### Example 1: Get all scripts

```powershell
PS C:\> Get-CMScript
```

This command gets all scripts that System Center Configuration Manager manages.

### Example 2: Get scripts by using name

```powershell
PS C:\> Get-CMScript -ScriptName "D*"
```

This command gets all scripts that have a name that begins with the letter D.

## PARAMETERS

### -Author

Specifies an author.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
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

### -Fast

Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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

### -ScriptName

Specifies a script name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_Scripts

IResultObject#SMS_Scripts

## RELATED LINKS

[Approve-CMScript](Approve-CMScript.md)

[Deny-CMScript](Deny-CMScript.md)

[Invoke-CMScript](Invoke-CMScript.md)

[Remove-CMScript](Remove-CMScript.md)

[Set-CMScriptDeploymentType](Set-CMScriptDeploymentType.md)

[Add-CMScriptDeploymentType](Add-CMScriptDeploymentType.md)