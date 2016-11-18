---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: F564E6AA-E38D-4F5A-B030-2A71844EFF6D
---

# Get-CMApprovalRequest

## SYNOPSIS
Gets a request to allow the installation of an application.

## SYNTAX

### SearchByName (Default)
```
Get-CMApprovalRequest [-ApplicationName <String[]>] [-User <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMApprovalRequest -Id <String[]> [-User <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByModelName
```
Get-CMApprovalRequest [-User <String>] -ModelName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMApprovalRequest [-User <String>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMApprovalRequest** cmdlet gets a request from a user to install an application.
You can specify an approval request by application name, application ID, or by user name.

## EXAMPLES

### Example 1: Get all approval requests
```
PS C:\>Get-CMApprovalRequest
```

This command gets all pending Microsoft System Center Configuration Manager approval requests.

### Example 2: Get an approval request by using an application ID
```
PS C:\>Get-CMApprovalRequest -Id "1635223"
```

This command gets an approval request for an application with the specified ID.

### Example 3: Get an approval request for a specific user
```
PS C:\>Get-CMApprovalRequest -Application "HelloWorld" -User "tsqa\davidchew"
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Approve-CMApprovalRequest](./Approve-CMApprovalRequest.md)

[Deny-CMApprovalRequest](./Deny-CMApprovalRequest.md)


