---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834076
schema: 2.0.0
ms.assetid: FBC76C13-CA04-4B44-BC77-35E93E8A5358
---

# Remove-CMDistributionPointGroup

## SYNOPSIS
Removes distribution point groups.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMDistributionPointGroup -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMDistributionPointGroup -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMDistributionPointGroup -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDistributionPointGroup** cmdlet removes one or more distribution point groups.
When you remove a distribution point group, you cannot use the distribution point group to distribute content to the site collections that are associated with the distribution point group and to the distribution points that are members of the distribution point group.

## EXAMPLES

### Example 1: Remove a distribution point group by using an ID
```
PS C:\>Remove-CMDistributionPointGroup -Id "{03BCD6FE-5604-4725-B650-DD1EA03676DE}"
```

This command removes the distribution point group that has the ID 03BCD6FE-5604-4725-B650-DD1EA03676DE.

### Example 2: Remove a distribution point group by using a name
```
PS C:\>Remove-CMDistributionPointGroup -Name "DpgDept01"
```

This command removes the distribution point group named DpgDept01.

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

### -Id
Specifies an array of IDs of distribution point groups.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: GroupId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMDistributionPointGroup** object.
To obtain a **CMDistributionPointGroup** object, use the [Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a distribution point group.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

### Specifies an array of names of distribution point groups.

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMDistributionPointGroup](./New-CMDistributionPointGroup.md)

[Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md)

[Set-CMDistributionPointGroup](./Set-CMDistributionPointGroup.md)


