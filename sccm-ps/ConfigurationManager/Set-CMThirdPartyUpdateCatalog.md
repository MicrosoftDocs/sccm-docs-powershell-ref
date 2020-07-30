---
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMThirdPartyUpdateCatalog

## SYNOPSIS

Use this cmdlet to modify a third-party updates catalog.

## SYNTAX

### SearchByName (Default)
```
Set-CMThirdPartyUpdateCatalog [[-Name] <String>] [-Subscribe] [-Unsubscribe] [-SyncNow]
 [-PublisherName <String>] [-NewName <String>] [-Description <String>] [-SupportUrl <Uri>]
 [-SupportContact <String>] [-Schedule <IResultObject>] [-PassThru] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMThirdPartyUpdateCatalog [-Id] <String> [-Subscribe] [-Unsubscribe] [-SyncNow] [-PublisherName <String>]
 [-NewName <String>] [-Description <String>] [-SupportUrl <Uri>] [-SupportContact <String>]
 [-Schedule <IResultObject>] [-PassThru] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMThirdPartyUpdateCatalog [-InputObject] <IResultObject> [-Subscribe] [-Unsubscribe] [-SyncNow]
 [-PublisherName <String>] [-NewName <String>] [-Description <String>] [-SupportUrl <Uri>]
 [-SupportContact <String>] [-Schedule <IResultObject>] [-PassThru] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1910, use this cmdlet to modify a third-party updates catalog.

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

## PARAMETERS

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

Specify the ID of the the third-party updates catalog to change.

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

Specify an object for the third-party updates catalog to change.

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
Accept wildcard characters: False
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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_ISVCatalogs

## NOTES

## RELATED LINKS
