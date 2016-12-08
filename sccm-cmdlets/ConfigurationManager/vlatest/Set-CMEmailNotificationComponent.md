---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833834
schema: 2.0.0
ms.assetid: 492BE510-2A4E-485F-A4BE-ED5BD5303085
---

# Set-CMEmailNotificationComponent

## SYNOPSIS
Changes configuration settings of an email notification component.

## SYNTAX

### Enable (Default)
```
Set-CMEmailNotificationComponent [-EnableEmailNotification] -SmtpServerFqdn <String> [-Port <Int32>]
 -TypeOfAuthentication <AuthenticationMethod> [-UserName <String>] -SendFrom <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Disable
```
Set-CMEmailNotificationComponent [-DisableEmailNotification] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMEmailNotificationComponent** cmdlet changes configuration settings of an email notification component in Microsoft System Center Configuration Manager.
You can configure the email notification component for each System Center Configuration Manager site to configure email subscriptions to alerts.

## EXAMPLES

### Example 1: Enable email notification
```
PS C:\>Set-CMEmailNotificationComponent -SiteSystemServerName "cmcen-dist02.tsqa.corp.contoso.com" -SiteCode "CM2" -EnableEmailNotification $True -MstpServerFqdn "mail.corp.contosco.com" -Port 25 -TypeOfAuthentication DefaultServiceAccount -SendFrom "evan.narvaez@contoso.com"
```

This command enables email notification for System Center Configuration Manager.
The command specifies that System Center Configuration Manager uses the System Center Configuration Manager site that has the site code CM2 on the server cmcen-dist02.tsqa.corp.contoso.com to host the site system role for email notification.
The command specifies that System Center Configuration Manager uses the server named mail.corp.contosco.com for the email server and specifies the outgoing SMTP port for sending email alerts.
The command specifies that System Center Configuration Manager uses the default service account for authenticating the site server to the SMTP Server, and specifies that System Center Configuration Manager sends email alerts from the email address evan.narvaez@contoso.com.

### Example 2: Disable email notification
```
PS C:\>Set-CMEmailNotificationComponent -SiteSystemServerName "cmcen-dist02.tsqa.corp.contoso.com" -EnableEmailNotification $False
```

This command disables email notification for System Center Configuration Manager on the site server named cmcen-dist02.tsqa.corp.contoso.com.

### Example 3: Set the outgoing SMTP port for email notification
```
PS C:\>Set-CMEmailNotificationComponent -SiteSystemServerName "cmcen-dist02.tsqa.corp.contoso.com" -Port 27
```

This command sets the outgoing SMTP port that System Center Configuration Manager uses for sending email alerts on the site server named cmcen-dist02.tsqa.corp.contoso.com to port 27.

## PARAMETERS

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

### -DisableEmailNotification
Indicates that email notification is disabled.

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 
Required: True
Position: 0
Default value: None
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

### -EnableEmailNotification
Indicates that Configuration Manager uses an SMTP server to send email alerts.

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 
Required: True
Position: 0
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

### -Port
Specifies the outgoing SMTP port for sending email alerts.

```yaml
Type: Int32
Parameter Sets: Enable
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendFrom
Specifies the email address from which Configuration Manager sends email alerts.

```yaml
Type: String
Parameter Sets: Enable
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SmtpServerFqdn
Specifies the fully qualified domain name (FQDN) of the SMTP server.

```yaml
Type: String
Parameter Sets: Enable
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeOfAuthentication
Specifies the method by which Configuration Manager authenticates the site server to the SMTP Server.
The acceptable values for this parameter are:

- Anonymous
- DefaultServiceAccount
- Other

```yaml
Type: AuthenticationMethod
Parameter Sets: Enable
Aliases: 
Accepted values: Anonymous, DefaultServiceAccount, Other
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the user name to authenticate with the SMTP server from which Configuration Manager sends email alerts.
This parameter also specifies the SMTP Server Connection account.

```yaml
Type: String
Parameter Sets: Enable
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMEmailNotificationComponent](./Get-CMEmailNotificationComponent.md)
