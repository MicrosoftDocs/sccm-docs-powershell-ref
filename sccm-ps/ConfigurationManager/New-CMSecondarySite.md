---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
schema: 2.0.0
title: New-CMSecondarySite
---

# New-CMSecondarySite

## SYNOPSIS

Create a secondary site.

## SYNTAX

### NewDistributionPointByHTTPAndCreateCertificate (Default)
```
New-CMSecondarySite [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>]
 [-BoundaryGroup <IResultObject[]>] -CertificateExpirationTimeUtc <DateTime>
 [-ContentMonitoringPriority <Priority>] [-CreateSelfSignedCertificate] [-EnableAnonymous <Boolean>]
 [-EnableBranchCache] [-Http] [-InstallationFolder <String>] -InstallationSourceFile <IResultObject[]>
 [-InstallInternetServer <Boolean>] [-MinFreeSpaceMB <Int32>] [-PrimaryContentLibraryLocation <DriveType>]
 [-PrimaryPackageShareLocation <DriveType>] [-PrimarySiteCode <String>]
 [-SecondaryContentLibraryLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 -SecondarySiteCode <String> -ServerName <String> -SiteName <String> -SqlServerSetting <IResultObject[]>
 [-ValidateContentSchedule <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### NewDistributionPointByHTTPSAndCreateCertificate
```
New-CMSecondarySite [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>]
 [-BoundaryGroup <IResultObject[]>] -CertificateExpirationTimeUtc <DateTime>
 [-ClientConnectionType <ClientConnectionTypes>] [-ContentMonitoringPriority <Priority>]
 [-CreateSelfSignedCertificate] [-EnableBranchCache] [-Https] [-InstallationFolder <String>]
 -InstallationSourceFile <IResultObject[]> [-InstallInternetServer <Boolean>] [-MinFreeSpaceMB <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-PrimarySiteCode <String>] [-SecondaryContentLibraryLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] -SecondarySiteCode <String> -ServerName <String>
 -SiteName <String> -SqlServerSetting <IResultObject[]> [-ValidateContentSchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewDistributionPointByHTTPSAndImportCertificate
```
New-CMSecondarySite [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>]
 [-BoundaryGroup <IResultObject[]>] -CertificatePassword <SecureString> -CertificatePath <String>
 [-ClientConnectionType <ClientConnectionTypes>] [-ContentMonitoringPriority <Priority>] [-EnableBranchCache]
 [-ForceWhenDuplicateCertificate <Boolean>] [-Https] [-ImportCertificate] [-InstallationFolder <String>]
 -InstallationSourceFile <IResultObject[]> [-InstallInternetServer <Boolean>] [-MinFreeSpaceMB <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-PrimarySiteCode <String>] [-SecondaryContentLibraryLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] -SecondarySiteCode <String> -ServerName <String>
 -SiteName <String> -SqlServerSetting <IResultObject[]> [-ValidateContentSchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewDistributionPointByHTTPAndImportCertificate
```
New-CMSecondarySite [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>]
 [-BoundaryGroup <IResultObject[]>] -CertificatePassword <SecureString> -CertificatePath <String>
 [-ContentMonitoringPriority <Priority>] [-EnableAnonymous <Boolean>] [-EnableBranchCache]
 [-ForceWhenDuplicateCertificate <Boolean>] [-Http] [-ImportCertificate] [-InstallationFolder <String>]
 -InstallationSourceFile <IResultObject[]> [-InstallInternetServer <Boolean>] [-MinFreeSpaceMB <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-PrimarySiteCode <String>] [-SecondaryContentLibraryLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] -SecondarySiteCode <String> -ServerName <String>
 -SiteName <String> -SqlServerSetting <IResultObject[]> [-ValidateContentSchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMSecondarySite** cmdlet creates a secondary site. For more information, see [Prepare to install Configuration Manager sites](/mem/configmgr/core/servers/deploy/install/prepare-to-install-sites).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a secondary site

This first command creates a SQL Server settings object. This object specifies that Microsoft SQL Server Express is copied to a Configuration Manager secondary site. The command stores the object in the **$CIObj** variable.

The second command creates a secondary site named **Contoso remote site** that has the site code **CM2** on the server named **server2.corp.contoso.com**.
The command specifies the SQL Server settings object for the secondary sited stored in $CIObj.
The command specifies the primary site for the secondary site that has the site code **CM1**.

```powershell
$CIObj = New-CMSqlServerSetting -CopySqlServerExpressOnSecondarySite

New-CMSecondarySite -CertificateExpirationTimeUtc "2/1/2020 12:00 AM" -CreateSelfSignedCertificate -Https -InstallationSourceFile "\\ContosoServer1\SourceFiles" -InstallInternetServer $True -ParentSiteCode "CM1" -ServerName "server2.corp.contoso.com" -SiteCode "CM2" -SiteName "Contoso remote site" -SqlServerSetting $CIObj
```

## PARAMETERS

### -AllowFallbackForContent

Indicates whether clients can use a fallback source location for content.

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

### -AllowPreStaging

Indicates whether the secondary site can prestage content.

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

### -BoundaryGroup

Specify an array of boundary group objects for this site system. To get this object, use the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: BoundaryGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateExpirationTimeUtc

Specifies the date and time at which the self-signed certificate expires for a distribution point on the secondary site.

```yaml
Type: DateTime
Parameter Sets: NewDistributionPointByHTTPAndCreateCertificate, NewDistributionPointByHTTPSAndCreateCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword

Specifies the password for the PKI imported certificate for the distribution point.

```yaml
Type: SecureString
Parameter Sets: NewDistributionPointByHTTPSAndImportCertificate, NewDistributionPointByHTTPAndImportCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePath

Specifies the import path for the PKI issued certificate that the distribution point uses.
This parameter applies when the secondary site has installed and configured IIS to create a distribution point.

```yaml
Type: String
Parameter Sets: NewDistributionPointByHTTPSAndImportCertificate, NewDistributionPointByHTTPAndImportCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientConnectionType

Specifies the client connection type.

```yaml
Type: ClientConnectionTypes
Parameter Sets: NewDistributionPointByHTTPSAndCreateCertificate, NewDistributionPointByHTTPSAndImportCertificate
Aliases:
Accepted values: Intranet, Internet, InternetAndIntranet

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentMonitoringPriority

Specifies the content monitoring priority.

```yaml
Type: Priority
Parameter Sets: (All)
Aliases:
Accepted values: Lowest, Low, Medium, High, Highest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateSelfSignedCertificate

Indicates that the secondary site creates a self-signed certificate for the distribution point.

```yaml
Type: SwitchParameter
Parameter Sets: NewDistributionPointByHTTPAndCreateCertificate, NewDistributionPointByHTTPSAndCreateCertificate
Aliases:

Required: True
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

### -EnableAnonymous

Indicates whether client computers communicate anonymously with the distribution point.
This parameter applies when the secondary site has installed and configured IIS to create a distribution point.

```yaml
Type: Boolean
Parameter Sets: NewDistributionPointByHTTPAndCreateCertificate, NewDistributionPointByHTTPAndImportCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableBranchCache

Indicates that clients that use Windows BranchCache are allowed to download content from an on-premises distribution point.

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

### -ForceWhenDuplicateCertificate

Indicates whether Configuration Manager overwrites a duplicate certificate when you import a PKI client certificate for the secondary site.

```yaml
Type: Boolean
Parameter Sets: NewDistributionPointByHTTPSAndImportCertificate, NewDistributionPointByHTTPAndImportCertificate
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

### -Http

Indicates that client computers communicate with the distribution point by using HTTP.
This parameter applies when the secondary site has installed and configured IIS to create a distribution point.
\
```yaml
Type: SwitchParameter
Parameter Sets: NewDistributionPointByHTTPAndCreateCertificate, NewDistributionPointByHTTPAndImportCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Https

Indicates that client computers communicate with the distribution point by using HTTPS.
This parameter applies when the secondary site has installed and configured IIS to create a distribution point.

```yaml
Type: SwitchParameter
Parameter Sets: NewDistributionPointByHTTPSAndCreateCertificate, NewDistributionPointByHTTPSAndImportCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportCertificate

Indicates that the cmdlet imports a PKI certificate instead of using a self-signed certificate for the distribution point.

```yaml
Type: SwitchParameter
Parameter Sets: NewDistributionPointByHTTPSAndImportCertificate, NewDistributionPointByHTTPAndImportCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallInternetServer

Specifies whether to install and configure IIS if Configuration Manager requires it.
This parameter must be `$True` before the cmdlet installs the site system role for the distribution point on the secondary site.

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

### -InstallationFolder

Specifies the installation folder on the secondary site server where the cmdlet installs the site files.

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstallDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationSourceFile

Specifies an array of installation source file objects for Configuration Manager. To get this object, use the [New-CMInstallationSourceFile](New-CMInstallationSourceFile.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinFreeSpaceMB

Specifies the amount of space, in megabytes, to reserve on each drive that the distribution point uses.
This value determines the remaining free space on the drive after the distribution stores content on the drive.

Starting in version 2107, the default minimum free space changed from 200 MB to **500 MB**.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryContentLibraryLocation

Specifies a primary content library location.

```yaml
Type: DriveType
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryPackageShareLocation

Specifies a primary package share location.

```yaml
Type: DriveType
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimarySiteCode

Specify the three-character site code of the parent site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ParentSiteCode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondaryContentLibraryLocation

Specifies a secondary content library location.

```yaml
Type: DriveType
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondaryPackageShareLocation

Specifies a secondary package share location.

```yaml
Type: DriveType
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondarySiteCode

Specify a unique three-character site code for the secondary site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SiteCode

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName

Specify the fully qualified domain name (FQDN) of the server to use as the secondary site server.

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

### -SiteName

Specifies the site name that helps identify the secondary site.

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

### -SqlServerSetting

Specifies an array of SQL Server settings object in Configuration Manager. To get this object, use the [New-CMSqlServerSetting](New-CMSqlServerSetting.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidateContentSchedule

Specifies an object that represents a schedule type. It determines how frequently Configuration Manager validates the integrity of packages on the distribution point. To create a schedule token object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
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

### None
## OUTPUTS

### IResultObject#SMS_Site
### IResultObject#SMS_SCI_SiteDefinition
### IResultObject#SMS_SCI_SysResUse
### IResultObject[]#SMS_SCI_Address
## NOTES

For more information on this return object and its properties, see [SMS_SCI_SysResUse server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_sysresuse-server-wmi-class).

## RELATED LINKS

[New-CMInstallationSourceFile](New-CMInstallationSourceFile.md)

[New-CMSqlServerSetting](New-CMSqlServerSetting.md)

[Remove-CMSecondarySite](Remove-CMSecondarySite.md)
