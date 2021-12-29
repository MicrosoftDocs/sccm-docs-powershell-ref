---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Invoke-CMScript
---

# Invoke-CMScript

## SYNOPSIS

Run a PowerShell script in Configuration Manager.

## SYNTAX

### ByInputObject
```
Invoke-CMScript [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-Device <IResultObject[]>] -InputObject <IResultObject> [-PassThru] [-ScriptParameter <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByGuid
```
Invoke-CMScript [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-Device <IResultObject[]>] [-PassThru] -ScriptGuid <String> [-ScriptParameter <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to run a PowerShell script in Configuration Manager. These scripts are integrated and managed in Configuration Manager.

You can't run a script until it's approved. To approve scripts programmatically, use the [Approve-CMScript](Approve-CMScript.md) cmdlet.

For more information, see [Create and run PowerShell scripts from the Configuration Manager console](/mem/configmgr/apps/deploy-use/create-deploy-scripts).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Run a script by using its ID

This command runs the script with ID `DF8E7546-FD66-4A3D-A129-53AF5AA54F80`.

```powershell
Invoke-CMScript -ScriptGuid "DF8E7546-FD66-4A3D-A129-53AF5AA54F80"
```

### Example 2: Run a script by using an object variable

The first command gets a script object by its ID, and stores it in the **$ScriptObj** variable. The second command runs the script stored in that variable.

```powershell
$ScriptObj = Get-CMScript -Id "DF8E7546-FD66-4A3D-A129-53AF5AA54F80"

Invoke-CMScript -InputObject $ScriptObj
```

### Example 3: Pass parameters to the target script

The first line stores parameters in a hashtable. The second line runs the script on the target device, passing the parameters in the hashtable.

```powershell
$parameters = @{
  "FolderName"="c:\test\test1"
  "FileName"="test2"
}

Invoke-CMScript -ScriptGuid $scriptGuid -Device (Get-CMDevice -Name $targetPCName) -ScriptParameter $parameters
```

## PARAMETERS

### -Collection

Specify a collection object to run this script. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

Specify the ID of a collection to run this script.

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

### -CollectionName

Specify the name of a collection to run this script.

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

### -Device

Specify an object for a device to run this script. To get this object, use the [Get-CMDevice](Get-CMDevice.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Devices

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

### -InputObject

Specify a script object to run. To get this object, use the [Get-CMScript](Get-CMScript.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -ScriptGuid

Specify the ID of the script to run. The format is a standard GUID.

```yaml
Type: String
Parameter Sets: ByGuid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptParameter

Applies to version 2010 and later. Use this parameter to pass parameters to the target script. Specify a hashtable with the required parameters. For an example of usage, see [Examples](#examples).

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### System.Object

## NOTES

## RELATED LINKS

[Approve-CMScript](Approve-CMScript.md)
[Deny-CMScript](Deny-CMScript.md)
[Get-CMScript](Get-CMScript.md)
[New-CMScript](New-CMScript.md)
[Remove-CMScript](Remove-CMScript.md)
[Set-CMScript](Set-CMScript.md)

[Create and run PowerShell scripts from the Configuration Manager console](/mem/configmgr/apps/deploy-use/create-deploy-scripts)
