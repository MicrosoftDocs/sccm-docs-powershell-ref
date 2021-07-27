---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/29/2021
online version:
schema: 2.0.0
---

# New-CMApplicationGroup

## SYNOPSIS

Create a new application group.

## SYNTAX

```
New-CMApplicationGroup [-Name] <String> -AddApplication <String[]> [-Description <String>]
 [-Publisher <String>] [-SoftwareVersion <String>] [-OptionalReference <String>] [-ReleaseDate <DateTime>]
 [-AddOwner <String[]>] [-AddSupportContact <String[]>] [-AppGroupCatalog <AppDisplayInfo[]>]
 [-DefaultLanguageId <Int32>] [-LocalizedName <String>] [-UserDocumentation <String>] [-LinkText <String>]
 [-PrivacyUrl <String>] [-LocalizedDescription <String>] [-Keyword <String[]>] [-IconLocationFile <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an application group. Use an application group to deploy multiple applications to a collection as a single deployment. The metadata you specify about the app group is seen in Software Center as a single entity. You can order the apps in the group so that the client installs them in a specific order. For more information, see [Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups).

There are some settings of an app group that you can't configure when you create it. To configure other settings, use the [Set-CMApplicationGroup](Set-CMApplicationGroup.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a group with two apps

This example creates a new app group named **Central app** that includes two apps.

```powershell
$apps = @('LOB Framework','CA UI')

New-CMApplicationGroup -Name 'Central app' -AddApplication $apps -Description 'Central app group' -Publisher 'Contoso IT' -SoftwareVersion '1.1.2' -ReleaseDate (Get-Date) -AddOwner 'jqpublic' -AddSupportContact 'jdoe' -LocalizedAppGroupName 'Central app'
```

## PARAMETERS

### -AddApplication

Specify a string array of app names to add to the group. If you already have an app object from another cmdlet like [Get-CMApplication](Get-CMApplication.md), this value is the **LocalizedDisplayName** property. For example: `$appList = @($app1.LocalizedDisplayName,$app2.LocalizedDisplayName)`

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddApplications

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddOwner

Specify one or more administrative users who are responsible for this app group.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddOwners

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddSupportContact

Specify one or more administrative users that end users can contact for help with this application.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddSupportContacts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppGroupCatalog

Use this parameter to specify a Software Center entry for a specific language. This entry can include all of the localized information about the app group:

- Description
- IconLocationFile
- Keyword
- LinkText
- PrivacyUrl
- Title
- UserDocumentation

To get this object, use the [New-CMApplicationDisplayInfo](New-CMApplicationDisplayInfo.md) cmdlet.

```yaml
Type: AppDisplayInfo[]
Parameter Sets: (All)
Aliases: AppCatalogs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLanguageId

Specify the language ID for the default Software Center language.

This ID is the decimal equivalent of the Windows language ID. For example, `1033` is `0x0409` for **English (United States)**, and `2108` is `0x083C` for **Irish (Ireland)**. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional administrator comment for the app group. The maximum length is 2048 characters.

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

### -IconLocationFile

Specify the path to the file that contains the icon for this app group. Icons can have pixel dimensions of up to 512x512. The file can be of the following image and icon file types:

- DLL
- EXE
- JPG
- ICO
- PNG

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

### -Keyword

Specify a list of keywords in the selected language. These keywords help Software Center users search for the app group.

> [!TIP]
> To add multiple keywords, use **CultureInfo.CurrentCulture.TextInfo.ListSeparator** as the delimiter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Keywords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinkText

When you use the **UserDocumentation** parameter, use this parameter to show a string in place of "Additional information" in Software Center. The maximum length is 128 characters.

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

### -LocalizedDescription

Specify a description for this app group in the selected language. The maximum length is 2048 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedAppGroupDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalizedName

Specify the app group name in the selected language. This name appears in Software Center.

A name is required for each language that you add.

The maximum length is 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedAppGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify a name for the app group. The maximum length is 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName, ApplicationGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OptionalReference

Specify an optional string to help you find the app group in the console. The maximum length is 256 characters.

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

### -PrivacyUrl

Specify a website address to the privacy statement for the app group. The format needs to be a valid URL, for example `https://contoso.com/privacy`. The maximum length of the entire string is 128 characters.

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

### -Publisher

Specify optional vendor information for this app group. The maximum length is 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Manufacturer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReleaseDate

Specify a date object for when this app group was released. To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareVersion

Specify an optional version string for the app group. The maximum length is 64 characters.

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

### -UserDocumentation

Specify the location of a file from which Software Center users can get more information about this app group. This location is a website address, or a network path and file name. Make sure that users have access to this location.

The maximum length of the entire string is 256 characters.

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

### None
## OUTPUTS

### IResultObject#SMS_ApplicationGroup
## NOTES

This cmdlet returns the **SMS_ApplicationGroup** WMI class object.

## RELATED LINKS

[Get-CMApplicationGroup](Get-CMApplicationGroup.md)
[Remove-CMApplicationGroup](Remove-CMApplicationGroup.md)
[Set-CMApplicationGroup](Set-CMApplicationGroup.md)

[New-CMApplicationDisplayInfo](New-CMApplicationDisplayInfo.md)

[Get-CMApplicationGroupDeployment](Get-CMApplicationGroupDeployment.md)
[New-CMApplicationGroupDeployment](New-CMApplicationGroupDeployment.md)
[Remove-CMApplicationGroupDeployment](Remove-CMApplicationGroupDeployment.md)
[Set-CMApplicationGroupDeployment](Set-CMApplicationGroupDeployment.md)

[Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups)
