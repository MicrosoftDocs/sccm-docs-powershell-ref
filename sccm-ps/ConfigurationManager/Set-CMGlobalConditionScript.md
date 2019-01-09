---
title: 
titleSuffix: Configuration Manager
description: 
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Set-CMGlobalConditionScript

## SYNOPSIS

{{Fill in the Synopsis}}

## SYNTAX

### SetScriptFromFile (Default)

```powershell
Set-CMGlobalConditionScript [-FilePath <String>] [-ScriptLanguage <ScriptingLanguage>]
 [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### SetScriptFromText

```powershell
Set-CMGlobalConditionScript [-ScriptText <String>] [-ScriptLanguage <ScriptingLanguage>]
 [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

## DESCRIPTION

The **Set-CMGlobalConditionScript** cmdlet modifies settings for a Script type global condition in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1

```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

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

### -Name

Specifies a name.

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

Returns the current working object.
By default, this cmdlet does not generate any output.

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

