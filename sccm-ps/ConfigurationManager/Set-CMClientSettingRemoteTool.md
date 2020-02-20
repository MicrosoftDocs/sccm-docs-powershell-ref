---
author: aczechowski
description: Sets a client setting remote tool.
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMClientSettingRemoteTool
titleSuffix: Configuration Manager
---

# Set-CMClientSettingRemoteTool

## SYNOPSIS
Sets a client setting remote tool.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingRemoteTool [-FirewallExceptionProfile <FirewallExceptionProfileType[]>]
 [-AllowClientChange <Boolean>] [-AllowUnattendedComputer <Boolean>] [-PromptUserForPermission <Boolean>]
 [-PromptUserForClipboardPermission <Boolean>] [-GrantPermissionToLocalAdministrator <Boolean>]
 [-AccessLevel <AccessLevelType>] [-PermittedViewer <String[]>] [-ShowNotificationIconOnTaskbar <Boolean>]
 [-ShowSessionConnectionBar <Boolean>] [-AudibleSignal <AudibleSignalType>]
 [-ManageUnsolicitedRemoteAssistance <Boolean>] [-ManageSolicitedRemoteAssistance <Boolean>]
 [-RemoteAssistanceAccessLevel <RemoteAssistanceAccessLevelType>] [-ManageRemoteDesktopSetting <Boolean>]
 [-AllowPermittedViewer <Boolean>] [-RequireAuthentication <Boolean>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingRemoteTool [-FirewallExceptionProfile <FirewallExceptionProfileType[]>]
 [-AllowClientChange <Boolean>] [-AllowUnattendedComputer <Boolean>] [-PromptUserForPermission <Boolean>]
 [-PromptUserForClipboardPermission <Boolean>] [-GrantPermissionToLocalAdministrator <Boolean>]
 [-AccessLevel <AccessLevelType>] [-PermittedViewer <String[]>] [-ShowNotificationIconOnTaskbar <Boolean>]
 [-ShowSessionConnectionBar <Boolean>] [-AudibleSignal <AudibleSignalType>]
 [-ManageUnsolicitedRemoteAssistance <Boolean>] [-ManageSolicitedRemoteAssistance <Boolean>]
 [-RemoteAssistanceAccessLevel <RemoteAssistanceAccessLevelType>] [-ManageRemoteDesktopSetting <Boolean>]
 [-AllowPermittedViewer <Boolean>] [-RequireAuthentication <Boolean>] [-DefaultSetting] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingRemoteTool [-FirewallExceptionProfile <FirewallExceptionProfileType[]>]
 [-AllowClientChange <Boolean>] [-AllowUnattendedComputer <Boolean>] [-PromptUserForPermission <Boolean>]
 [-PromptUserForClipboardPermission <Boolean>] [-GrantPermissionToLocalAdministrator <Boolean>]
 [-AccessLevel <AccessLevelType>] [-PermittedViewer <String[]>] [-ShowNotificationIconOnTaskbar <Boolean>]
 [-ShowSessionConnectionBar <Boolean>] [-AudibleSignal <AudibleSignalType>]
 [-ManageUnsolicitedRemoteAssistance <Boolean>] [-ManageSolicitedRemoteAssistance <Boolean>]
 [-RemoteAssistanceAccessLevel <RemoteAssistanceAccessLevelType>] [-ManageRemoteDesktopSetting <Boolean>]
 [-AllowPermittedViewer <Boolean>] [-RequireAuthentication <Boolean>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -AccessLevel
```yaml
Type: AccessLevelType
Parameter Sets: (All)
Aliases:
Accepted values: NoAccess, ViewOnly, FullControl

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowClientChange
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

### -AllowPermittedViewer
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowPermittedViewersToRemoteDesktop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowUnattendedComputer
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowRemoteControlOfUnattendedComputer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AudibleSignal
```yaml
Type: AudibleSignalType
Parameter Sets: (All)
Aliases:
Accepted values: PlayNoSound, PlaySoundAtBeginAndEnd, PlaySoundRepeatedly

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

### -DefaultSetting
```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases:

Required: True
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

### -FirewallExceptionProfile
```yaml
Type: FirewallExceptionProfileType[]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Public, Private, Domain

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

### -GrantPermissionToLocalAdministrator
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: GrantRemoteControlPermissionToLocalAdministrator

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ManageRemoteDesktopSetting
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

### -ManageSolicitedRemoteAssistance
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

### -ManageUnsolicitedRemoteAssistance
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

### -Name
```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -PermittedViewer
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: PermittedViewers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PromptUserForClipboardPermission
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: PromptUserForClipboardAccessPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PromptUserForPermission
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: PromptUserForRemoteControlPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteAssistanceAccessLevel
```yaml
Type: RemoteAssistanceAccessLevelType
Parameter Sets: (All)
Aliases:
Accepted values: None, RemoteViewing, FullControl

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireAuthentication
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

### -ShowNotificationIconOnTaskbar
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

### -ShowSessionConnectionBar
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

### System.Object

## NOTES

## RELATED LINKS
