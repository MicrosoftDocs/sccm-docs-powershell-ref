---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/03/2022
online version:
schema: 2.0.0
---

# Move-CMContentLibrary

## SYNOPSIS

Move the content library before adding a passive site.

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

Use this cmdlet to move the content library. To configure site server high availability or to free up hard drive space on your central administration or primary site servers, relocate the content library to another storage location. For more information, see [Configure a remote content library for the site server](/mem/configmgr/core/plan-design/hierarchy/remote-content-library).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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

Specify a site object. To get this object, use the [Get-CMSite](Get-CMSite.md) cmdlet.

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

[Get-CMSite](Get-CMSite.md)

[Configure a remote content library for the site server](/mem/configmgr/core/plan-design/hierarchy/remote-content-library)
