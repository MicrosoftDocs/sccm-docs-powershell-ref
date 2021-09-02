---
description: Approves a request to allow the installation of an application.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/29/2019
schema: 2.0.0
title: Approve-CMApprovalRequest
---

# Approve-CMApprovalRequest

## SYNOPSIS

Approves a request to allow the installation of an application.

## SYNTAX

### SearchByValueMandatory (Default)
```
Approve-CMApprovalRequest [-Comment <String>] -InputObject <IResultObject>
 [-InstallActionBehavior <ActionBehavior>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Approve-CMApprovalRequest -ApplicationName <String[]> [-Comment <String>]
 [-InstallActionBehavior <ActionBehavior>] -User <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Approve-CMApprovalRequest [-Comment <String>] -Id <String[]> [-InstallActionBehavior <ActionBehavior>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByGuid
```
Approve-CMApprovalRequest [-Comment <String>] [-InstallActionBehavior <ActionBehavior>] -RequestGuid <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Approve-CMApprovalRequest** cmdlet approves a request from a user to install an application.
You can specify an approval request by application name, application ID, or by user.
You can also use the [Get-CMApprovalRequest](Get-CMApprovalRequest.md) cmdlet to view approval requests.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Approve a request for a specific application

```powershell
PS XYZ:\>Approve-CMApprovalRequest -Id "ScopeId_2A11048C-917A-4C11-9E77-7DCC402F30EC/Application_426dfca1-0cc0-4aa3-85f8-3cd1b184d494/1"
```

This command approves a request from a user to install an application specified by its ID.

### Example 2: Approve a request for a specific user

```powershell
PS XYZ:\>Approve-CMApprovalRequest -Application "Test" -User "tsqa\davidchew" -Comment "Request approved."
```

This command approves a request for an application named Test for the specified user. The command includes a comment.

### Example 3: Approve a request by using a variable

```powershell
PS XYZ:\> $Approval = Get-CMApprovalRequest -Id "ScopeId_2A11048C-917A-4C11-9E77-7DCC402F30EC/Application_d047e945-d6af-46f4-910f-ed36c880ae06/1"
PS XYZ:\> Approve-CMApprovalRequest -InputObject $Approval -Comment "Request approved."
```

The first command gets an approval request for a specified application ID and stores it in the variable `$Approval`.

The second command accepts the request stored in `$Approval`. The command includes a comment.

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

### -DisableWildcardHandling

DisableWildcardHandling treats wildcard characters as literal character values. Don't combine with **ForceWildcardHandling**.

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

ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Don't combine with **DisableWildcardHandling**.

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

Specifies an approval request object. To obtain an approval request object, use the [Get-CMApprovalRequest](Get-CMApprovalRequest.md) cmdlet.

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

### -InstallActionBehavior

Specifies when to install the application, either right away or during non-business hours.

```yaml
Type: ActionBehavior
Parameter Sets: (All)
Aliases:
Accepted values: InstallNow, InstallNonBusinessHours

Required: False
Position: Named
Default value: InstallNow
Accept pipeline input: False
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

Specifies the name of a user who submitted the approval request. Use the format **domain\user**.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't make any changes.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Deny-CMApprovalRequest](Deny-CMApprovalRequest.md)

[Get-CMApprovalRequest](Get-CMApprovalRequest.md)
