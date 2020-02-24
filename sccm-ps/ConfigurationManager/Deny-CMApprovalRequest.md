---
author: aczechowski
description: Denies a request to allow the installation of an application.
external help file: AdminUI.PS.AppModel.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Deny-CMApprovalRequest
titleSuffix: Configuration Manager
---

# Deny-CMApprovalRequest

## SYNOPSIS

Denies a request to allow the installation of an application.

## SYNTAX

### SearchByValueMandatory (Default)
```
Deny-CMApprovalRequest -InputObject <IResultObject> [-Comment <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Deny-CMApprovalRequest -Id <String[]> [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Deny-CMApprovalRequest -ApplicationName <String[]> -User <String> [-Comment <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByGuid
```
Deny-CMApprovalRequest -RequestGuid <String> [-Comment <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Deny-CMApprovalRequest** cmdlet denies a request from a user to install an application.
You can specify an approval request by application name, application ID, or by user.
You can use the [Get-CMApprovalRequest](Get-CMApprovalRequest.md) cmdlet to view approval requests.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Deny a request by application ID

```powershell
PS XYZ:\>Deny-CMApprovalRequest -Id "ScopeId_2A11048C-917A-4C11-9E77-7DCC402F30EC/Application_426dfca1-0cc0-4aa3-85f8-3cd1b184d494/1" -Comment "All requests for this application are denied."
```

This command denies a request for an application that has the specified ID.
The command includes a comment.

### Example 2: Deny a request from a specific user

```powershell
PS XYZ:\>Deny-CMApprovalRequest -Application "Test" -User "tsqa\davidchew"
```

This command denies a request for an application named Test for the specified user.

### Example 3: Deny a request by using a variable

```powershell
PS XYZ:\> $Approval = Get-CMApprovalRequest -Id "ScopeId_2A11048C-917A-4C11-9E77-7DCC402F30EC/Application_426dfca1-0cc0-4aa3-85f8-3cd1b184d494/1"
PS XYZ:\> Deny-CMApprovalRequest -InputObject $Approval -Comment "Request denied."
```

The first command gets an approval request for a specified application ID and stores it in the $Approval variable.

The second command denies the request stored in $Approval.
The command includes a comment.

## PARAMETERS

### -ApplicationName

Specifies an array of names of applications.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory
Aliases: Application, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment

Specifies a comment about the denial of the request.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

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

### -Id

Specifies an array of IDs of applications.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: CIUniqueId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies an approval request object.
To obtain an approval request object, use the [Get-CMApprovalRequest](Get-CMApprovalRequest.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RequestGuid

Specifies the request ID.

```yaml
Type: String
Parameter Sets: SearchByGuid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -User

Specifies an array of user names of persons who submitted the approval request.
Use the format domain\user.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Approve-CMApprovalRequest](Approve-CMApprovalRequest.md)

[Get-CMApprovalRequest](Get-CMApprovalRequest.md)
