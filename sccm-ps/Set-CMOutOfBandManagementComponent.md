---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833966
schema: 2.0.0
ms.assetid: 31071321-3393-445D-8345-B2DF8875EB1D
---

# Set-CMOutOfBandManagementComponent

## SYNOPSIS
Sets the site system server that hosts the out of band management role in System Center Configuration Manager.

## SYNTAX

```
Set-CMOutOfBandManagementComponent [-SiteCode <String>] [-EnrollmentPoint <IResultObject>]
 [-AmtAccountOU <String>] [-UniversalSecurityGroup <String>] [-IssuingCertificationAuthority <String>]
 [-CertificationAuthorityName <String>] [-CertificateTemplate <String>] [-EnableCrlChecking <Boolean>]
 [-MebxAccount <String>] [-MebxPassword <SecureString>] [-AddAmtUserAccount <String[]>]
 [-RemoveAmtUserAccount <String[]>] [-PowerState <PowerStateType>] [-EnableWebInterface <Boolean>]
 [-EnableIdeRedirection <Boolean>] [-AllowPingResponse <Boolean>] [-EnableBypassBiosPassword <Boolean>]
 [-KerberosClockToleranceMins <Int32>] [-AuditLogSettingName <AuditLogSettingType[]>]
 [-AmtProvisioningAccount <Dictionary`2[]>] [-AmtProvisioningSchedule <IResultObject>]
 [-AmtProvisioningRemovalAccount <String>] [-AmtProvisioningRemovalPassword <SecureString>]
 [-EnableWiredNetworkAccess <Boolean>] [-WiredProfileObject <WiredProfile>]
 [-WirelessProfile <WirelessProfile[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMOutOfBandManagementComponent** cmdlet sets the site system computer that hosts the out of band management role in Microsoft System Center Configuration Manager.
The out of band management role manages computers that have the Intel vPro chip set and a version of Intel Active Management Technology (AMT) that System Center Configuration Manager supports.
Out of band management lets you connect to a computer AMT management controller when the computer is turned off, in hibernation, or otherwise unresponsive through the operating system.

## EXAMPLES

### Example 1: Set an out of band management component
```
PS C:\> $Cert = Get-CMTrustedRootCertificate -CertificationAuthorityServerName "CertAuth.Contoso.Com"
PS C:\> $WiredP = New-CMWiredProfileObject -TrustedRootCertificate $Cert -ClientAuthenticationMethod EapTtlsMschapv2 -ClientIssuingCertificationAuthority "ContosoCorpTPM.Contoso.Com" -ClientCertificationAuthorityName "Contoso TPM" -ClientCertificateTemplate "Contoso Certificate Access" - MachineAuth - TPM"
PS C:\> $WirelessP = New-CMWirelessProfileObject -ProfileName "Test -NetworkName Net1" -SecurityType WPA2Enterprise -EncryptionMethod AES -TrustedRootCertificate $Cert -ClientAuthenticationMethod EapTtlsMschapv2 -ClientIssuingCertificationAuthority "ContosoCorpTPM.Contoso.Com" -ClientCertificationAuthorityName "Contoso TPM" -ClientCertificateTemplate "Contoso Certificate Access" - MachineAuth - TPMv2"
PS C:\> Set-CMOutOfBandManagementComponent -SiteCode "CM2" -EnableWiredNetworkAccess $True -WiredProfileObject $WiredP -WirelessProfile $WirelessP
```

The first command uses the [Get-CMTrustedRootCertificate](Get-CMTrustedRootCertificate.md) cmdlet to get a certificate, and stores the certificate in the $Cert variable.

The second command uses the [New-CMWiredProfileObject](New-CMWiredProfileObject/,md) cmdlet to create a profile object, and stores the object in the $WiredP variable.

The third command uses the [New-CMWirelessProfileObject](New-CMWirelessProfileObject.md) cmdlet to create a wireless profile object, and stores the object in the $WirelessP variable.

The fourth command sets an out of band management component by using the $WiredP and $WirelessP variables.

### Example 2: Set an out of band management component with an AMT provisioning account
```
PS C:\> $SS= Read-Host -AsSecureString
PS C:\> $Apa = New-CMAmtProvisioningAccount -UserName "ElisaDaugherty" -Password $SS -Description "New AMT Provisioning Account"
PS C:\> $Schedule = New-CMSchedule -DayOfWeek Saturday -RecurCount 2 -Start "2012/11/22 12:10:00"
PS C:\> Set-CMOutOfBandManagementComponent -SiteCode CM2 -AmtProvisioningAccount $Apa -AmtProvisioningSchedule $Schedule -AmtProvisioningRemovalAccount "TSQA\ElisaDaugherty" -AmtProvisioningRemovalPassword $SS
```

The first command creates a password string for the AMT provisioning account.
The command uses a secure string to obscure the password.

The second command uses the [New-CMAmtProvisioningAccount](New-CMAmtProvisioningAccount.md) cmdlet to create an account, and then stores the result in the $Apa variable.

The third command uses the **New-CMSchedule** cmdlet to create a schedule, and then stores the result in the $Schedule variable.

The fourth command sets an out of band management component, by using the $Apa and $Schedule variables.
The command specifies an account for the *AmtProvisioningAccount* parameter.

### Example 3: Set an out of band management component with an AMT user account
```
PS C:\> $SS = Read-Host -AsSecureString
PS C:\> $Apa = New-CMAmtProvisioningAccount -UserName "ElisaDaugherty " -Password "$SS" -Description "New AMT Provisioning Account"
PS C:\> $Schedule= New-CMSchedule -DayOfWeek Saturday -RecurCount 2 -Start "2012/11/22 12:10:00"
PS C:\> Set-CMOutOfBandManagementComponent -SiteCode "CM2"  -AmtUserAccount "TSQA\ElisaDaugherty " -PowerState HostIsOnS0 -EnableWebInterface $True -EnableIDERedirection $False -AllowPingResponse $True -EnableBypassBiosPassword $False -KerberosClockToleranceMinutes 3 -AuditLogSettingName EndpointAccessControl,CircuitBreakerManager,AgentPresenceManager -AmtProvisioningAccount $Apa -AmtProvisioningSchedule $Schedule -AmtProvisioningRemovalAccount "TSQA\ElisaDaugherty" -AmtProvisioningRemovalPassword $SS
```

The first command creates a password string for the AMT provisioning account.
The command uses a secure string to obscure the password.

The second command uses **New-CMAmtProvisioningAccount** to create an account, and stores the result in the $Apa variable.

The third command uses **New-CMSchedule** to create a schedule, and stores the result in the $Schedule variable.

The fourth command sets an out of band management component, by using the $Apa and $Schedule variables.
The command specifies an account name for the *AmtUserAccount* parameter.

### Example 4: Set an out of band management component with an AMT account OU
```
PS C:\> Set-CMOutOfBandManagementComponent -SiteCode "CM2" -AmtAccountOU "LDAP://OU=Resources,DC=TSQA,DC=Contoso,DC=Com" -UniversalSecurityGroup "Administrators" -IssuingCertificationAuthority "Test.TSQA.Contoso.Com" -CertificationAuthorityName "Contoso Test" -CertificateTemplate "Test - Secure Web Server 2yr" -EnableCrlChecking $False
```

The command sets an out of band management component, and specifies an organizational unit with the *AmtAccountOU* parameter.

## PARAMETERS

### -AddAmtUserAccount
Specifies an array of AMT user accounts to add.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPingResponse
Indicates whether to allow ping responses.

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

### -AmtAccountOU
Specifies an organizational unit (OU) for an AMT account.

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

### -AmtProvisioningAccount


```yaml
Type: Dictionary`2[]
Parameter Sets: (All)
Aliases: AmtProvisioningAccounts
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AmtProvisioningRemovalAccount
Specifies an AMT account.

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

### -AmtProvisioningRemovalPassword
Specifies a secure string that contains a password.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AmtProvisioningSchedule
Specifies an input object.
To obtain an input object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -AuditLogSettingName
Specifies an array of audit log setting names.
The acceptable values for this parameter are:

- AgentPresenceManager
- CircuitBreakerManager
- EndpointAccessControl
- EventManager
- FirmwareUpdateManager
- NetworkAdministration
- NetworkTime
- RedirectionManager
- RemoteControlOperations
- SecurityAdministration
- SecurityAuditLog
- StorageAdministration
- WirelessConfiguration

```yaml
Type: AuditLogSettingType[]
Parameter Sets: (All)
Aliases: AuditLogSettingNames
Accepted values: SecurityAdministration, RemoteControlOperations, RedirectionManager, FirmwareUpdateManager, SecurityAuditLog, NetworkTime, NetworkAdministration, StorageAdministration, EventManager, CircuitBreakerManager, AgentPresenceManager, WirelessConfiguration, EndpointAccessControl
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateTemplate
Specifies a certificate template.

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

### -CertificationAuthorityName
Specifies the name of a certification authority.

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

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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

### -EnableBypassBiosPassword
Indicates whether to bypass the BIOS password.

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

### -EnableCrlChecking
Indicates whether to enable certificate revocation list (CRL) checking.

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

### -EnableIdeRedirection
Indicates whether to enable IDE redirection.
Intel AMT uses IDE redirection to redirect serial and IDE communication from a managed client to a management console.

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

### -EnableWebInterface
Indicates whether to enable the Web interface.

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

### -EnableWiredNetworkAccess
Indicates whether to enable wired network access.

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

### -EnrollmentPoint
Specifies an enrollment point in Configuration Manager.

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

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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

### -IssuingCertificationAuthority
Specifies the issuing certification authority.

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

### -KerberosClockToleranceMins


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: KerberosClockToleranceMinutes
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MebxAccount
Specifies the name of an account for Management Engine BIOS Extensions (MEBx).
The MEBx account provides authenticated access to the AMT firmware on AMT-based computers.

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

### -MebxPassword
Specifies a secure string that contains the password for the MEBx account.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
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

### -PowerState
Specifies an AMT power state that describes system states as on, sleeping, hibernating, or off.
The acceptable values for this parameter are:

- AlwaysOnS0S5
- HostIsOnS0

```yaml
Type: PowerStateType
Parameter Sets: (All)
Aliases: 
Accepted values: HostIsOnS0, AlwaysOnS0S5
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveAmtUserAccount
Specifies an array of AMT user accounts to remove.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code in Configuration Manager.

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

### -UniversalSecurityGroup
Specifies the name of a universal security group.

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

### -WiredProfileObject
Specifies a wired profile object.

```yaml
Type: WiredProfile
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WirelessProfile
Specifies an array of wireless profiles.

```yaml
Type: WirelessProfile[]
Parameter Sets: (All)
Aliases: WirelessProfiles
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMOutOfBandManagementComponent](Get-CMOutOfBandManagementComponent.md)

[New-CMSchedule](New-CMSchedule.md)

[Get-CMTrustedRootCertificate](Get-CMTrustedRootCertificate.md)

[New-CMAmtProvisioningAccount](New-CMAmtProvisioningAccount.md)

[New-CMWiredProfileObject](New-CMWiredProfileObject.md)
