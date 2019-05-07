---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: AF06715E-5255-4E82-841F-49800982E9F7
online version: https://go.microsoft.com/fwlink/?linkid=834254
schema: 2.0.0
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

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get settings for components
```
PS XYZ:\> Get-CMComponentStatusSetting -SiteCode "CAS" -ComponentName SMS_REPL*
```

This command gets status setting objects for the site that has the site code CAS for components with names that begin with SMS_REPL.

### Example 2: Get settings for components on specified systems
```
PS XYZ:\> Get-CMComponentStatusSetting -SiteSystemName VM* -ComponentName SMS_REPL*
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

[Get-CMComponentStatusMessage](Get-CMComponentStatusMessage.md)


