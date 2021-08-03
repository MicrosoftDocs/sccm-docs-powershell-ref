---
description: Gets an approval request to allow the installation of a Configuration Manager application.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMApprovalRequest
---

# Get-CMApprovalRequest

## SYNOPSIS

Gets an approval request to allow the installation of a Configuration Manager application.

## SYNTAX

### SearchByName (Default)
```
Get-CMApprovalRequest [-ApplicationName <String[]>] [-CurrentState <RequestState>] [-User <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMApprovalRequest [-CurrentState <RequestState>] -Id <String[]> [-User <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMApprovalRequest [-CurrentState <RequestState>] -InputObject <IResultObject> [-User <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByModelName
```
Get-CMApprovalRequest [-CurrentState <RequestState>] -ModelName <String> [-User <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByGuid
```
Get-CMApprovalRequest [-CurrentState <RequestState>] -RequestGuid <String> [-User <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMApprovalRequest** cmdlet gets a request from a user to install a Configuration Manager application.
You can specify an approval request by application name, application ID, or by user name.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all approval requests

```powershell
PS XYZ:\> Get-CMApprovalRequest
```

This command gets all pending Configuration Manager approval requests.

### Example 2: Get an approval request by using an application ID

```powershell
PS XYZ:\> Get-CMApprovalRequest -Id "1635223"
```

This command gets an approval request for an application with the specified ID.

### Example 3: Get an approval request for a specific user

```powershell
PS XYZ:\> Get-CMApprovalRequest -Application "HelloWorld" -User "tsqa\davidchew"
```

This command gets an approval request for the application HelloWorld for a specified user.

## PARAMETERS

### -ApplicationName

Specifies an array of names of applications.

```yaml
Type: String[]
Parameter Sets: SearchByName
Aliases: Application

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CurrentState

```yaml
Type: RequestState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Requested, Canceled, Denied, Approved

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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
Parameter Sets: SearchById
Aliases: CIUniqueId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ModelName
```yaml
Type: String
Parameter Sets: SearchByModelName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestGuid

Sepcifies the request ID.

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
Parameter Sets: (All)
Aliases:

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

### IResultObject[]#SMS_UserApplicationRequest
### IResultObject#SMS_UserApplicationRequest
## NOTES

## RELATED LINKS

[Approve-CMApprovalRequest](Approve-CMApprovalRequest.md)

[Deny-CMApprovalRequest](Deny-CMApprovalRequest.md)
