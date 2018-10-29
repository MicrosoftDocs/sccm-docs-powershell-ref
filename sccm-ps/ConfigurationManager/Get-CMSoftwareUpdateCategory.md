---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-CMSoftwareUpdateCategory

## SYNOPSIS
Gets a software update category

## SYNTAX

### ByName (Default)
```
Get-CMSoftwareUpdateCategory [-Name <String>] [-TypeName <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMSoftwareUpdateCategory -Id <String> [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByUniqueId
```
Get-CMSoftwareUpdateCategory -UniqueId <String> [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
```

 

## PARAMETERS

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

### -Fast
 

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
 

```yaml
Type: String
Parameter Sets: ById
Aliases: CategoryInstanceID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
 

```yaml
Type: String
Parameter Sets: ByName
Aliases: LocalizedCategoryInstanceName, CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeName
 

```yaml
Type: String
Parameter Sets: ByName
Aliases: CategoryTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UniqueId
 

```yaml
Type: String
Parameter Sets: ByUniqueId
Aliases: CategoryInstance_UniqueID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_UpdateCategoryInstance
IResultObject#SMS_UpdateCategoryInstance

## NOTES

## RELATED LINKS

