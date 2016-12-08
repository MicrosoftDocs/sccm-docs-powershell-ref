---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834254
schema: 2.0.0
ms.assetid: AF06715E-5255-4E82-841F-49800982E9F7
---

# Get-CMComponentStatusSetting

## SYNOPSIS
Gets Configuration Manager component status settings.

## SYNTAX

```
Get-CMComponentStatusSetting [-SiteSystemServerName <String>] [-ComponentName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMComponentStatusSetting** cmdlet gets component status setting objects.
These objects contain thresholds for Microsoft System Center Configuration Manager component status messages.

## EXAMPLES

### Example 1: Get settings for components
```
PS C:\> Get-CMComponentStatusSetting -SiteCode "CAS" -ComponentName SMS_REPL*
```

This command gets status setting objects for the site that has the site code CAS for components with names that begin with SMS_REPL.

### Example 2: Get settings for components on specified systems
```
PS C:\> Get-CMComponentStatusSetting -SiteSystemName VM* -ComponentName SMS_REPL*
```

This command gets status setting objects for systems with names that begin with VM for components with names that begin with SMS_REPL.

## PARAMETERS

### -ComponentName
Specifies a name of a thread or process.
A thread or process sends a component status message.
You can use wildcards.

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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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

### -SiteSystemServerName


```yaml
Type: String
Parameter Sets: (All)
Aliases: Name
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMComponentStatusMessage](./Get-CMComponentStatusMessage.md)


