---
---

# New-CMGlobalConditionXPathQuery

## SYNOPSIS

{{Fill in the Synopsis}}

## SYNTAX

### NewQueryFromFile (Default)

```
New-CMGlobalConditionXPathQuery -DataType <GlobalConditionDataType> -XmlFilePath <String>
 -XPathQueryFilePath <String> [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] [-XmlNamespace <String[]>]
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

### NewQueryFromText

```
New-CMGlobalConditionXPathQuery -DataType <GlobalConditionDataType> -XmlFilePath <String>
 [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] [-XmlNamespace <String[]>] -XPathQuery <String>
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

{{Fill in the Description}}

## EXAMPLES

### Example 1

```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -DataType

{{Fill DataType Description}}

```yaml
Type: GlobalConditionDataType
Parameter Sets: (All)
Aliases:
Accepted values: String, DateTime, Integer, FloatingPoint, Version, Boolean

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

{{Fill Description Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

{{Fill DisableWildcardHandling Description}}

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

{{Fill ForceWildcardHandling Description}}

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

### -IncludeSubfolder

{{Fill IncludeSubfolder Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: IncludeSubfolders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Is64Bit

{{Fill Is64Bit Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

{{Fill Name Description}}

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

### -XmlFilePath

{{Fill XmlFilePath Description}}

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

### -XmlNamespace

{{Fill XmlNamespace Description}}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: XmlNamespaces

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XPathQuery

{{Fill XPathQuery Description}}

```yaml
Type: String
Parameter Sets: NewQueryFromText
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XPathQueryFilePath

{{Fill XPathQueryFilePath Description}}

```yaml
Type: String
Parameter Sets: NewQueryFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### None


## OUTPUTS

### System.Object

## NOTES

