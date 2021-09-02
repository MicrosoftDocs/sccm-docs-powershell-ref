---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
online version:
schema: 2.0.0
---

# Set-CMThirdPartyUpdateCatalog

## SYNOPSIS

Modify a third-party updates catalog.

## SYNTAX

### SearchByName (Default)
```
Set-CMThirdPartyUpdateCatalog [-Description <String>] [-Force] [[-Name] <String>] [-NewName <String>]
 [-PassThru] [-PublisherName <String>] [-Schedule <IResultObject>] [-Subscribe] [-SupportContact <String>]
 [-SupportUrl <Uri>] [-SyncNow] [-Unsubscribe] [-CategoryNamePublishOption <Hashtable>]
 [-CategoryIdPublishOption <Hashtable>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMThirdPartyUpdateCatalog [-Description <String>] [-Force] [-Id] <String> [-NewName <String>] [-PassThru]
 [-PublisherName <String>] [-Schedule <IResultObject>] [-Subscribe] [-SupportContact <String>]
 [-SupportUrl <Uri>] [-SyncNow] [-Unsubscribe] [-CategoryNamePublishOption <Hashtable>]
 [-CategoryIdPublishOption <Hashtable>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMThirdPartyUpdateCatalog [-Description <String>] [-Force] [-InputObject] <IResultObject>
 [-NewName <String>] [-PassThru] [-PublisherName <String>] [-Schedule <IResultObject>] [-Subscribe]
 [-SupportContact <String>] [-SupportUrl <Uri>] [-SyncNow] [-Unsubscribe]
 [-CategoryNamePublishOption <Hashtable>] [-CategoryIdPublishOption <Hashtable>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to modify a third-party updates catalog. For more information, see [Enable third-party updates](/mem/configmgr/sum/deploy-use/third-party-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a third-party update catalog

This example gets a third-party update catalog by name, and then changes the name.

```powershell
Set-CMThirdPartyUpdateCatalog -Name "Contoso updates" -NewName "Contoso update catalog"
```

### Example 2: Change the description

This example gets a third-party update catalog by object, and then changes the description.

```powershell
Set-CMThirdPartyUpdateCatalog -ThirdPartyUpdateCatalog $catalog -Description "All of the current Contoso hardware updates"
```

### Example 3: Change support information

This example gets a third-party update catalog piped on the command line, and then changes the support contact and URL.

```powershell
$catalog | Set-CMThirdPartyUpdateCatalog -SupportContact "Contoso hardware support" -SupportUrl "https://hardware.contoso.com"
```

### Example 4: Set the category publishing options for a v3 catalog

This example shows the syntax to create the hashtables to set the categories when you subscribe to a v3 catalog.

```powershell
$id = "5768207d-6c40-465b-ad65-50501661368f"
$option = [Microsoft.ConfigurationManagement.Cmdlets.Sum.Commands.PublishOptionType]::MetadataOnly
$idOptionPair = @{$id = $option}
Set-CMThirdPartyUpdateCatalog -CatalogName 'pmp' -CategoryIdPublishOption $idOptionPair -Subscribe -Force

$name = "2BrightSparks"
$name1 = "8x8, Inc."
$option = [Microsoft.ConfigurationManagement.Cmdlets.Sum.Commands.PublishOptionType]::MetadataOnly
$nameOptionPair = @{$name = $option; $name1 = $option}
Set-CMThirdPartyUpdateCatalog -CatalogName 'pmp' -CategoryNamePublishOption $nameOptionPair -Subscribe -Force
```

## PARAMETERS

### -CategoryIdPublishOption

Set the category ID publish option when you subscribe to a v3 catalog.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CategoryNamePublishOption

Set the category name publish option when you subscribe to a v3 catalog.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify the description for the third-party updates catalog.

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

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

Specify the ID of the third-party updates catalog to change.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CatalogId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for the third-party updates catalog to change. To get this object, use the [Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ThirdPartyUpdateCatalog

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the third-party updates catalog to change.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CatalogName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -NewName

Rename the selected third-party updates catalog.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewCatalogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -PublisherName

Change the publisher name for the specified third-party updates catalog.

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

### -Schedule

Specify a schedule object to apply to the specified third-party updates catalog. Custom schedules override the default synchronization schedule, and are only available for subscribed catalogs.

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

### -Subscribe

Configure the site to subscribe to the third-party updates catalog. This parameter is the same as the console action to **Subscribe to Catalog**.

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

### -SupportContact

Change the support contact for the specified third-party updates catalog.

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

### -SupportUrl

Change the support URL for the specified third-party updates catalog.

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

### -SyncNow

Trigger the site to synchronize the specified third-party updates catalog. This parameter is the same as the console action to **Sync now**.

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

### -Unsubscribe

Configure the site to unsubscribe from the third-party updates catalog. This parameter is the same as the console action to **Unsubscribe from Catalog**.

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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### IResultObject#SMS_ISVCatalogs
## NOTES

This cmdlet returns an object of the **SMS_ISVCatalogs** WMI class.

## RELATED LINKS

[Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md)
[New-CMThirdPartyUpdateCatalog](New-CMThirdPartyUpdateCatalog.md)
[Remove-CMThirdPartyUpdateCatalog](Remove-CMThirdPartyUpdateCatalog.md)

[Publish-CMThirdPartySoftwareUpdateContent](Publish-CMThirdPartySoftwareUpdateContent.md)

[Get-CMThirdPartyUpdateCategory](Get-CMThirdPartyUpdateCategory.md)
[Set-CMThirdPartyUpdateCategory](Set-CMThirdPartyUpdateCategory.md)

[Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates)
