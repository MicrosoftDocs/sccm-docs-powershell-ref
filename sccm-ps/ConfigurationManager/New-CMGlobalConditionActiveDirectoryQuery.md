---
title: New-CMGlobalConditionActiveDirectoryQuery
titleSuffix: Configuration Manager
description: 
ms.date: 01/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# New-CMGlobalConditionActiveDirectoryQuery

## SYNOPSIS

{{Fill in the Synopsis}}

## SYNTAX

```powershell
New-CMGlobalConditionActiveDirectoryQuery -DataType <GlobalConditionDataType> [-LdapPrefix <String>]
 -DistinguishedName <String> -LdapFilter <String> -SearchScope <SearchScope> -Property <String> -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
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
Accepted values: String, DateTime, Integer, FloatingPoint, Version, Boolean, StringArray, IntegerArray

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

### -DistinguishedName

{{Fill DistinguishedName Description}}

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

### -LdapFilter

{{Fill LdapFilter Description}}

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

### -LdapPrefix

{{Fill LdapPrefix Description}}

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

### -Property

{{Fill Property Description}}

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

### -SearchScope

{{Fill SearchScope Description}}

```yaml
Type: SearchScope
Parameter Sets: (All)
Aliases:
Accepted values: Base, OneLevel, Subtree

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

