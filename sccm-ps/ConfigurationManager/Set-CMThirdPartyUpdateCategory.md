---
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMThirdPartyUpdateCategory

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByName (Default)
```
Set-CMThirdPartyUpdateCategory [[-CatalogName] <String>] [-Id <String>] [-Name <String>] [-ParentId <String>]
 [-PublishOption <PublishOptionType>] [-EnableCategory <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValue
```
Set-CMThirdPartyUpdateCategory -InputObject <IResultObject> [-Id <String>] [-Name <String>]
 [-ParentId <String>] [-PublishOption <PublishOptionType>] [-EnableCategory <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Set-CMThirdPartyUpdateCategory [[-CatalogId] <String>] [-Id <String>] [-Name <String>] [-ParentId <String>]
 [-PublishOption <PublishOptionType>] [-EnableCategory <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByCategory
```
Set-CMThirdPartyUpdateCategory [-Category] <IResultObject[]> [-PublishOption <PublishOptionType>]
 [-EnableCategory <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -CatalogId
{{ Fill CatalogId Description }}

```yaml
Type: String
Parameter Sets: SearchById
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CatalogName
{{ Fill CatalogName Description }}

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Category
{{ Fill Category Description }}

```yaml
Type: IResultObject[]
Parameter Sets: SearchByCategory
Aliases: Categories

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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

### -EnableCategory
{{ Fill EnableCategory Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill Id Description }}

```yaml
Type: String
Parameter Sets: SearchByName, SearchByValue, SearchById
Aliases: CategoryId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Catalog

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: SearchByName, SearchByValue, SearchById
Aliases: CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentId
{{ Fill ParentId Description }}

```yaml
Type: String
Parameter Sets: SearchByName, SearchByValue, SearchById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
{{ Fill PassThru Description }}

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

### -PublishOption
{{ Fill PublishOption Description }}

```yaml
Type: PublishOptionType
Parameter Sets: (All)
Aliases:
Accepted values: Skip, MetadataOnly, FullContent

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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### IResultObject#SMS_ISVCatalogCategories

## NOTES

## RELATED LINKS
