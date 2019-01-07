---
---

# Set-CMGlobalConditionScript

## SYNOPSIS

{{Fill in the Synopsis}}

## SYNTAX

### SetScriptFromFile (Default)

```
Set-CMGlobalConditionScript [-FilePath <String>] [-ScriptLanguage <ScriptingLanguage>]
 [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### SetScriptFromText

```
Set-CMGlobalConditionScript [-ScriptText <String>] [-ScriptLanguage <ScriptingLanguage>]
 [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
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
Parameter Sets: SetScriptFromFile
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

### -PassThru

{{Fill PassThru Description}}

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

### -ScriptLanguage

{{Fill ScriptLanguage Description}}

```yaml
Type: ScriptingLanguage
Parameter Sets: (All)
Aliases:
Accepted values: JScript, PowerShell, VBScript

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptText

{{Fill ScriptText Description}}

```yaml
Type: String
Parameter Sets: SetScriptFromText
Aliases:

Required: False
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

## INPUTS

### None


## OUTPUTS

### System.Object

## NOTES

