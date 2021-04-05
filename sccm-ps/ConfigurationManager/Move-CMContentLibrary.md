---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Move-CMContentLibrary

## SYNOPSIS

Use this cmdlet to move the content library before adding a passive site.

## SYNTAX

### MoveByInputObjectMandatory (Default)
```
Move-CMContentLibrary -InputObject <IResultObject> -NewLocation <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MoveBySiteCodeMandatory
```
Move-CMContentLibrary -NewLocation <String> -SiteCode <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to move the content library before adding a passive site.

## EXAMPLES

### Example 1: Move the content library for a site object

This example uses a site object to move its content library to the specified location path.

```powershell
Move-CMContentLibrary -InputObject $Site -NewLocation $NewLocationPath
```

### Example 2: Move the content library for a site code

This example uses a site code to move its content library to the specified location path.

```powershell
Move-CMContentLibrary -SiteCode $SiteCode -NewLocation $NewLocationPath
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

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

Specify a site object.

```yaml
Type: IResultObject
Parameter Sets: MoveByInputObjectMandatory
Aliases: Site

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NewLocation

Specify the network path to the new location for the content library.

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

### -SiteCode

Specify the site code.

```yaml
Type: String
Parameter Sets: MoveBySiteCodeMandatory
Aliases:

Required: True
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
