---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Get-CMObjectSecurityScope
---

# Get-CMObjectSecurityScope

## SYNOPSIS

Get the security scope for an object.

## SYNTAX

### FilterByName (Default)
```
Get-CMObjectSecurityScope -InputObject <IResultObject> [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### FilterById
```
Get-CMObjectSecurityScope [-Id <String>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the security scopes that are associated with a Configuration Manager object.

For more information on security scopes, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get security scopes for an application

This command first gets the application object named **Central app**. It then uses the pipeline operator to pass the object to **Get-CMObjectSecurityScope**, which gets all security scopes associated with the application object.

```powershell
Get-CMApplication -Name "Central app" | Get-CMObjectSecurityScope
```

### Example 2: Get a security scope for a package

This command gets the security scope named **Scope1** that is associated with the package with ID **XYZ00001**.

```powershell
$pkg = Get-CMPackage -Id "XYZ00001"
Get-CMObjectSecurityScope -InputObject $pkg -Name "Scope1"
```

## PARAMETERS

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

### -Id

Specify the ID of a security scope that's associated with a Configuration Manager object. This value is the `CategoryID` property, for example `SMS00UNA` for the **Default** scope.

```yaml
Type: String
Parameter Sets: FilterById
Aliases: CategoryId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a Configuration Manager object that's associated with a security scope. To get this object, use the **Get** cmdlet for the object type. For example, **Get-CMApplication** for app objects.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a security scope that's associated with a Configuration Manager object.

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_SecuredCategory

### IResultObject#SMS_SecuredCategory

## NOTES

For more information on this return object and its properties, see [SMS_SecuredCategory server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_securedcategory-server-wmi-class).

## RELATED LINKS

[Add-CMObjectSecurityScope](Add-CMObjectSecurityScope.md)

[Remove-CMObjectSecurityScope](Remove-CMObjectSecurityScope.md)

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
