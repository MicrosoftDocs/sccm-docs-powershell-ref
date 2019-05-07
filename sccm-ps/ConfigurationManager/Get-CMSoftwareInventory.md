---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
ms.assetid: A94D2654-D7A1-41D1-AA53-C6DD0E346891
online version: https://go.microsoft.com/fwlink/?linkid=833889
schema: 2.0.0
---

# Get-CMSoftwareInventory

## SYNOPSIS
Retrieves an object that collects software inventory data in Configuration Manager.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareInventory [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareInventory -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareInventory** cmdlet retrieves an object that collects information about files that client devices contain.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get a software inventory object
```
PS XYZ:\> Get-CMSoftwareInventory -Name "MSXML 6.0 Parser"
```

This command gets the software inventory object named MSXML 6.0 Parser.

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
Specifies an array of IDs of software files.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: SoftwareKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software files.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CommonName

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

[Set-CMSoftwareInventory](Set-CMSoftwareInventory.md)

[Undo-CMSoftwareInventory](Undo-CMSoftwareInventory.md)


