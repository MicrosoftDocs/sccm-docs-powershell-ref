---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
online version:
schema: 2.0.0
---

# Get-CMAzureService

## SYNOPSIS
Get an Azure service.

## SYNTAX

### SearchByName (Default)
```
Get-CMAzureService [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAzureService -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the Azure service. For more information, see [Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard).

> [!NOTE]
> This cmdlet might work with other Azure services, but it's only tested with the **Cloud management** connection to support the cloud management gateway (CMG).

## EXAMPLES

### Example 1: Get the Azure service by name

The following example gets the Azure service from the site by its name.

```powershell
Get-CMAzureService -Name "Contoso"
```

### Example 2: Get the Azure service by ID

The following example gets the Azure services from the site by its ID.

```powershell
Get-CMAzureService -Id 2
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

Specify the site's ID for the Azure service. The **Id** is the integer value stored in the site database for the service. For example, run the following SQL query, and look at the **ID** column: `select * from Azure_CloudService`.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the site's name for the Azure service. The **Name** is the same value as in the **Azure Services** node in the console.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject#SMS_Azure_CloudService
## NOTES

## RELATED LINKS

[Remove-CMAzureService](Remove-CMAzureService.md)

[Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard)
