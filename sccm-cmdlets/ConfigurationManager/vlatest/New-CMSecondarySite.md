---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: F94DB807-7FB0-403F-A8D2-318E1A1AC933
online version: https://go.microsoft.com/fwlink/?linkid=833746
schema: 2.0.0
---

# New-CMSecondarySite

## SYNOPSIS
Creates a secondary site in Configuration Manager.

## SYNTAX

### NewDistributionPointByHTTPAndCreateCertificate (Default)
```
New-CMSecondarySite -SecondarySiteCode <String> -ServerName <String> -SiteName <String>
 [-InstallationFolder <String>] [-PrimarySiteCode <String>] -InstallationSourceFile <IResultObject[]>
 -SqlServerSetting <IResultObject[]> [-BoundaryGroup <IResultObject[]>] [-AllowFallbackForContent <Boolean>]
 [-InstallInternetServer <Boolean>] [-EnableBranchCache] [-Http] [-EnableAnonymous <Boolean>]
 [-CreateSelfSignedCertificate] -CertificateExpirationTimeUtc <DateTime> [-AllowPreStaging <Boolean>]
 [-MinFreeSpaceMB <Int32>] [-PrimaryContentLibraryLocation <DriveType>]
 [-SecondaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] [-ValidateContentSchedule <IResultObject>]
 [-ContentMonitoringPriority <Priority>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### NewDistributionPointByHTTPAndImportCertificate
```
New-CMSecondarySite -SecondarySiteCode <String> -ServerName <String> -SiteName <String>
 [-InstallationFolder <String>] [-PrimarySiteCode <String>] -InstallationSourceFile <IResultObject[]>
 -SqlServerSetting <IResultObject[]> [-BoundaryGroup <IResultObject[]>] [-AllowFallbackForContent <Boolean>]
 [-InstallInternetServer <Boolean>] [-EnableBranchCache] [-Http] [-EnableAnonymous <Boolean>]
 [-ImportCertificate] -CertificatePath <String> -CertificatePassword <SecureString>
 [-ForceWhenDuplicateCertificate <Boolean>] [-AllowPreStaging <Boolean>] [-MinFreeSpaceMB <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-SecondaryContentLibraryLocation <DriveType>]
 [-PrimaryPackageShareLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 [-ValidateContentSchedule <IResultObject>] [-ContentMonitoringPriority <Priority>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewDistributionPointByHTTPSAndCreateCertificate
```
New-CMSecondarySite -SecondarySiteCode <String> -ServerName <String> -SiteName <String>
 [-InstallationFolder <String>] [-PrimarySiteCode <String>] -InstallationSourceFile <IResultObject[]>
 -SqlServerSetting <IResultObject[]> [-BoundaryGroup <IResultObject[]>] [-AllowFallbackForContent <Boolean>]
 [-InstallInternetServer <Boolean>] [-EnableBranchCache] [-Https]
 [-ClientConnectionType <ClientConnectionTypes>] [-CreateSelfSignedCertificate]
 -CertificateExpirationTimeUtc <DateTime> [-AllowPreStaging <Boolean>] [-MinFreeSpaceMB <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-SecondaryContentLibraryLocation <DriveType>]
 [-PrimaryPackageShareLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 [-ValidateContentSchedule <IResultObject>] [-ContentMonitoringPriority <Priority>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewDistributionPointByHTTPSAndImportCertificate
```
New-CMSecondarySite -SecondarySiteCode <String> -ServerName <String> -SiteName <String>
 [-InstallationFolder <String>] [-PrimarySiteCode <String>] -InstallationSourceFile <IResultObject[]>
 -SqlServerSetting <IResultObject[]> [-BoundaryGroup <IResultObject[]>] [-AllowFallbackForContent <Boolean>]
 [-InstallInternetServer <Boolean>] [-EnableBranchCache] [-Https]
 [-ClientConnectionType <ClientConnectionTypes>] [-ImportCertificate] -CertificatePath <String>
 -CertificatePassword <SecureString> [-ForceWhenDuplicateCertificate <Boolean>] [-AllowPreStaging <Boolean>]
 [-MinFreeSpaceMB <Int32>] [-PrimaryContentLibraryLocation <DriveType>]
 [-SecondaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] [-ValidateContentSchedule <IResultObject>]
 [-ContentMonitoringPriority <Priority>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSecondarySite** cmdlet creates a secondary site in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Create a secondary site
```
PS C:\> $CIObj = New-CMSqlServerSetting -CopySqlServerExpressOnSecondarySite
PS C:\> New-CMSecondarySite -CertificateExpirationTimeUtc "2/1/2020 12:00 AM" -CreateSelfSignedCertificate -Https -InstallationSourceFile "\\ContosoServer1\SourceFiles" -InstallInternetServer $True -ParentSiteCode "CM1" -ServerName "server2.corp.contoso.com" -SiteCode "CM2" -SiteName "Contoso remote site" -SqlServerSetting $CIObj
```

This first command creates a SQL Server settings object and specifies that Microsoft SQL Server Express is copied to a Configuration Manager secondary site.
The command stores the object in the $CIObj variable.

The second command creates a secondary site named Contoso remote site that has the site code CM2 on the server named server2.corp.contoso.com.
The command specifies the SQL Server settings object for the secondary sited stored in $CIObj.
The command specifies the primary site for the secondary site that has the site code CM1.

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
Indicates whether the secondary site can pre-stage contents.

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
Parameter Sets: NewDistributionPointByHTTPAndImportCertificate, NewDistributionPointByHTTPSAndImportCertificate
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
Parameter Sets: NewDistributionPointByHTTPAndImportCertificate, NewDistributionPointByHTTPSAndImportCertificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientConnectionType
Specifies a client connection type.
The acceptable values for this parameter are:

- Internet 
- InternetAndIntranet
- Intranet

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
Specifies content monitoring priority.
The acceptable values for this parameter are:

- High 
- Highest 
- Low 
- Lowest 
- Medium

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
Indicates that the secondary site creates a self-signed certificate.

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
Content downloads from cloud-based distribution points can always be shared by clients that use Windows BranchCache.

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
Parameter Sets: NewDistributionPointByHTTPAndImportCertificate, NewDistributionPointByHTTPSAndImportCertificate
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

### -Http
Indicates that client computers communicate with the distribution point by using HTTP.
This parameter applies when the secondary site has installed and configured IIS to create a distribution point.
This option does not support mobile devices or computers running Mac OS.

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
This option does not support mobile devices or computers running Mac OS.

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
Parameter Sets: NewDistributionPointByHTTPAndImportCertificate, NewDistributionPointByHTTPSAndImportCertificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallInternetServer
Specifies whether to install and configure IIS if Configuration Manager requires it.
This parameter must be $True before the cmdlet installs the site system role for the distribution point on the secondary site.

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
Specifies an array of installation source file objects for Configuration Manager.
To obtain an installation source file object, use the New-CMInstallationSourceFile cmdlet.

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
The acceptable values for this parameter are:

- Automatic. 
- Drive letter from A: through Z:.

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
The acceptable values for this parameter are:

- Automatic. 
- Drive letter from A: through Z:.

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
The acceptable values for this parameter are:

- Automatic. 
- Drive letter from A: through Z:.

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
The acceptable values for this parameter are:

- Automatic. 
- Drive letter from A: through Z:.

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
Specifies a fully qualified domain name (FQDN) for the secondary site server.

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
Specifies an array of SQL Server settings object in Configuration Manager.
To obtain a SQL Server settings object, use the New-CMSqlServerSetting cmdlet.

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
Specifies an object that represents a schedule type and determines how frequently System Center Configuration Manager validates the integrity of packages on the distribution point.

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

[New-CMInstallationSourceFile](./New-CMInstallationSourceFile.md)

[New-CMSqlServerSetting](./New-CMSqlServerSetting.md)

[Remove-CMSecondarySite](./Remove-CMSecondarySite.md)
