---
---

# New-CMGlobalConditionScript

## SYNOPSIS

{{Fill in the Synopsis}}

## SYNTAX

### NewScriptFromFile (Default)

```
New-CMGlobalConditionScript -DataType <GlobalConditionDataType> -FilePath <String>
 -ScriptLanguage <ScriptingLanguage> [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>]
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

### NewScriptFromText

```
New-CMGlobalConditionScript -DataType <GlobalConditionDataType> -ScriptText <String>
 -ScriptLanguage <ScriptingLanguage> [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>]
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

### -FilePath

{{Fill FilePath Description}}

```yaml
Type: String
Parameter Sets: NewScriptFromFile
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

### -ScriptLanguage

{{Fill ScriptLanguage Description}}

```yaml
Type: ScriptingLanguage
Parameter Sets: (All)
Aliases:
Accepted values: JScript, PowerShell, VBScript

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptText

{{Fill ScriptText Description}}

```yaml
Type: String
Parameter Sets: NewScriptFromText
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Use32BitHost

{{Fill Use32BitHost Description}}

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

### -UseLoggedOnUserCredential

{{Fill UseLoggedOnUserCredential Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UseLoggedOnUserCredentials

Required: False
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

