---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
ms.assetid: EE34D675-431A-4CE6-A3C0-3114CF29C023
online version: https://go.microsoft.com/fwlink/?linkid=833750
schema: 2.0.0
---

# Get-CMMdmEnrollmentManager

## SYNOPSIS
Gets a Device Enrollment Manager.

## SYNTAX

### ByName (Default)
```
Get-CMMdmEnrollmentManager [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByValue
```
Get-CMMdmEnrollmentManager -Id <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMdmEnrollmentManger** cmdlet gets one or more Device Enrollment Managers.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get a device enrollment manager by name
```
PS XYZ:\> Get-CMMdmEnrollmentManager -name "Contoso\User01"
```

This command gets the device enrollment manager named User01.

### Example 2: Get a device enrollment manager by ID
```
PS XYZ:\> Get-CMMdmEnrollmentManager -ID "1234567890"
```

This command gets the device enrollment manager named 1234567890.

## PARAMETERS

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
Specifies an array of Configuration Manager user IDs.

```yaml
Type: Int32[]
Parameter Sets: ByValue
Aliases: Ids, ResourceId, ResourceIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a Configuration Manager user.

```yaml
Type: String
Parameter Sets: ByName
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

### IResultObject#SMS_MDMDeviceEnrollmentManagers

## NOTES

## RELATED LINKS

[Add-CMMdmEnrollmentManager](Add-CMMdmEnrollmentManager.md)

[Remove-CMMdmEnrollmentManager](Remove-CMMdmEnrollmentManager.md)


