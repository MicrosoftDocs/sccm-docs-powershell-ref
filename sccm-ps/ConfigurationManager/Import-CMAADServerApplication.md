---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
online version:
schema: 2.0.0
---

# Import-CMAADServerApplication

## SYNOPSIS

Create the Microsoft Entra server app definition in Configuration Manager.

## SYNTAX

```
Import-CMAADServerApplication [-AppIdUri <Uri>] [-AppName] <String>
 [-AzureEnvironmentOption <AzureEnvironment>] [-ClientId] <String> [-SecretKey] <SecureString>
 [-SecretKeyExpiry] <DateTime> [-TenantId] <String> [-TenantName] <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to import the server app from Microsoft Entra ID, and define it for the Configuration Manager site. It assumes that an Azure administrator already created the app in Microsoft Entra ID. In Microsoft Entra ID, this app is known as a _web_ app registration.

For more information on how to use this cmdlet to create a cloud management gateway (CMG), see [2010 release notes: Cloud management gateway](/powershell/sccm/2010-release-notes#cloud-management-gateway).

For more information about Microsoft Entra apps in Configuration Manager, see [Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard).

> [!NOTE]
> This cmdlet might work with other Azure services, but it's only tested with the **Cloud management** connection to support the cloud management gateway (CMG).

## EXAMPLES

### Example 1

In this example, the first command creates a datetime variable for `11/16/2021`. The second command uses this date variable as the secret key expiry date, when it imports the server app using the details provided.

```powershell
$date = [datetime]::parseexact("11/16/2021", 'MM/dd/yyyy', $null)

Import-CMAADServerApplication -TenantName "Contoso" -TenantId "05a349fa-298a-4427-8771-9efcdb73431e" -AppName "CmgServerApp" -ClientId "7078946d-fc1c-43b7-8dee-dd6e6b00d783" -SecretKey "1uXGR^!0@Cjas6qI*J02ZeS&&zY19^hC*9" -SecretKeyExpiry $date
```

## PARAMETERS

### -AppIdUri

Specify the  **Application ID URI** of the app registration entry in the Microsoft Entra admin center. This value needs to be unique in your Microsoft Entra tenant. It's in the access token used by the Configuration Manager client to request access to the service. The format is similar to https://ConfigMgrService.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppName

Specify the friendly name for the app. This value is the display name in the app registration.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureEnvironmentOption

Specify whether this app registration is in the global Azure cloud (`AzurePublicCloud`), or the Azure Government cloud (`AzureUSGovernmentCloud`).

```yaml
Type: AzureEnvironment
Parameter Sets: (All)
Aliases:
Accepted values: AzurePublicCloud, AzureUSGovernmentCloud

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientId

Specify the **Application (client) ID** value of the app registration in Microsoft Entra ID. The format is a standard GUID.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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

### -SecretKey

Specify the secret key for this app as copied from the Azure portal. You copied the secret key when you registered the app in Microsoft Entra ID.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecretKeyExpiry

Specify the date when the **SecretKey** will expire. You configure this value when you create the secret key for the app in Microsoft Entra ID.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId

Specify the GUID of your Microsoft Entra tenant.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantName

Specify the name of your Microsoft Entra tenant.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### IResultObject#SMS_AAD_Application_Ex
## NOTES

## RELATED LINKS

[Get-CMAADApplication](Get-CMAADApplication.md)

[Import-CMAADClientApplication](Import-CMAADClientApplication.md)

[Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard)
