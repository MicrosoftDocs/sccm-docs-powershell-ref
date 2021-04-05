---
description: Move a Configuration Manager object into a different folder.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/26/2020
schema: 2.0.0
title: Move-CMObject
---

# Move-CMObject

## SYNOPSIS

Move a Configuration Manager object into a different folder.

## SYNTAX

### SearchByObjectMandatory (Default)
```
Move-CMObject -FolderPath <String> -InputObject <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Move-CMObject -FolderPath <String> -ObjectId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Move-CMObject** cmdlet moves a Configuration Manager object into a different folder.
Specify the object to move and the destination folder.
Because an object exists in only one folder, the cmdlet doesn't specify the current folder.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Move an app by object

This example first gets an application object by name. It then moves the object to the folder **TestFolder**.

```powershell
$app = Get-CMApplication -Name "Teams"
Move-CMObject -FolderPath "XYZ:\Application\TestFolder" -InputObject $app
```

### Example 2: Move a task sequence by ID

This example moves the task sequence with package ID **XYZ00550** to the **Development** folder.

```powershell
Move-CMObject -FolderPath "XYZ:\TaskSequence\Development" -ObjectId "XYZ00550"
```

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

### -FolderPath

Specifies a destination folder path, in the following format: `<site code>:\<object type>\folder\subfolder\subfolder`.

- `<site code>`: The Configuration Manager site code.
- `<object type>`: One of the following keywords for the type of object to move:
  - **Application**
  - **BootImage**
  - **ConfigurationBaseline**
  - **ConfigurationItem**
  - **DeviceCollection**
  - **Driver**
  - **DriverPackage**
  - **OperatingSystemImage**
  - **OperatingSystemInstaller**
  - **Package**
  - **Query**
  - **TaskSequence**
  - **UserCollection**
  - **UserStateMigration**

For example, a folder named **LOB Apps** for an application at the site CM1 has the following file path: `CM1:\Application\LOB Apps`.

To move an object to the root folder, don't specify a folder. For example, `CM1:\Application`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -InputObject

Specify an array of Configuration Manager objects to move. If you specify an array, use the same object type. Match the object type with the keyword used with the **-FolderPath** parameter.

Use one of the following cmdlets to get these objects:

- [Get-CMApplication](Get-CMApplication.md)
- [Get-CMPackage](Get-CMPackage.md)
- [Get-CMDriverPackage](Get-CMDriverPackage.md)
- [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)
- [Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)
- [Get-CMBootImage](Get-CMBootImage.md)
- [Get-CMTaskSequence](Get-CMTaskSequence.md)

```yaml
Type: IResultObject[]
Parameter Sets: SearchByObjectMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId

Specifies an array of object IDs to move. If you specify an array, use the same object type. Match the object type with the keyword used with the **-FolderPath** parameter.

For example, `XYZ00550`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: InstanceKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Lock-CMObject](Lock-CMObject.md)

[Unlock-CMObject](Unlock-CMObject.md)
