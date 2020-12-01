---
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
online version:
schema: 2.0.0
---

# Remove-CMAzureService

## SYNOPSIS

Remove the Azure service.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMAzureService [-Force] -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMAzureService [-Force] -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMAzureService [-Force] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove the Azure service. For more information, see [Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard).

> [!NOTE]
> This cmdlet might work with other Azure services, but it's only tested with the **Cloud management** connection to support the cloud management gateway (CMG).

## EXAMPLES

### Example 1: Remove the Azure service by name

The following example removes the Azure service from the site by its name.

```powershell
Remove-CMAzureService -Name "Contoso"
```

### Example 2: Force remove the Azure service by its ID

The following example removes the Azure services from the site by its ID.

```powershell
Remove-CMAzureService -Id 2 -Force
```

### Example 3: Get the Azure service by name and then remove it

The following example uses the **Get-CMAzureService** to get the service. It then passes that object with the pipeline operator to remove the service.

```powershell
Get-CMAzureService -Name "Contoso" | Remove-CMAzureService
```

## PARAMETERS

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

### -Force

Run the command without asking for confirmation.

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

### -InputObject

Specify an Azure service object to remove. To get this object, use the [Get-CMAzureService](Get-CMAzureService.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: AzureService

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the site's name for the Azure service. The **Name** is the same value as in the **Azure Services** node in the console.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMAzureService](Get-CMAzureService.md)

[Configure Azure services](/mem/configmgr/core/servers/deploy/configure/azure-services-wizard)
