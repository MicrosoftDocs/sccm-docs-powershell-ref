---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833878
schema: 2.0.0
ms.assetid: 25E1BFF0-57F9-41D0-9D13-4E8AF57A1570
---

# Get-CMSiteStatusMessage

## SYNOPSIS
Gets site system status messages.

## SYNTAX

```
Get-CMSiteStatusMessage [-ComputerName <String>] [-Severity <Severity>] [-SiteCode <String>]
 -StartDateTime <DateTime> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSiteStatusMessage** cmdlet gets status messages for one or more Microsoft System Center Configuration Manager site system components.
A status message is a message that a System Center Configuration Manager component generates that contains information about the success, failure, or operation of site system components.
System Center Configuration Manager stores status messages in a System Center Configuration Manager site database.
You can view status messages in the Status Message Viewer.

## EXAMPLES

### Example 1: Get site status messages
```
PS C:\>Get-CMSiteStatusMessage -ViewingPeriod "2012/09/03 02:16:10.000" -ComputerName "cmcen-dist02" -Severity Error -SiteCode "CM2"
```

This command gets the site status messages that System Center Configuration Manager receives on or after September 3, 2012 and that have an error severity.
System Center Configuration Manager gets the status messages from the Configuration Manager site that has the site code CM2 on the computer named cmcen-dist02.tsqa.contoso.com.

## PARAMETERS

### -ComputerName
Specifies the fully qualified domain name (FQDN) of the server that hosts the site system role.

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

### -Severity
Specifies the severity of a status message.
The acceptable values for this parameter are:

- All
- Error
- Information
- Warning

```yaml
Type: Severity
Parameter Sets: (All)
Aliases: 
Accepted values: All, Error, Warning, Information

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

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

### -StartDateTime


```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: ViewingPeriod

Required: True
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


