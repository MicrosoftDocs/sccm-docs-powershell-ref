---
description: Configure settings for client push installation.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Set-CMClientPushInstallation
---

# Set-CMClientPushInstallation

## SYNOPSIS

Configure settings for client push installation.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMClientPushInstallation [-AddAccount <String[]>] [-AllownNTLMFallback <Boolean>]
 [-ChosenAccount <String[]>] [-ClearAccount] [-EnableAutomaticClientPushInstallation <Boolean>]
 [-EnableSystemTypeConfigurationManager <Boolean>] [-EnableSystemTypeServer <Boolean>]
 [-EnableSystemTypeWorkstation <Boolean>] -InputObject <IResultObject> [-InstallationProperty <String>]
 [-InstallClientToDomainController <Boolean>] [-RemoveAccount <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByComponentValueMandatory
```
Set-CMClientPushInstallation [-AddAccount <String[]>] [-AllownNTLMFallback <Boolean>]
 [-ChosenAccount <String[]>] [-ClearAccount] [-EnableAutomaticClientPushInstallation <Boolean>]
 [-EnableSystemTypeConfigurationManager <Boolean>] [-EnableSystemTypeServer <Boolean>]
 [-EnableSystemTypeWorkstation <Boolean>] -InputObject <IResultObject> [-InstallationProperty <String>]
 [-InstallClientToDomainController <Boolean>] [-RemoveAccount <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMClientPushInstallation [-AddAccount <String[]>] [-AllownNTLMFallback <Boolean>]
 [-ChosenAccount <String[]>] [-ClearAccount] [-EnableAutomaticClientPushInstallation <Boolean>]
 [-EnableSystemTypeConfigurationManager <Boolean>] [-EnableSystemTypeServer <Boolean>]
 [-EnableSystemTypeWorkstation <Boolean>] [-InstallationProperty <String>]
 [-InstallClientToDomainController <Boolean>] -Name <String> [-RemoveAccount <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySiteCodeMandatory
```
Set-CMClientPushInstallation [-AddAccount <String[]>] [-AllownNTLMFallback <Boolean>]
 [-ChosenAccount <String[]>] [-ClearAccount] [-EnableAutomaticClientPushInstallation <Boolean>]
 [-EnableSystemTypeConfigurationManager <Boolean>] [-EnableSystemTypeServer <Boolean>]
 [-EnableSystemTypeWorkstation <Boolean>] [-InstallationProperty <String>]
 [-InstallClientToDomainController <Boolean>] [-RemoveAccount <String[]>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to change the site configuration for client push installation. The client push installation method installs the Configuration Manager client on computers that the site discovers.

You can also start a client push installation by running the Client Push Installation Wizard for a specific collection or resource within a collection.

For more information, see [How to install clients on Windows-based computers in Configuration Manager](/mem/configmgr/core/clients/deploy/deploy-clients-to-windows-computers#BKMK_ClientPush).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the settings of a client push installation

This command makes the following configurations:

- Automatically use client push for discovered computers.
- Push the client to site system servers
- The site uses the account named **contoso\svc_smspush** to connect to the computer to install the client software.

The **InstallationProperty** parameter sets the value of the **SMSSITECODE** property for the Windows Installer package to **CM1**. This setting assigns the client to the site that has the site code **CM1**.

```powershell
Set-CMClientPushInstallation -SiteCode "CM1" -EnableAutomaticClientPushInstallation $True -EnableSystemTypeConfiguationManager $True -ChosenAccount "contoso\svc_smspush" -InstallationProperty "SMSSITECODE=CM1"
```

## PARAMETERS

### -AddAccount

Specify a string array for one or more accounts that can install the client. The accounts need to be a local **Administrator** on the destination computer. For each account, use the format `domain\username`.

For more information, see [Client push installation account](/mem/configmgr/core/plan-design/hierarchy/accounts#client-push-installation-account).

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

### -AllownNTLMFallback

When this parameter is **$true**, if the site can't authenticate the client by using Kerberos, it retries the connection by using NTLM. The recommended configuration for improved security is to set this parameter to **$false**, which requires Kerberos without NTLM fallback.

> [!NOTE]
> When it uses client push to install the Configuration Manager client, the site server creates a remote connection to the client. The site can require Kerberos mutual authentication by not allowing fallback to NTLM before establishing the connection. This behavior helps to secure the communication between the server and the client.
>
> Depending on your security policies, your environment might already prefer or require Kerberos over the older NTLM authentication. For more information on the security considerations of these authentication protocols, read about the [Windows security policy setting to restrict NTLM](/windows/security/threat-protection/security-policy-settings/network-security-restrict-ntlm-outgoing-ntlm-traffic-to-remote-servers#security-considerations).
>
> To use this feature, clients must be in a trusted Active Directory forest. Kerberos in Windows relies on Active Directory for mutual authentication.

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

### -ChosenAccount

Specify a string array for one or more accounts already added to Configuration Manager.

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

Add this parameter to remove all accounts that are currently specified for client push at the site. To remove a single account, use the **RemoveAccount** parameter.

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

### -EnableAutomaticClientPushInstallation

Set this parameter to **$true** to install the Configuration Manager client on newly discovered computer resources. It also enables installation on existing computer resources that don't have the client installed.

If you set this parameter to **$false**, you can still use the [Install client](/mem/configmgr/core/clients/manage/client-notification#install-client) action on a collection or device.

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

Set this parameter to **$true** to install the Configuration Manager client on site system servers.

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

Set this parameter to **$true** to install the Configuration Manager client on servers.

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

Set this parameter to **$true** to install the Configuration Manager client on workstations.

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

Specify a client push installation object. To get this object, use the [Get-CMClientPushInstallation](Get-CMClientPushInstallation.md) cmdlet.

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

Specify any installation properties to use when installing the Configuration Manager client.

For example:

`/mp:mp01.contoso.com CCMDEBUGLOGGING="1" CCMLOGGINGENABLED="TRUE" CCMLOGLEVEL="0" CCMLOGMAXHISTORY="5" CCMLOGMAXSIZE="10000000" SMSCACHESIZE="15000" SMSSITECODE="XYZ" SMSMP=mp01.contoso.com`

For more information, see [About client installation parameters and properties in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-installation-properties).

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

Set this parameter to specify whether to install the Configuration Manager client on domain controllers:

- **$true**: Always install the client on domain controllers.
- **$false**: Never install the client on domain controllers, unless specified in the Client Push Installation Wizard.

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

Specify a string array of client push installation accounts to remove. To remove all accounts, use the **ClearAccount** parameter.

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

Specify the three character site code. For example, `XYZ`.

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

## NOTES

## RELATED LINKS

[Get-CMClientPushInstallation](Get-CMClientPushInstallation.md)

[How to install clients on Windows-based computers in Configuration Manager](/mem/configmgr/core/clients/deploy/deploy-clients-to-windows-computers#BKMK_ClientPush)
