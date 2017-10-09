---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-CMIosEnrollmentProfile

## SYNOPSIS
Sets an ios enrollment profile

## SYNTAX

### ByValue (Default)
```
Set-CMIosEnrollmentProfile [-InputObject] <IResultObject> [-NewName <String>] [-Description <String>]
 [-Affinity <AffinitySetting>] [-IsDepEnable <Boolean>] [-Department <String>] [-SupportPhone <String>]
 [-Preparation <PreparationMode>] [-IsMdmRemovable <Boolean>] [-Passcode <Boolean>] [-Location <Boolean>]
 [-Restore <Boolean>] [-AppleId <Boolean>] [-TermAndCondition <Boolean>] [-TouchId <Boolean>]
 [-ApplePay <Boolean>] [-Zoom <Boolean>] [-Siri <Boolean>] [-Diagnostic <Boolean>]
 [-AllowPairingType <PairingType>] [-ClearCertificatePath] [-RemoveCertificatePath <String[]>]
 [-AddCertificatePath <String[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMIosEnrollmentProfile [-Name] <String> [-NewName <String>] [-Description <String>]
 [-Affinity <AffinitySetting>] [-IsDepEnable <Boolean>] [-Department <String>] [-SupportPhone <String>]
 [-Preparation <PreparationMode>] [-IsMdmRemovable <Boolean>] [-Passcode <Boolean>] [-Location <Boolean>]
 [-Restore <Boolean>] [-AppleId <Boolean>] [-TermAndCondition <Boolean>] [-TouchId <Boolean>]
 [-ApplePay <Boolean>] [-Zoom <Boolean>] [-Siri <Boolean>] [-Diagnostic <Boolean>]
 [-AllowPairingType <PairingType>] [-ClearCertificatePath] [-RemoveCertificatePath <String[]>]
 [-AddCertificatePath <String[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMIosEnrollmentProfile -Id <String> [-NewName <String>] [-Description <String>]
 [-Affinity <AffinitySetting>] [-IsDepEnable <Boolean>] [-Department <String>] [-SupportPhone <String>]
 [-Preparation <PreparationMode>] [-IsMdmRemovable <Boolean>] [-Passcode <Boolean>] [-Location <Boolean>]
 [-Restore <Boolean>] [-AppleId <Boolean>] [-TermAndCondition <Boolean>] [-TouchId <Boolean>]
 [-ApplePay <Boolean>] [-Zoom <Boolean>] [-Siri <Boolean>] [-Diagnostic <Boolean>]
 [-AllowPairingType <PairingType>] [-ClearCertificatePath] [-RemoveCertificatePath <String[]>]
 [-AddCertificatePath <String[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddCertificatePath
{{Fill AddCertificatePath Description}}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddCertificatePaths

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Affinity
{{Fill Affinity Description}}

```yaml
Type: AffinitySetting
Parameter Sets: (All)
Aliases: UserAffinity
Accepted values: NoUserAffinity, PromptForUserAffinity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPairingType
{{Fill AllowPairingType Description}}

```yaml
Type: PairingType
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable, RequireCertificate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppleId
{{Fill AppleId Description}}

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

### -ApplePay
{{Fill ApplePay Description}}

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

### -ClearCertificatePath
{{Fill ClearCertificatePath Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearCertificate

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Department
{{Fill Department Description}}

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

### -Description
{{Fill Description Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProfileDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diagnostic
{{Fill Diagnostic Description}}

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

### -Id
{{Fill Id Description}}

```yaml
Type: String
Parameter Sets: ById
Aliases: ProfileId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{Fill InputObject Description}}

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsDepEnable
{{Fill IsDepEnable Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ConfigureDeviceEnrollmentProgram

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsMdmRemovable
{{Fill IsMdmRemovable Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: LockEnrollmentProfileToDevice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
{{Fill Location Description}}

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

### -Name
{{Fill Name Description}}

```yaml
Type: String
Parameter Sets: ByName
Aliases: ProfileName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
{{Fill NewName Description}}

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

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -Passcode
{{Fill Passcode Description}}

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

### -Preparation
{{Fill Preparation Description}}

```yaml
Type: PreparationMode
Parameter Sets: (All)
Aliases: 
Accepted values: Unsupervised, Supervised

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveCertificatePath
{{Fill RemoveCertificatePath Description}}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveCertificatePaths

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Restore
{{Fill Restore Description}}

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

### -Siri
{{Fill Siri Description}}

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

### -SupportPhone
{{Fill SupportPhone Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: SupportPhoneNumber

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TermAndCondition
{{Fill TermAndCondition Description}}

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

### -TouchId
{{Fill TouchId Description}}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zoom
{{Fill Zoom Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

