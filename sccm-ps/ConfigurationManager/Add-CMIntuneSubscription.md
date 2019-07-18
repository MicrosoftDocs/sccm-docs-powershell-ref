---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
ms.assetid: E3DB3EC2-E24E-4CEC-A7F4-92CF76D058D2
online version: https://go.microsoft.com/fwlink/?linkid=833688
schema: 2.0.0
---

# Add-CMIntuneSubscription

## SYNOPSIS
Adds a Microsoft Intune subscription.

## SYNTAX

```
Add-CMIntuneSubscription [-ColorScheme <Color>] [-CompanyLogoPath <String>] [-CompanyLogoThemedPath <String>]
 -CompanyName <String> [-CompanyNameWithLogo] [-ContactAdditional <String>] [-ContactEmail <String>]
 [-ContactName <String>] [-ContactPhoneNumber <String>] -IntuneCredential <PSCredential>
 [-MaximumUserDevice <Int32>] [-MultifactorEnabled] [-OnPremOnly] [-PrivacyUrl <String>] [-SiteCode <String>]
 [-SupportSiteName <String>] [-SupportUrl <String>] -UserCollection <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMIntuneSubscription** cmdlet adds a Microsoft Intune subscription to Microsoft System Center Configuration Manager.
You must provide credentials for a Microsoft Intune organizational account.

NOTE:  You can only add a Microsoft Intune subscription to a Central Administration Site or  a stand-alone primary site.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Add a Microsoft Intune subscription
```
PS XYZ:\> $SecPasswd = ConvertTo-SecureString "P@ssW0rD! -AsPlainText -Force
PS XYZ:\> MyCreds = New-Object System.Management.Automation.PSCredential ("AccountName@CompanyName.onmicrosoft.com", $SecPasswd)
PS XYZ:\> $UC = Get-CMUserCollection -Name "All Users"
PS XYZ:\> Add-CMIntuneSubscription -CompanyName "CompanyName" -IntuneCredential $MyCreds -UserCollection $UC
```

The first command converts a password into a secure string and stores the secure string in the $SecPasswd variable.

The second command creates a **PSCredential** object with a Microsoft Intune organizational account and the password stored in $SecPassword.
The command then stores the **PSCredential** object in the $MyCreds variable.

The third command gets the user collection object named "All Users" and stores the object in the $UC variable.

The last command adds a Microsoft Intune subscription using the Intune credentials stored in $MyCreds, and the user collection stored in $UC.

## PARAMETERS

### -ColorScheme
Specifies a color scheme for the company portal.

```yaml
Type: Color
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CompanyLogoPath
Specifies the path to the company logo to use when the company portal background is white.

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

### -CompanyLogoThemedPath
Specifies the path to the company logo to use when the company portal background has a color scheme.

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

### -CompanyName
Specifies a company name.

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

### -CompanyNameWithLogo
Indicates that the company name is displayed next to the company logo.

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

### -ContactAdditional
Specifies additional company contact information.

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

### -ContactEmail
Specifies the IT department email address.

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

### -ContactName
Specifies the IT department contact name.

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

### -ContactPhoneNumber
Specifies the IT department phone number.

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

### -IntuneCredential
Specifies, as a **PSCredential**, a Microsoft Intune organizational account and password.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Credentials, Credential

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumUserDevice
Specifies the maximum number of devices that a user can enroll.

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

### -MultifactorEnabled
Indicates that multi-factor authentication is enabled.
This applies to Windows 8.1 or later and Windows Phone 8.1 or later device enrollment.

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

### -OnPremOnly
Indicates that only devices on premises are managed.
Information from devices on premises do not replicate to the cloud.

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

### -PrivacyUrl
Specifies the URL to company privacy documentation.

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
Specifies the Configuration Manager site code for device assignment.

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

### -SupportSiteName
Specifies the name of the support website.
The website name is displayed to users.

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

### -SupportUrl
Specifies the URL to the support website.
The URL is not displayed to users.

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

### -UserCollection
Specifies a user collection.
To obtain a user collection object, use the Get-CMUserCollection or Get-CMCollection cmdlet.
Members of this user collection will be able to enroll their devices for management.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: Collection

Required: True
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

[Get-CMIntuneSubscription](Get-CMIntuneSubscription.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Remove-CMIntuneSubscription](Remove-CMIntuneSubscription.md)

[Set-CMIntuneSubscription](Set-CMIntuneSubscription.md)


