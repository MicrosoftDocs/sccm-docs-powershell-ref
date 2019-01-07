---
---

# New-CMGlobalConditionSqlQuery

## SYNOPSIS

{{Fill in the Synopsis}}

## SYNTAX

### NewQueryFromFile (Default)

```
New-CMGlobalConditionSqlQuery -DataType <GlobalConditionDataType> -FilePath <String> [-AllInstances]
 [-InstanceName <String>] -Database <String> -Column <String> -Name <String> [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling]
```

### NewQueryFromText

```
New-CMGlobalConditionSqlQuery -DataType <GlobalConditionDataType> -QueryText <String> [-AllInstances]
 [-InstanceName <String>] -Database <String> -Column <String> -Name <String> [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling]
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

### -AllInstances

{{Fill AllInstances Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: UseAllInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Column

{{Fill Column Description}}

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

### -Database

{{Fill Database Description}}

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

### -FilePath

{{Fill FilePath Description}}

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

### -InstanceName

{{Fill InstanceName Description}}

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

### -QueryText

{{Fill QueryText Description}}

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

## INPUTS

### None


## OUTPUTS

### System.Object

## NOTES

