---
external help file: AdminUI.PS.Rba.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMAdministrativeUserPermission

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByValue (Default)
```
New-CMAdministrativeUserPermission -InputObject <IResultObject> [-SecurityScopeId <String[]>]
 [-SecurityScopeName <String[]>] [-SecurityScope <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] [-Collection <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
New-CMAdministrativeUserPermission -RoleId <String> [-SecurityScopeId <String[]>]
 [-SecurityScopeName <String[]>] [-SecurityScope <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] [-Collection <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
New-CMAdministrativeUserPermission -RoleName <String> [-SecurityScopeId <String[]>]
 [-SecurityScopeName <String[]>] [-SecurityScope <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] [-Collection <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -Collection
{{ Fill Collection Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Collections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
{{ Fill CollectionId Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
{{ Fill CollectionName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CollectionNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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
{{ Fill ForceWildcardHandling Description }}

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

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleId
{{ Fill RoleId Description }}

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
{{ Fill RoleName Description }}

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScope
{{ Fill SecurityScope Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SecurityScopes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeId
{{ Fill SecurityScopeId Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SecurityScopeIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeName
{{ Fill SecurityScopeName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SecurityScopeNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_APermission

## NOTES

## RELATED LINKS
