---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: C32CF428-1E90-4EB5-8490-5CA9E9D75835
online version: https://go.microsoft.com/fwlink/?linkid=834171
schema: 2.0.0
---

# Remove-CMReportingServicePoint

## SYNOPSIS
Removes a reporting service point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMReportingServicePoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMReportingServicePoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMReportingServicePoint** cmdlet removes a reporting service point from a Microsoft System Center Configuration Manager site.
The reporting service point is a site system role that is installed on a server that is running Microsoft SQL Server Reporting Services.

After you remove a reporting service point from a System Center Configuration Manager site, you cannot manage reports in System Center Configuration Manager at the site.

## EXAMPLES

### Example 1: Remove a reporting service point
```
PS C:\> Remove-CMReportingServicePoint -SiteCode "CM1" -SiteSystemServerName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM"
```

This command removes the reporting service point from the System Center Configuration Manager site that has the site code CM1 on the site system server named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM.

### Example 2: Remove a reporting service point by using an object variable
```
PS C:\> $Rsp = Get-CMReportingServicePoint -SiteCode "CM1" -SiteSystemServerName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM"
PS C:\> Remove-CMReportingServicePoint -InputObject $Rsp
```

The first command gets the reporting service point from the System Center Configuration Manager site that has the site code CM1 on the site system server named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM.
The command stores the results in the $Rsp variable.

The second command removes the reporting service point in $Rsp.

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

### -Force
Forces the command to run without asking for user confirmation.

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

### -InputObject
Specifies a **CMReportingServicePoint** object.
To obtain a **CMReportingServicePoint** object, use the Get-CMReportingServicePoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ReportingServicePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName

Required: True
Position: 0
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

[Add-CMReportingServicePoint](Add-CMReportingServicePoint.md)

[Get-CMReportingServicePoint](Get-CMReportingServicePoint.md)

[Set-CMReportingServicePoint](Set-CMReportingServicePoint.md)


