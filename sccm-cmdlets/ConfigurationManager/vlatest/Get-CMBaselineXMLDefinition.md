---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834142
schema: 2.0.0
ms.assetid: 73C221D9-2219-4362-A22C-69D65EA490F5
---

# Get-CMBaselineXMLDefinition

## SYNOPSIS
Gets the XML definition of a configuration baseline.

## SYNTAX

### SearchByName (Default)
```
Get-CMBaselineXMLDefinition [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBaselineXMLDefinition [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMBaselineXMLDefinition [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBaselineXMLDefinition** cmdlet gets and displays the XML definition of one or more baseline configurations.

## EXAMPLES

### Example 1: Get a configuration baseline XML definition
```
PS C:\>$CIObj = Get-CMBaseline -Id "16777568"
PS C:\> Get-CMBaselineXMLDefinition -InputObject $CIObj
```

The first command gets the configuration baseline object that has the ID 16777568, and stores the object in the $CIObj variable.

The second command gets the XML definition of the configuration baseline stored in $CIObj.

## PARAMETERS

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
Specifies an array of IDs of baseline configurations.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMBaseline** object.
To obtain a **CMBaseline** object, use the Get-CMBaseline cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of baseline configuration names.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName
Required: False
Position: 0
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

[Get-CMBaseline](./Get-CMBaseline.md)


