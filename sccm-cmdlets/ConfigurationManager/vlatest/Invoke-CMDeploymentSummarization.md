---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834121
schema: 2.0.0
ms.assetid: A2A4F695-E2B3-4869-8235-B9486C9CB4EB
---

# Invoke-CMDeploymentSummarization

## SYNOPSIS
Runs a Configuration Manager deployment summarization.

## SYNTAX

### SearchByIdMandatory (Default)
```
Invoke-CMDeploymentSummarization -DeploymentId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMDeploymentSummarization -CollectionName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMDeploymentSummarization -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMDeploymentSummarization** cmdlet runs a Microsoft System Center Configuration Manager deployment summarization as soon as possible.
Summarization compiles information about current deployment of software from the Configuration Manager site database.
By default, Configuration Manager runs this summarization every four hours.
If you use this cmdlet to create the summarization immediately, it does not interfere with the regular schedule of creating the current summarization.

You can specify a deployment summarization by ID or by collection or you can specify a deployment summarization object.

## EXAMPLES

### Example 1: Invoke a deployment summarization
```
PS C:\>Invoke-CMDeploymentSummarization -CollectionName "CMWest"
```

This command runs a deployment summarization for the collection named CMWest.

## PARAMETERS

### -CollectionName
Specifies a name of a collection.

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

### -DeploymentId
Specifies an ID of a deployment.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 
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

### -InputObject
Specifies a deployment summarization object.

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


