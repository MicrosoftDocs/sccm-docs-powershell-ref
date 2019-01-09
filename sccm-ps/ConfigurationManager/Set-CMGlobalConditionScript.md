---
title: Set-CMGlobalConditionScript
titleSuffix: Configuration Manager
description: Sets a Script type global condition in Configuration Manager.
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

Sets a Script type global condition in Configuration Manager.

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

Specifies the script file path. You can use Windows PowerShell, VBScript, or JScript scripts.

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

Specifies the script language. You can use Windows PowerShell, VBScript, or JScript scripts.

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

Specifies script text.

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

Indicates whether to use a 32-bit host.

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

If you enable this option, the script will run on client computers by using the credentials of the user who is signed in.

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

## OUTPUTS

### System.Object

## RELATED LINKS

- [New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)
- [Set-CMGlobalCondition](./Set-CMGlobalCondition.md)
- [Set-CMGlobalConditionActiveDirectoryQuery](./Set-CMGlobalConditionActiveDirectoryQuery.md)
- [Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)
- [Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)
- [Set-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)
- [Set-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)
- [Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)
- [Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)
- [Set-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)
- [Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)
- [Set-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXPathQuery.md)