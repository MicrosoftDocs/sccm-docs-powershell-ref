---
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMOneDriveBusinessProfile

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByName (Default)
```
Set-CMOneDriveBusinessProfile [-AddSupportedPlatform <IResultObject[]>] [-ClearSupportedPlatform]
 [-Description <String>] [-KnownFolderMoveOption <MoveKnownFolderOptionType>] -Name <String>
 [-NewName <String>] [-O365TenantId <String>] [-PreventRedirectKnownFolders <Boolean>]
 [-RemoveSupportedPlatform <IResultObject[]>] [-ShowNotification <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMOneDriveBusinessProfile [-AddSupportedPlatform <IResultObject[]>] [-ClearSupportedPlatform]
 [-Description <String>] -Id <Int32> [-KnownFolderMoveOption <MoveKnownFolderOptionType>] [-NewName <String>]
 [-O365TenantId <String>] [-PreventRedirectKnownFolders <Boolean>] [-RemoveSupportedPlatform <IResultObject[]>]
 [-ShowNotification <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
Set-CMOneDriveBusinessProfile [-AddSupportedPlatform <IResultObject[]>] [-ClearSupportedPlatform]
 [-Description <String>] -InputObject <IResultObject> [-KnownFolderMoveOption <MoveKnownFolderOptionType>]
 [-NewName <String>] [-O365TenantId <String>] [-PreventRedirectKnownFolders <Boolean>]
 [-RemoveSupportedPlatform <IResultObject[]>] [-ShowNotification <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddSupportedPlatform
{{ Fill AddSupportedPlatform Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddSupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearSupportedPlatform
{{ Fill ClearSupportedPlatform Description }}

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

### -Description
{{ Fill Description Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill Id Description }}

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CI_ID, CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: OneDriveBusinessPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KnownFolderMoveOption
{{ Fill KnownFolderMoveOption Description }}

```yaml
Type: MoveKnownFolderOptionType
Parameter Sets: (All)
Aliases: OneDriveKnownFolderMoveOption
Accepted values: PromptToMove, SilentlyMove

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: ByName
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
{{ Fill NewName Description }}

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

### -O365TenantId
{{ Fill O365TenantId Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: AADTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreventRedirectKnownFolders
{{ Fill PreventRedirectKnownFolders Description }}

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

### -RemoveSupportedPlatform
{{ Fill RemoveSupportedPlatform Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveSupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowNotification
{{ Fill ShowNotification Description }}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS
