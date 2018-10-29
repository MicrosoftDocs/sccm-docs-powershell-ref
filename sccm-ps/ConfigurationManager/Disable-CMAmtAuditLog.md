---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833939
schema: 2.0.0
ms.assetid: 09ADAA08-AF61-48EB-A923-1E931C914A83
---

# Disable-CMAmtAuditLog

## SYNOPSIS
Disables audit logging for Intel AMT-based computers.

## SYNTAX

### SearchByValueMandatory (Default)
```
Disable-CMAmtAuditLog -Device <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Disable-CMAmtAuditLog -DeviceName <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Disable-CMAmtAuditLog -DeviceId <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-CMAmtAuditLog** cmdlet disables audit logging for Intel Active Management Technology (Intel AMT)-based computers.
The audit log records authorized and authenticated out-of-band management activities performed on Intel AMT computers.

You can specify computers by using the Microsoft System Center Configuration Manager device name or device ID, or you can use the [Get-CMDevice](Get-CMDevice.md) cmdlet to get a device object.
If you want to delete the current log entries, use the [Clear-CMAmtAuditLog](Clear-CMAmtAuditLog.md) cmdlet.

## EXAMPLES

### Example 1: Disable audit logging for a device by using an ID
```
PS C:\>Disable-CMAmtAuditLog -DeviceID "16777230"
```

This command disables Intel AMT audit logging for a device that has the ID 16777230.

### Example 2: Disable audit logging for named device
```
PS C:\>Disable-CMAmtAuditLog -DeviceName "Accn023.Contoso.com"
```

This command disables Intel AMT audit logging for a device named Accn023.Contoso.com.

### Example 3: Disable audit logging by using a variable
```
PS C:\> $CMD = Get-CMDevice -Name "Accn023.Contoso.com"
PS C:\> Disable-CMAmtAuditLog -Device $CMD
```

The first command gets a device object by using the **Get-CMDevice** command, and then stores it in the $CMD variable.

The second command disables Intel AMT audit logging for the device in $CMD.
The command uses the *Force* parameter.
Therefore, it does not prompt you for confirmation.

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

### -Device
Specifies a device object.
To obtain a device object, use **Get-CMDevice**.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: InputObject
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceId
Specifies an array of IDs of devices.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: ResourceId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of names of devices.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name
Required: True
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

### -Force
Forces the command to run without asking for user confirmation.

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

[Clear-CMAmtAuditLog](Clear-CMAmtAuditLog.md)

[Enable-CMAmtAuditLog](Enable-CMAmtAuditLog.md)

[Get-CMDevice](Get-CMDevice.md)


