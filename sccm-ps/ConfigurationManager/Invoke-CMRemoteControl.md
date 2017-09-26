---
external help file: AdminUI.PS.Oob.dll-Help.xml
ms.assetid: 072CB4A9-2915-4126-99E2-A595A94C57F4
online version: https://go.microsoft.com/fwlink/?linkid=834157
schema: 2.0.0
---

# Invoke-CMRemoteControl

## SYNOPSIS
Enables remote control on computers.

## SYNTAX

### InvokeDeviceByValueMandatory (Default)
```
Invoke-CMRemoteControl -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeSiteStatusByNameMandatory
```
Invoke-CMRemoteControl -SiteSystemServerName <String> [-SiteSystemRole <String>] [-SiteCode <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeDeviceByNameMandatory
```
Invoke-CMRemoteControl -DeviceName <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeDeviceByIdMandatory
```
Invoke-CMRemoteControl -DeviceId <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMRemoteControl** cmdlet enables remote control on the computers that you want to use in a remote control session.
You can enable remote control on computers by specifying the ID or name of the computers, the site systems, or the site status.

Use remote control in Microsoft System Center Configuration Manager to remotely administer, provide assistance, or view any client computer in the hierarchy.
You can use remote control to troubleshoot hardware and software configuration problems on client computers and to provide help desk support when access to the computer of a user is required.
System Center Configuration Manager supports the remote control of workgroup computers and computers that are joined to an Active Directory domain.

## EXAMPLES

### Example 1: Enable remote control on a computer
```
PS C:\>Invoke-CMRemoteControl -DeviceName "CMCEN-DIST02"
```

This command enables remote control on the computer named CMCEN-DIST02.

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

### -DeviceId
Specifies an array of device IDs.

```yaml
Type: String
Parameter Sets: InvokeDeviceByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of device names.

```yaml
Type: String
Parameter Sets: InvokeDeviceByNameMandatory
Aliases: 

Required: True
Position: Named
Default value: None
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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: InvokeDeviceByValueMandatory
Aliases: Device, SiteStatus

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
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

### -SiteCode
Specifies an array of site codes of Configuration Manager sites that host the site system roles.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemRole
Specifies an array of Configuration Manager roles that the site system performs.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
Aliases: Role

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies an array of fully qualified domain names (FQDN) of the servers that host the site system roles.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
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

[Get-CMDevice](Get-CMDevice.md)

[Get-CMSiteStatusMessage](Get-CMSiteStatusMessage.md)
