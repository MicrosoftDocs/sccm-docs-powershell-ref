---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: 1343FB22-DB1A-4CBC-A26B-DFED53CF00A1
online version: https://go.microsoft.com/fwlink/?linkid=833770
schema: 2.0.0
---

# New-CMSoftwareUpdateGroup

## SYNOPSIS
Creates a software update group.

## SYNTAX

```
New-CMSoftwareUpdateGroup -Name <String> [-Description <String>] [-UpdateId <Int32[]>]
 [-SoftwareUpdateId <String[]>] [-SoftwareUpdateName <String[]>] [-InputObject <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSoftwareUpdateGroup** cmdlet creates a software update group for Microsoft System Center Configuration Manager.
A software update group is a collection of one or more software updates.
You can add software updates to a software update group and then deploy the group to clients.
After you deploy a software update group, you can add new software updates to the group and System Center Configuration Manager automatically deploys them.

## EXAMPLES

### Example 1: Create a software update group
```
PS C:\> New-CMSoftwareUpdateGroup -Name "ClientUpdateGroup01" -UpdateID 100027 -Description "Client software update group 01 for Accounts Payable"
```

This command creates a software update group named ClientUpdateGroup01 that includes the software update that has the update ID 100027.

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

### -Description
Specifies a description of a software update group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

Required: False
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
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SoftwareUpdates, SoftwareUpdate

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a software update group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateId
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SoftwareUpdateIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SoftwareUpdateNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateId
Specifies an array of IDs of software updates.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: Updates

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

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)

[Remove-CMSoftwareUpdateGroup](Remove-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdateGroup](Set-CMSoftwareUpdateGroup.md)


