---
external help file: AdminUI.PS.AppModel.dll-Help.xml
ms.assetid: FFCE8AD9-01ED-42FC-9638-D74CA31F453A
online version: https://go.microsoft.com/fwlink/?linkid=833710
schema: 2.0.0
---

# Get-CMGlobalCondition

## SYNOPSIS
Gets global condition objects.

## SYNTAX

### SearchByName (Default)
```
Get-CMGlobalCondition [-Name <String>] [-AsDcmSdkObject] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMGlobalCondition -Id <String> [-AsDcmSdkObject] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMGlobalCondition** cmdlet gets global condition objects.
You can pass the results of this cmdlet to the **Set-CMGlobalCondition** cmdlet or the **Remove-CMGlobalCondition** cmdlet.

Microsoft System Center Configuration Manager uses global conditions to represent business or technical conditions.
Global conditions specify how to provide and deploy applications to client devices.

You can get global conditions by name, ID, or security scope.
You can also specify one or more security scope names with either names or IDs.
For instance, you might specify an array of global condition names and specify a security scope to narrow your results.

## EXAMPLES

### Example 1: Get a global condition by name
```
PS C:\> Get-CMGlobalCondition -Name "CPU speed"
```

This command gets the global condition named CPU speed.

### Example 2: Get a global condition by name and security scope
```
PS C:\> Get-CMGlobalCondition -Name "CPU speed" -SecuredScopeNames "Scope22"
```

This command gets the global condition named CPU speed that has a security scope named Scope22.

## PARAMETERS

### -AsDcmSdkObject
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

### -Id
Specifies an array of identifiers of global conditions.
This value corresponds to the **CI_ID** property of a global condition object.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names for global conditions.
This value corresponds to the **LocalizedDisplayName** property of a global condition object.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMGlobalCondition](New-CMGlobalCondition.md)

[Remove-CMGlobalCondition](Remove-CMGlobalCondition.md)

[Set-CMGlobalCondition](Set-CMGlobalCondition.md)


