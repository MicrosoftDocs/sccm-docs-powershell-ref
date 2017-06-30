---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: CB5EE603-74FA-4FF6-8063-06F257643B15
online version: https://go.microsoft.com/fwlink/?linkid=833948
schema: 2.0.0
---

# Get-CMStatusSummarizer

## SYNOPSIS
Gets a status summarizer object for Configuration Manager.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Get-CMStatusSummarizer -StatusSummarizerType <StatusSummarizerType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameOrSiteCode
```
Get-CMStatusSummarizer [-SiteCode <String>] [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMStatusSummarizer** cmdlet gets a status summarizer object.
The Microsoft System Center Configuration Manager status summarizers apply to the areas of application deployment, application statistics, component status, and site system status.

## EXAMPLES

### Example 1: Get a status summarizer
```
PS C:\> Get-CMStatusSummarizer -SiteCode "CM1" -StatusSummarizerType ComponentStatusSummarizer
```

This command gets the status summarizer for the component status.

## PARAMETERS

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
```yaml
Type: String
Parameter Sets: SearchByNameOrSiteCode
Aliases: SiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for the Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByNameOrSiteCode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatusSummarizerType
Specifies a status summarization type.

```yaml
Type: StatusSummarizerType
Parameter Sets: SearchBySiteCodeMandatory
Aliases: 
Accepted values: ApplicationDeploymentSummarizer, ApplicationStatisticsSummarizer, ComponentStatusSummarizer, SiteSystemStatusSummarizer

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

[Set-CMStatusSummarizer](./Set-CMStatusSummarizer.md)


