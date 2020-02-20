---
author: mumian
description: Approves a Configuration Manager PowerShell script.
external help file: AdminUI.PS.ClientOperations.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: jgao
ms.date: 11/15/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
schema: 2.0.0
title: Approve-CMScript
titleSuffix: Configuration Manager
---

# Approve-CMScript

## SYNOPSIS

Approves a Configuration Manager PowerShell script.

## SYNTAX

### ByScript
```
Approve-CMScript -InputObject <IResultObject> [-Comment <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByScriptId
```
Approve-CMScript -ScriptGuid <String> [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Approve-CMScript** cmdlet approves a Microsoft System Center Configuration Manager Powershell script. System Center Configuration Manager has an integrated ability to run Powershell scripts. The scripts simplify building custom tools to administer software and let you accomplish mundane tasks quickly, allowing you to get large jobs done more easily and more consistently. For more information, see [Create and run PowerShell scripts from the Configuration Manager console](https://docs.microsoft.com/sccm/apps/deploy-use/create-deploy-scripts).

You can approve a specific script by specifying the script object or the name of the script.

## EXAMPLES

### Example 1: Approve a script by using the script id

```powershell
PS XYZ:\> Approve-CMScript -ScriptGuid "DF8E7546-FD66-4A3D-A129-53AF5AA54F80"
```

This command approves a script that has the ID DF8E7546-FD66-4A3D-A129-53AF5AA54F80  .

### Example 2: Approve a script by using script object variable

```powershell
PS XYZ:\> $ScriptObj = Get-CMScript -Id "DF8E7546-FD66-4A3D-A129-53AF5AA54F80"
PS XYZ:\> Approve-CMScript -InputObject $ScriptObj
```

The first command gets a **CMScript** object that has the ID DF8E7546-FD66-4A3D-A129-53AF5AA54F80, and then stores it in the $ScriptObj variable.

The second command approves the script stored in the $ScriptObj variable.

## PARAMETERS

### -Comment

Specifies a comment about the approval of the script.

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

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

Specifies a **CMScript** object.
To obtain a **CMScript** object, use [Get-CMScript](Get-CMScript.md).

```yaml
Type: IResultObject
Parameter Sets: ByScript
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ScriptGuid

Specifies the script ID.

```yaml
Type: String
Parameter Sets: ByScriptId
Aliases:

Required: True
Position: Named
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Deny-CMScript](Deny-CMScript.md)

[Get-CMScript](Invoke-CMScript.md)

[Invoke-CMScript](Invoke-CMScript.md)

[Remove-CMScript](Remove-CMScript.md)

[Approve-CMScript](Approve-CMScript.md)

[Set-CMScriptDeploymentType](Set-CMScriptDeploymentType.md)

[Add-CMScriptDeploymentType](Add-CMScriptDeploymentType.md)
