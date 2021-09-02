---
description: Sets an enrollment point in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMEnrollmentPoint
---

# Set-CMEnrollmentPoint

## SYNOPSIS
Sets an enrollment point in Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMEnrollmentPoint -InputObject <IResultObject> [-PassThru] [-UseComputerAccount] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMEnrollmentPoint [-PassThru] [-SiteCode <String>] [-SiteSystemServerName] <String> [-UseComputerAccount]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMEnrollmentPoint** cmdlet sets an enrollment point in Configuration Manager.
An enrollment point is a site system role that uses public key infrastructure (PKI) certificates to complete mobile device enrollment and to provision Intel AMT-based computers.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set an enrollment point
```
PS XYZ:\> Set-CMEnrollmentPoint -SiteSystemServerName "CM-Contoso.Contoso.Com" -SiteCode "CM2" -UserName "Contoso\ElisaDaugherty"
```

The command sets an enrollment point, and specifies an account name to use to connect to the Configuration Manager database.

### Example 2: Set an enrollment point with the computer account
```
PS XYZ:\> Set-CMEnrollmentPoint -SiteSystemServerName "CM-Contoso.Contoso.Com" -SiteCode "CM2" -UseComputerAccount
```

The command sets an enrollment point by specifying the site system server and site code, and uses the computer account to connect to the Configuration Manager database.

### Example 3: Set an enrollment point by using an input object
```
PS XYZ:\> $Ep = Get-CMEnrollmentPoint -SiteSystemServerName "CM-Contoso.Contoso.Com" -SiteCode "CM2"
PS XYZ:\> Set-CMEnrollmentPoint -InputObject $Ep -UserName "Contoso\ElisaDaugherty"
```

The first command uses the **Get-CMEnrollmentPoint** cmdlet to get an enrollment point, and stores the result in the $Ep variable.

The second command sets an enrollment point for a server by using the input object stored in the $Ep variable.

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

### -InputObject
Specifies an input object.
To get an input object, use the [Get-CMEnrollmentPoint](Get-CMEnrollmentPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: EnrollmentPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseComputerAccount
Indicates that you use the computer account to connect to the Configuration Manager database.

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

### -UserName
Specifies a user account that the enrollment point uses to connect to the Configuration Manager database.

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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Add-CMEnrollmentPoint](Add-CMEnrollmentPoint.md)

[Get-CMEnrollmentPoint](Get-CMEnrollmentPoint.md)

[Remove-CMEnrollmentPoint](Remove-CMEnrollmentPoint.md)
