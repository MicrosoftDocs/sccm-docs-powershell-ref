---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833886
schema: 2.0.0
ms.assetid: D4DBB01E-986C-4B70-B24C-0F477791386B
---

# Remove-CMAmtProvisioningData

## SYNOPSIS
Removes provisioning information for an Intel AMT computer.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMAmtProvisioningData -Device <IResultObject> -ControlType <RemoteControlType> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMAmtProvisioningData -DeviceName <String> -ControlType <RemoteControlType> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMAmtProvisioningData -DeviceId <String> -ControlType <RemoteControlType> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAmtProvisioningData** cmdlet removes the Microsoft System Center Configuration Manager provisioning information for an Intel Active Management Technology (Intel AMT)-based computer.
You might want to remove provisioning information when you no longer want to manage a computer out of band by using System Center Configuration Manager.

You can either remove all configuration data or retain identification information about the computer, such as its host name, IP address, and DNS suffix.

By default, System Center Configuration Manager automatically reprovisions Intel AMT-based computers if you have configured Intel AMT provisioning.
Use the *ControlType* parameter to control reprovisioning for individual computers.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Remove provisioning information completely for a specified computer
```
PS XYZ:\> Remove-CMAmtProvisioningData -ControlType FullUnprovisionSuppressAuto -DeviceId "SMS000076" -Force
```

This command removes provisioning information from a computer that has the ID SMS000076.
The cmdlet removes all provisioning data and suppresses automatic reprovisioning.
The command specifies the *Force* parameter.
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

### -ControlType
Specifies how Configuration Manager removes provisioning information.
This parameter controls whether the cmdlet removes some or all provisioning information.
This parameter also determines whether the cmdlet allows Configuration Manager to reprovision an Intel AMT-based computer later.

The acceptable values for this parameter are:

- FullUnprovision.
Resets Intel AMT to the factory default settings.
- FullUnprovisionSuppressAuto.
Resets Intel AMT to the factory default settings and does not allow Configuration Manager to reprovision the computer.
- KerberosFullUnprovision.
Resets Intel AMT for Kerberos-enabled computers to factory default settings.
- KerberosFullUnprovisionSuppressAuto.
Resets Intel AMT for Kerberos-enabled computers to factory default settings, and does not allow Configuration Manager to reprovision the computer.
- KerberosPartialUnprovision.
Resets Intel AMT for Kerberos-enabled computers except for identification information about the computer.
- KerberosPartialUnprovisionSuppressAuto.
Resets Intel AMT for Kerberos-enabled computers except for identification information about the computer, and does not allow Configuration Manager to reprovision the computer.
- PartialUnprovision.
Resets Intel AMT to the factory default settings, except for identification information about the computer.
- PartialUnprovisionSuppressAuto.
Resets Intel AMT to the factory default settings, except for identification information about the computer, and does not allow Configuration Manager to reprovision the computer.

```yaml
Type: RemoteControlType
Parameter Sets: (All)
Aliases: 
Accepted values: DiscoveryBmc, PartialUnprovision, FullUnprovision, FullUnprovisionSuppressAuto, PartialUnprovisionSuppressAuto, KerberosFullUnprovision, KerberosFullUnprovisionSuppressAuto, KerberosPartialUnprovision, KerberosPartialUnprovisionSuppressAuto, Unsuppress, EnableAudit, DisableAudit, ClearAuditLog
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Device
Specifies a device object.
To obtain a device object, use the **Get-CMDevice** cmdlet.

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

The acceptable values for this parameter are:

- FullUnprovision.
Resets Intel AMT to the factory default settings.
- FullUnprovisionSuppressAuto.
Resets Intel AMT to the factory default settings and does not allow Configuration Manager to reprovision the computer.
- KerberosFullUnprovision.
Resets Intel AMT for Kerberos-enabled computers to factory default settings.
- KerberosFullUnprovisionSuppressAuto.
Resets Intel AMT for Kerberos-enabled computers to factory default settings, and does not allow Configuration Manager to reprovision the computer.
- KerberosPartialUnprovision.
Resets Intel AMT for Kerberos-enabled computers except for identification information about the computer.
- KerberosPartialUnprovisionSuppressAuto.
Resets Intel AMT for Kerberos-enabled computers except for identification information about the computer, and does not allow Configuration Manager to reprovision the computer.
- PartialUnprovision.
Resets Intel AMT to the factory default settings, except for identification information about the computer.
- PartialUnprovisionSuppressAuto.
Resets Intel AMT to the factory default settings, except for identification information about the computer, and does not allow Configuration Manager to reprovision the computer.

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

[Invoke-CMAmtProvisioningDiscovery](Invoke-CMAmtProvisioningDiscovery.md)

[Update-CMAMTProvisioning](Update-CMAMTProvisioning.md)

[Get-CMDevice](Get-CMDevice.md)


