---
description: Gets a package deployment from Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/30/2018
schema: 2.0.0
title: Get-CMPackageDeployment
---

# Get-CMPackageDeployment

## SYNOPSIS

Gets a package deployment from Configuration Manager.

## SYNTAX

### SearchByName (Default)
```
Get-CMPackageDeployment [-Name <String>] [-ProgramName <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMPackageDeployment [-DeploymentId <String>] [-ProgramName <String>] [-Summary]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMPackageDeployment [-InputObject <IResultObject>] [-ProgramName <String>] [-Summary]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMPackageDeployment [-PackageId <String>] [-ProgramName <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMPackageDeployment** cmdlet starts deployment of a specified software package to computers that belong to a Configuration Manager collection.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> Get-CMPackageDeployment -PackageId $thisPackage.packageid
```

This command gets a package deployment by the package id.

## PARAMETERS

### -Collection

Specifies the user collection.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

Specifies the ID of a device or user collection.

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

### -CollectionName

Specifies the name of a user collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -DeploymentId

Specifies the ID of a deployment.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AdvertisementID, PackageDeploymentID

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

### -InputObject

Specifies a package.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Package

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies the name of a package.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: PackageName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -PackageId

Specifies the ID of a package.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: SmsObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgramName

Specifies the name of a program.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Summary

Add this parameter to return the [SMS_DeploymentSummary WMI class](/mem/configmgr/develop/reference/apps/sms_deploymentsummary-server-wmi-class) object.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_DeploymentSummary
### IResultObject#SMS_DeploymentSummary
### IResultObject[]#SMS_Advertisement
### IResultObject#SMS_Advertisement
## NOTES

For more information on these return objects and their properties, see the following articles:

- [SMS_DeploymentSummary server WMI class](/mem/configmgr/develop/reference/apps/sms_deploymentsummary-server-wmi-class)
- [SMS_Advertisement server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_advertisement-server-wmi-class)

## RELATED LINKS

[New-CMPackageDeployment](New-CMPackageDeployment.md)
[Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md)
[Set-CMPackageDeployment](Set-CMPackageDeployment.md)
[Remove-CMPackageDeployment](Remove-CMPackageDeployment.md)
[Get-CMPackage](Get-CMPackage.md)
