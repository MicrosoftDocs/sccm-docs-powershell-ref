---
title: Approve-CMApprovalRequest
titleSuffix: Configuration Manager
description: Approves a request to allow the installation of an application.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Approve-CMApprovalRequest

## SYNOPSIS

Approves a request to allow the installation of an application.

## SYNTAX

### SearchByValueMandatory (Default)

```powershell
Approve-CMApprovalRequest [-Comment <String>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory

```powershell
Approve-CMApprovalRequest -ApplicationName <String[]> [-Comment <String>] -User <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory

```powershell
Approve-CMApprovalRequest [-Comment <String>] -Id <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByGuid

```powershell
Approve-CMApprovalRequest [-Comment <String>] -RequestGuid <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Approve-CMApprovalRequest** cmdlet approves a request from a user to install an application.
You can specify an approval request by application name, application ID, or by user.
You can also use the [Get-CMApprovalRequest](Get-CMApprovalRequest.md) cmdlet to view approval requests.

## EXAMPLES

### Example 1: Approve a request for a specific application

```powershell
PS C:\>Approve-CMApprovalRequest -Id "ScopeId_2A11048C-917A-4C11-9E77-7DCC402F30EC/Application_426dfca1-0cc0-4aa3-85f8-3cd1b184d494/1"
```

This command approves a request from a user to install an application specified by its ID.

### Example 2: Approve a request for a specific user

```powershell
PS C:\>Approve-CMApprovalRequest -Application "Test" -User "tsqa\davidchew" -Comment "Request approved."
```

This command approves a request for an application named Test for the specified user.
The command includes a comment.

### Example 3: Approve a request by using a variable

```powershell
PS C:\> $Approval = Get-CMApprovalRequest -Id "ScopeId_2A11048C-917A-4C11-9E77-7DCC402F30EC/Application_d047e945-d6af-46f4-910f-ed36c880ae06/1"
PS C:\> Approve-CMApprovalRequest -InputObject $Approval -Comment "Request approved."
```

The first command gets an approval request for a specified application ID and stores it in the variable $Approval.

The second command accepts the request stored in $Approval.
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

Specifies a comment about the approval of the request.

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

Specifies the name of a user who submitted the approval request.
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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Deny-CMApprovalRequest](Deny-CMApprovalRequest.md)

[Get-CMApprovalRequest](Get-CMApprovalRequest.md)
