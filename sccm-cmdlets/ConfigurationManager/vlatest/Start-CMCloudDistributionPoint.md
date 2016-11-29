---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834207
schema: 2.0.0
ms.assetid: 0F8788AA-2C2A-4834-9CEA-9390D1E67F52
---

# Start-CMCloudDistributionPoint

## SYNOPSIS
Starts the cloud distribution point service.

## SYNTAX

### SearchByValueMandatory (Default)
```
Start-CMCloudDistributionPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Start-CMCloudDistributionPoint -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Start-CMCloudDistributionPoint -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMCloudDistributionPoint** cmdlet starts the cloud distribution point service.

You can use the Stop-CMCloudDistributionPoint cmdlet to suspend distribution of content.

## EXAMPLES

### Example 1: Start the cloud distribution point service using an ID
```
PS C:\>Start-CMCloudDistributionPoint -Id "16777242"
```

This command starts the cloud distribution point service for the cloud distribution point that has the specified identifier.

### Example 2: Start the cloud distribution point service using a name
```
PS C:\>Start-CMCloudDistributionPoint -Name "West01"
```

This command starts the cloud distribution point service for the cloud distribution point named West01.

### Example 3: Start the cloud distribution point service using an object
```
PS C:\>$DistPnt = Get-CMCloudDistributionPoint -Id "16777242"
PS C:\> Start-CMCloudDistributionPoint -InputObject $DistPnt
```

The first command uses the Get-CMCloudDistributionPoint cmdlet to get the distribution point with the specified identifier, and then saves it in the $DistPnt variable.

The second command starts the cloud distribution point service for the distribution point stored in $DistPnt.

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
You can use a comma-separated list.

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

[Remove-CMCloudDistributionPoint](./Remove-CMCloudDistributionPoint.md)

[Set-CMCloudDistributionPoint](./Set-CMCloudDistributionPoint.md)

[Stop-CMCloudDistributionPoint](./Stop-CMCloudDistributionPoint.md)


