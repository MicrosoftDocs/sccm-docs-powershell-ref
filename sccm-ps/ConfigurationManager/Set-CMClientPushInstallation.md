---
description: Changes settings of a client push installation.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMClientPushInstallation
---

# Set-CMClientPushInstallation

## SYNOPSIS
Changes settings of a client push installation.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMClientPushInstallation -InputObject <IResultObject> [-ChosenAccount <String[]>] [-ClearAccount]
 [-RemoveAccount <String[]>] [-AddAccount <String[]>] [-EnableAutomaticClientPushInstallation <Boolean>]
 [-EnableSystemTypeConfigurationManager <Boolean>] [-EnableSystemTypeServer <Boolean>]
 [-EnableSystemTypeWorkstation <Boolean>] [-InstallClientToDomainController <Boolean>]
 [-InstallationProperty <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchBySiteCodeMandatory
```
Set-CMClientPushInstallation [-SiteCode <String>] [-ChosenAccount <String[]>] [-ClearAccount]
 [-RemoveAccount <String[]>] [-AddAccount <String[]>] [-EnableAutomaticClientPushInstallation <Boolean>]
 [-EnableSystemTypeConfigurationManager <Boolean>] [-EnableSystemTypeServer <Boolean>]
 [-EnableSystemTypeWorkstation <Boolean>] [-InstallClientToDomainController <Boolean>]
 [-InstallationProperty <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMClientPushInstallation -Name <String> [-ChosenAccount <String[]>] [-ClearAccount]
 [-RemoveAccount <String[]>] [-AddAccount <String[]>] [-EnableAutomaticClientPushInstallation <Boolean>]
 [-EnableSystemTypeConfigurationManager <Boolean>] [-EnableSystemTypeServer <Boolean>]
 [-EnableSystemTypeWorkstation <Boolean>] [-InstallClientToDomainController <Boolean>]
 [-InstallationProperty <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByComponentValueMandatory
```
Set-CMClientPushInstallation -InputObject <IResultObject> [-ChosenAccount <String[]>] [-ClearAccount]
 [-RemoveAccount <String[]>] [-AddAccount <String[]>] [-EnableAutomaticClientPushInstallation <Boolean>]
 [-EnableSystemTypeConfigurationManager <Boolean>] [-EnableSystemTypeServer <Boolean>]
 [-EnableSystemTypeWorkstation <Boolean>] [-InstallClientToDomainController <Boolean>]
 [-InstallationProperty <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMClientPushInstallation** cmdlet changes the settings of an object that installs a Configuration Manager client by using client push.
A client push installation installs client software on computers that Configuration Manager discovered.
When you configure client push installation for a site, the client installation automatically runs on the computers that Configuration Manager discovered within the site's configured boundaries when those boundaries are part of a boundary group.
You can also start a client push installation by running the Client Push Installation Wizard for a specific collection or resource within a collection.

For more information about how to install clients, see [How to Install Clients on Windows-Based Computers in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=247203) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Change the settings of a client push installation
```
PS XYZ:\> Set-CMClientPushInstallation -EnableAutomaticClientPushInstallation $True -EnableSystemTypeConfiguationManager $True -ChosenAccount "CENTRAL\00ID$" -InstallationProperty "SMSSITECODE=CM1"
```

This command specifies that Configuration Manager automatically uses client push for discovered computers.
The command specifies that Configuration Manager pushes the client software to site system servers and uses the account named CENTRAL\00ID$ to connect to the computer to install the client software.
The *InstallationProperty* parameter sets the value of the SMSSITECODE property for the Windows Installer package to CM1.
This setting assigns the client to the site that has the site code CM1.

## PARAMETERS

### -AddAccount
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddAccounts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ChosenAccount
Specifies an array of accounts for Configuration Manager to use when it connects to the computer to install the client software.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ChosenAccounts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearAccount
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearAccounts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -EnableAutomaticClientPushInstallation
Indicates whether Configuration Manager automatically uses client push for discovered computers.

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

### -EnableSystemTypeConfigurationManager
Indicates whether Configuration Manager pushes the client software to Configuration Manager site system servers.

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

### -EnableSystemTypeServer
Indicates whether Configuration Manager pushes the client software to servers.

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

### -EnableSystemTypeWorkstation
Indicates whether Configuration Manager pushes the client software to workstations.

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

### -InputObject
Specifies a client push installation object.
To obtain a client push installation object, use the [Get-CMClientPushInstallation](Get-CMClientPushInstallation.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory, SearchByComponentValueMandatory
Aliases: ClientPushComponent

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallationProperty
Specifies any installation properties to use when installing the Configuration Manager client.

For Configuration Manager with no service pack installed: You can specify only installation properties for the Windows Installer package (Client.msi); you cannot specify properties for CCMSetup.exe.

For Configuration Manager SP1: You can specify installation properties for the Windows Installer package (Client.msi) and the following CCMSetup.exe properties:

- forcereboot
- skipprereq
- logon
- BITSPriority
- downloadtimeout
- forceinstall

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

### -InstallClientToDomainController
Indicates whether to use automatic site-wide client push installation to install the Configuration Manager client software on domain controllers.

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

### -Name
Specifies a name for the client push installation.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveAccount
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveAccounts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### 

## NOTES

## RELATED LINKS

[How to Install Clients on Windows-Based Computers in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=247203)

[Get-CMClientPushInstallation](Get-CMClientPushInstallation.md)
