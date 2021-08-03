---
description: Creates a Script type global condition in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/08/2019
schema: 2.0.0
title: New-CMGlobalConditionScript
---

# New-CMGlobalConditionScript

## SYNOPSIS

Creates a Script type global condition in Configuration Manager.

## SYNTAX

### NewScriptFromFile (Default)
```
New-CMGlobalConditionScript -DataType <GlobalConditionDataType> -FilePath <String>
 -ScriptLanguage <ScriptingLanguage> [-Use32BitHost <Boolean>] [-UseLoggedOnUserCredential <Boolean>]
 [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### NewScriptFromText
```
New-CMGlobalConditionScript -DataType <GlobalConditionDataType> -ScriptLanguage <ScriptingLanguage>
 -ScriptText <String> [-Use32BitHost <Boolean>] [-UseLoggedOnUserCredential <Boolean>] [-Description <String>]
 -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMGlobalConditionScript** cmdlet creates a Script type global condition in Configuration Manager.

A global condition is a setting or expression in Configuration Manager that you can use to specify how Configuration Manager provides and deploys an application to clients.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
$GlobalScript = New-CMGlobalConditionScript -DataType String -ScriptText $string -ScriptLanguage JScript -Name GC5
```

This command creates a Script type global condition in Configuration Manager.

## PARAMETERS

### -DataType

Specifies a data type.

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

Specifies a description.

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

### -FilePath

Specifies a file path of the script.  You can use Windows PowerShell, VBScript, or JScript scripts.

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

### -ScriptLanguage

Specifies a script language.

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

Specifies a script string.

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

Indicate whether to use 32-bit host.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)

[New-CMGlobalCondition](./New-CMGlobalCondition.md)

[New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)

[New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)

[New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)

[New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)

[New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)

[New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)

[New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)

[New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)

[New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)

[New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXPathQuery.md)
