---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/15/2021
schema: 2.0.0
title: Add-CMReportingServicePoint
---

# Add-CMReportingServicePoint

## SYNOPSIS

Add a reporting service point.

## SYNTAX

### ReportingServicePointByValue (Default)
```
Add-CMReportingServicePoint [-DatabaseName <String>] [-DatabaseServerName <String>] [-Force]
 -InputObject <IResultObject> [-ReportServerInstance <String>] -UserName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ReportingServicePoint
```
Add-CMReportingServicePoint [-DatabaseName <String>] [-DatabaseServerName <String>] [-FolderName <String>]
 [-Force] [-ReportServerInstance <String>] [-SiteCode <String>] [-SiteSystemServerName] <String>
 -UserName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
Use this cmdlet to add a reporting service point to the site. A reporting service point is a site system role that's installed on a server that run Microsoft SQL Server Reporting Services.

For more information, see [Introduction to reporting in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-reporting).

> [!IMPORTANT]
> This cmdlet doesn't support [PowerShell 7](/powershell/sccm/overview#support-for-powershell-version-7).<!-- 12500019 --> It requires the .NET Framework instead of .NET Core that's used with PowerShell version 7.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a reporting service point

This command adds a reporting service point on the computer named CMReportingServicePoint.TSQA.Contoso.com for the Configuration Manager site that has the site code CM1.

```powershell
Add-CMReportingServicePoint -SiteCode "CM1" -SiteSystemServerName "CMReportingServicePoint.TSQA.Contoso.com"
```

## PARAMETERS

### -DatabaseName

Specify the name of the Configuration Manager database that you want to use as the data source for reports from Microsoft SQL Server Reporting Services.

To specify a database instance, use the format `ServerName\InstanceName`.

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

### -DatabaseServerName

Specify the name of the Configuration Manager database server that you want to use as the data source for reports from Microsoft SQL Server Reporting Services.

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

### -FolderName

Specify the name of the report folder on the report server.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Run the command without asking for confirmation.

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

### -InputObject

Specify a site system server object on which to add the reporting service point role. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ReportingServicePointByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReportServerInstance

Specify the name of an instance of Microsoft SQL Server Reporting Services.

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

### -SiteCode

Specify the three-character code for the site that manages the system role for the reporting service point.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName

Specify the name of the site system server to host the reporting service point role.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName

Specify the user name for the Reporting services point account. This account provides authenticated access from the site to Microsoft SQL Server Reporting Services. For more information, see [Accounts used in Configuration Manager](/mem/configmgr/core/plan-design/hierarchy/accounts#reporting-services-point-account).

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_SCI_SysResUse

## NOTES

For more information on this return object and its properties, see [SMS_SCI_SysResUse server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_sysresuse-server-wmi-class).

## RELATED LINKS

[Get-CMReportingServicePoint](Get-CMReportingServicePoint.md)

[Remove-CMReportingServicePoint](Remove-CMReportingServicePoint.md)

[Set-CMReportingServicePoint](Set-CMReportingServicePoint.md)
