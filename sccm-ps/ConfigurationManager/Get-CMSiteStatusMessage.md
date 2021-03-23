---
description: Gets site system status messages.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSiteStatusMessage
---

# Get-CMSiteStatusMessage

## SYNOPSIS
Gets site system status messages.

## SYNTAX

```
Get-CMSiteStatusMessage [-Component <String[]>] [-ComputerName <String[]>] [-FilterHashtable <Hashtable>]
 [-MessageId <Int32[]>] [-Module <String[]>] [-PassThru] [-Severity <Severity[]>] [-SiteCode <String[]>]
 [-StartDateTime <DateTime>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSiteStatusMessage** cmdlet gets status messages for one or more Configuration Manager site system components.
A status message is a message that a Configuration Manager component generates that contains information about the success, failure, or operation of site system components.
Configuration Manager stores status messages in a Configuration Manager site database.
You can view status messages in the Status Message Viewer.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get site status messages
```
PS XYZ:\> Get-CMSiteStatusMessage -ViewingPeriod "2012/09/03 02:16:10.000" -ComputerName "cmcen-dist02" -Severity Error -SiteCode "CM2"
```

This command gets the site status messages that Configuration Manager receives on or after September 3, 2012 and that have an error severity.
Configuration Manager gets the status messages from the Configuration Manager site that has the site code CM2 on the computer named cmcen-dist02.tsqa.contoso.com.

## PARAMETERS

### -Component
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ComponentName, Components, ComponentNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Specifies the fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ComputerNames

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

### -FilterHashtable
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

### -MessageId
```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: MessageIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Module
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ModuleName, Modules, ModuleNames

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

### -Severity
Specifies the severity of a status message.
The acceptable values for this parameter are:

- All
- Error
- Information
- Warning

```yaml
Type: Severity[]
Parameter Sets: (All)
Aliases: Severities
Accepted values: All, Error, Information, Warning

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SiteCodes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDateTime
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: ViewingPeriod

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

### IResultObject[]#SMS_StatusMessage

### IResultObject#SMS_StatusMessage

## NOTES

## RELATED LINKS
