---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833927
schema: 2.0.0
ms.assetid: 4DC33097-C090-407F-A8D8-1542C6A9A952
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

## DESCRIPTION
The **Deny-CMApprovalRequest** cmdlet denies a request from a user to install an application.
You can specify an approval request by application name, application ID, or by user.
You can use the [Get-CMApprovalRequest](./Get-CMApprovalRequest.md) cmdlet to view approval requests.

## EXAMPLES

### Example 1: Deny a request by application ID
```
PS C:\>Deny-CMApprovalRequest -Id "ScopeId_2A11048C-917A-4C11-9E77-7DCC402F30EC/Application_426dfca1-0cc0-4aa3-85f8-3cd1b184d494/1" -Comment "All requests for this application are denied."
```

This command denies a request for an application that has the specified ID.
The command includes a comment.

### Example 2: Deny a request from a specific user
```
PS C:\>Deny-CMApprovalRequest -Application "Test" -User "tsqa\davidchew"
```

This command denies a request for an application named Test for the specified user.

### Example 3: Deny a request by using a variable
```
PS C:\> $Approval = Get-CMApprovalRequest -Id "ScopeId_2A11048C-917A-4C11-9E77-7DCC402F30EC/Application_426dfca1-0cc0-4aa3-85f8-3cd1b184d494/1"
PS C:\> Deny-CMApprovalRequest -InputObject $Approval -Comment "Request denied."
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
To obtain an approval request object, use the [Get-CMApprovalRequest](./Get-CMApprovalRequest.md) cmdlet.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Approve-CMApprovalRequest](./Approve-CMApprovalRequest.md)

[Get-CMApprovalRequest](./Get-CMApprovalRequest.md)


