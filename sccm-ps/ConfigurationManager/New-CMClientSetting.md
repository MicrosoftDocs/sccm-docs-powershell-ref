---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
ms.assetid: 728F467C-C28D-428E-9C2F-8812F6A4F80F
online version: https://go.microsoft.com/fwlink/?linkid=833581
schema: 2.0.0
---

# New-CMClientSetting

## SYNOPSIS
Creates customized client settings.

## SYNTAX

```
New-CMClientSetting -Name <String> [-Description <String>] -Type <Types> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMClientSetting** cmdlet creates a collection of customized settings for Microsoft System Center Configuration Manager client computers.
After you create the customized settings and deploy them to client computer collections, the customized settings override the default client settings for that collection.

For more information about client settings, see [About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226) on TechNet.

## EXAMPLES

### Example 1: Create a customized collection of client settings
```
PS C:\> New-CMClientSetting -Name "Win08ClientSettings" -Description "Windows 8 Client Computers Settings" -Type 1
AgentConfigurations: {}
AssignmentCount:     0
CreatedBy:           Contoso\DChew
DateCreated:         8/04/2012 4:40:03 PM
DateModified:        8/04/2012 4:40:03 PM
Description:         Windows 8 Client Computers Settings
Enabled:             False
FeatureType:         1
Flags:               0
LastModifiedBy:      Contoso\DChew
Name:                Win08ClientSettings
Priority:            0
SecuredScopeNames:   {Default}
Settings ID:         16777220
Type:                1
UniqueID:            {0CCA6700-AE5E-4949-8FBC-AA6719775CC3}
```

This command creates customized device settings for the group of client computers that run Windows® 8.
After the new collection of settings is created, the command displays an unpopulated list of setting properties.
To refresh and view a populated list of properties, use **Get-CMClientSetting**.
The output for this example shows a populated list.

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

### -Description
Specifies a description of the content of the new settings.

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
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -Name
Specifies a name for customized client settings.

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

### -Type
Specifies the type of customized settings.
Valid values are: 1 (device) or 2 (user).

```yaml
Type: Types
Parameter Sets: (All)
Aliases: 
Accepted values: Default, Device, User

Required: True
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

[About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226)

[Get-CMClientSetting](Get-CMClientSetting.md)

[Remove-CMClientSetting](Remove-CMClientSetting.md)

[Set-CMClientSetting](Set-CMClientSetting.md)
