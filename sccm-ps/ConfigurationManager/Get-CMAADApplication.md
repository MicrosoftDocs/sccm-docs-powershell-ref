---
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
online version:
ms.date: 11/20/2020
schema: 2.0.0
---

# Get-CMAADApplication

## SYNOPSIS

Get the Azure Active Directory (Azure AD) app object from the site.

## SYNTAX

```
Get-CMAADApplication [-AppName <String>] [-AppType <CloudApplicationType>] [-ClientId <String>]
 [-TenantId <String>] [-TenantName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the Azure AD app object from the site. It's commonly used with the [New-CMCloudManagementAzureService](New-CMCloudManagementAzureService.md) cmdlet.

For more information about Azure AD apps in Configuration Manager, see [Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard).

> [!NOTE]
> While some of the new cmdlets might work with other Azure services, they're only tested with the **Cloud management** connection to support the cloud management gateway (CMG).

## EXAMPLES

### Example 1: Get Azure AD client apps by tenant name

This example returns all client apps in the specified tenant.

```powershell
Get-CMAADApplication -TenantName "Contoso" -AppType ClientApplication
```

### Example 2: Get Azure AD server apps by tenant ID

This example returns all server apps in the specified tenant.

```powershell
Get-CMAADApplication -TenantId "05a349fa-298a-4427-8771-9efcdb73431e" -AppType ServerApplication
```

### Example 3: Get an Azure AD app by its name

```powershell
Get-CMAADApplication -AppName "CmgServerApp"
```

## PARAMETERS

### -AppName

Specify the name of the app in Azure AD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppType

Specify whether to target the server or client app.

In Azure AD, the server app is known as a _web_ app registration, and the client app is known as a _native_ app registration.

```yaml
Type: CloudApplicationType
Parameter Sets: (All)
Aliases: ApplicationType
Accepted values: ServerApplication, ClientApplication

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientId

Specify the **Application (client) ID** value of the app registration in Azure AD. The format is a standard GUID.

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

### -TenantId

Specify the GUID of your Azure AD tenant.

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

### -TenantName

Specify the name of your Azure AD tenant.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_AAD_Application_Ex

## NOTES

## RELATED LINKS

[New-CMCloudManagementAzureService](New-CMCloudManagementAzureService.md)

[Get-CMAzureService](Get-CMAzureService.md)

[Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard)
