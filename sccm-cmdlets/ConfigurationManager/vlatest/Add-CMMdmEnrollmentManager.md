---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833708
schema: 2.0.0
ms.assetid: 63BCD25A-C343-463F-820A-B3668CB7B22E
---

# Add-CMMdmEnrollmentManager

## SYNOPSIS
Adds a Device Enrollment Manager.

## SYNTAX

### ByValue (Default)
```
Add-CMMdmEnrollmentManager -InputObject <IResultObject[]> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Add-CMMdmEnrollmentManager -Id <Int32[]> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMMdmEnrollmentManager -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMMdmEnrollmentManager** cmdlet adds a Device Enrollment Manager to the Microsoft Intune subscription.

## EXAMPLES

### Example 1: Add a device enrollment manager using the pipeline
```
PS C:\> Get-CMUser -Name "Contoso\User01" | Add-CMMdmEnrollmentManager
```

This command gets the user object named User01 and uses the pipeline operator to pass the object to **Add-CMMdmEnrollmentManager**, which adds the user as a device enrollment manager.

### Example 2: Add a device enrollment manager by name
```
PS C:\> Add-CMMdmEnrollmentManager -Name "Contoso\User02"
```

This command adds the user named User02 as a device enrollment manager.

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
Specifies an array of Configuration Manager user IDs.

```yaml
Type: Int32[]
Parameter Sets: ById
Aliases: Ids
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an array of user objects.
To obtain a user object, use the Get-CMUser cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: User, EnrollmentManager, Users, EnrollmentManagers
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a Configuration Manager user.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### IResultObject#SMS_MDMDeviceEnrollmentManagers

## NOTES

## RELATED LINKS

[Get-CMMdmEnrollmentManager](./Get-CMMdmEnrollmentManager.md)

[Get-CMUser](./Get-CMUser.md)

[Remove-CMMdmEnrollmentManager](./Remove-CMMdmEnrollmentManager.md)


