---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
online version:
schema: 2.0.0
---

# Import-CMAADClientApplication

## SYNOPSIS

Create the Microsoft Entra client app definition in Configuration Manager.

## SYNTAX

### ByServerApp
```
Import-CMAADClientApplication -AppName <String> -ClientId <String> -ServerApp <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Import-CMAADClientApplication -AppName <String> -ClientId <String> -TenantId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to import the client app from Microsoft Entra ID, and define it for the Configuration Manager site. It assumes that an Azure administrator already created the app in Microsoft Entra ID. In Microsoft Entra ID, this app is known as a _native_ app registration.

For more information on how to use this cmdlet to create a cloud management gateway (CMG), see [2010 release notes: Cloud management gateway](/powershell/sccm/2010-release-notes#cloud-management-gateway).

For more information about Microsoft Entra apps in Configuration Manager, see [Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard).

> [!NOTE]
> This cmdlet might work with other Azure services, but it's only tested with the **Cloud management** connection to support the cloud management gateway (CMG).

## EXAMPLES

### Example 1: Import the client app based on the tenant ID

```powershell
Import-CMAADClientApplication -TenantId "05a349fa-298a-4427-8771-9efcdb73431e" -AppName "CmgClientApp" -ClientId "cf114f48-88db-4829-ac45-0c186e86dbf6"
```

### Example 2: Import the client app based on the server app

```powershell
$serverApp = Get-CMAADApplication -TenantName "Contoso" -AppType ServerApplication -AppName "CmgServerApp"

Import-CMAADClientApplication -ServerApp $serverApp -AppName "CmgClientApp" -ClientId "cf114f48-88db-4829-ac45-0c186e86dbf6"
```

## PARAMETERS

### -AppName

Specify the name of the app in Microsoft Entra ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
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

### -ServerApp

Specify an object for the server app. To get the server app, use the [Get-CMAADApplication](Get-CMAADApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByServerApp
Aliases: ServerApplication

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId

Specify the GUID of your Microsoft Entra tenant.

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

[Import-CMAADServerApplication](Import-CMAADServerApplication.md)

[Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard)
