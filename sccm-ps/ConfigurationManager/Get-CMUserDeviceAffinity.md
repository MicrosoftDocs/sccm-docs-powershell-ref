---
description: Get the relationships between a device and its primary users.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/14/2021
schema: 2.0.0
title: Get-CMUserDeviceAffinity
---

# Get-CMUserDeviceAffinity

## SYNOPSIS

Get the relationships between a device and its primary users.

## SYNTAX

### SearchByUserNameMandatory (Default)
```
Get-CMUserDeviceAffinity -UserName <String[]> [-ShowApprovedOnly] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Get-CMUserDeviceAffinity -DeviceId <Int32[]> [-ShowApprovedOnly] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Get-CMUserDeviceAffinity -DeviceName <String[]> [-ShowApprovedOnly] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByUserIdMandatory
```
Get-CMUserDeviceAffinity -UserId <Int32[]> [-ShowApprovedOnly] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMUserDeviceAffinity** cmdlet gets one or more user device affinities in Configuration Manager. User device affinities are the relationships between a device and its primary users. For more information, see [Link users and devices with user device affinity in Configuration Manager](/mem/configmgr/apps/deploy-use/link-users-and-devices-with-user-device-affinity).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get user device affinities by user name

This command gets any user device affinities for the user **contoso\jqpublic**.

```powershell
Get-CMUserDeviceAffinity -UserName "contoso\jqpublic"
```

### Example 2: Get devices for a given user

This example is similar to the first, but reduces the returned list of attributes with the **Select-Object** cmdlet. You can use this example to quickly find which devices a specific user regularly uses. This example shows the output in this modified format.

```powershell
PS XYZ:\> $user = "contoso\jqpublic"
PS XYZ:\> Get-CMUserDeviceAffinity -UserName $user | Select-Object ResourceName
ResourceName
------------
PUYALLUP01
KULSHAN02
TAHOMA42
```

### Example 3: Get user device affinities by user ID

This command gets any user device affinities for the user with the resource ID **2063597981**.

```powershell
Get-CMUserDeviceAffinity -UserID "2063597981"
```

### Example 4: Get a user device affinity for a device name

This command gets the user device affinity for the device named **CMCEN-DIST02**.

```powershell
Get-CMUserDeviceAffinity -DeviceName "CMCEN-DIST02"
```

### Example 5: Get a user device affinity for a device ID

This command gets the user device affinity for the device with resource ID **16780642**.

```powershell
Get-CMUserDeviceAffinity -DeviceID "16780642"
```

### Example 6: Get primary users for a list of devices

This script sample displays the primary user for an imported list of devices. One method to get this list is from the Configuration Manager console, in the **Devices** node, multi-select multiple rows, and copy the text (**Ctrl** + **V**). Paste the data into a plain text file, replace the tab characters as commas (`,`), and then save it as **computers.csv**.

```powershell
$computers = Import-Csv -Path "C:\Users\jqpublic\computers.csv"

foreach ( $computer in $computers )
{
  $uda = Get-CMUserDeviceAffinity -DeviceName $computer.Name
  
  if ( ($uda.UniqueUserName).count -gt 1 )
  {
    foreach ( $user in $uda.UniqueUserName )
    {
      Write-Host $uda.ResourceName[1] $user
    }
  }
  else
  {
    write-host $uda.ResourceName $uda.UniqueUserName
  }
}
```

The script sample uses the Import-Csv cmdlet to take input from a comma-separated list that has a **Name** column for the device name.

- The first `foreach` command loops through each line from the comma-separated file. It uses the **Get-CMUserDeviceAffinity** cmdlet to get the primary users for that device.
- If there are more than one primary users of the device, then it writes the computer name and each user on a separate line.
- If there is only one primary user of the device, it writes the computer name and the user.
- The output of the script is a simple list of computer names and associated primary user names.

## PARAMETERS

### -DeviceId

Specify an array of device resource IDs to get their primary users.

```yaml
Type: Int32[]
Parameter Sets: SearchByDeviceIdMandatory
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName

Specify an array of device names.

```yaml
Type: String[]
Parameter Sets: SearchByDeviceNameMandatory
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

### -ShowApprovedOnly

Add this parameter to filter out non-approved affinities.

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

### -UserId

Specifies an array of user resource IDs. Use this parameter to get any devices for which this user is the primary user.

```yaml
Type: Int32[]
Parameter Sets: SearchByUserIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName

Specify an array of user names. Use this parameter to get any devices for which this user is the primary user.

```yaml
Type: String[]
Parameter Sets: SearchByUserNameMandatory
Aliases: UniqueUserName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_UserMachineRelationship

### IResultObject#SMS_UserMachineRelationship

## NOTES

For more information on this return object and its properties, see [SMS_UserMachineRelationship server WMI class](/mem/configmgr/develop/reference/core/clients/manage/sms_usermachinerelationship-server-wmi-class).

## RELATED LINKS

[Approve-CMUserDeviceAffinityRequest](Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](Deny-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinityRequest](Get-CMUserDeviceAffinityRequest.md)

[Import-CMUserDeviceAffinity](Import-CMUserDeviceAffinity.md)

[Link users and devices with user device affinity in Configuration Manager](/mem/configmgr/apps/deploy-use/link-users-and-devices-with-user-device-affinity)
