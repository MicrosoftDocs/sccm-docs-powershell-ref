---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833964
schema: 2.0.0
ms.assetid: 471DC886-634B-4D50-A183-5FCDFE4CED8A
---

# Remove-CMCloudDistributionPoint

## SYNOPSIS
Removes cloud-based distribution points.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMCloudDistributionPoint -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMCloudDistributionPoint -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMCloudDistributionPoint -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMCloudDistributionPoint** cmdlet removes specified cloud-based distribution points.

When you remove a distribution point, System Center Configuration Manager deletes all the content stored there.
If you want to suspend a distribution point temporarily, use the Stop-CMCloudDistributionPoint cmdlet.

## EXAMPLES

### Example 1: Remove all distribution points
```
PS C:\>Remove-CMCloudDistributionPoint
```

This command removes all the cloud distribution points from System Center Configuration Manager.
Unless you use the *Force* parameter, the cmdlet prompts you for confirmation.

### Example 2: Remove a distribution point using a name
```
PS C:\>Remove-CMCloudDistributionPoint -Name "West01"
```

This command removes the cloud distribution point named West01.
Unless you use the *Force* parameter, the cmdlet prompts you for confirmation.

### Example 3: Remove a distribution point using an ID
```
PS C:\>Remove-CMCloudDistributionPoint -Id "16777236"
```

This command removes the cloud distribution point that has the specified identifier.
Unless you use the *Force* parameter, the cmdlet prompts you for confirmation.

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
Specifies an array of identifiers for cloud distribution points.
You can use a comma separated list.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a cloud distribution point object.
To obtain a cloud distribution point object, you can use the Get-CMCloudDistributionPoint cmdlet.

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
Specifies the name of a cloud distribution point.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCloudDistributionPoint](./Get-CMCloudDistributionPoint.md)

[New-CMCloudDistributionPoint](./New-CMCloudDistributionPoint.md)

[Set-CMCloudDistributionPoint](./Set-CMCloudDistributionPoint.md)

[Start-CMCloudDistributionPoint](./Start-CMCloudDistributionPoint.md)

[Stop-CMCloudDistributionPoint](./Stop-CMCloudDistributionPoint.md)


