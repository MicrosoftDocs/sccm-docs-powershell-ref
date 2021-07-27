---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/04/2020
online version:
schema: 2.0.0
---

# Get-CMOneDriveBusinessProfile

## SYNOPSIS

Get a policy for a OneDrive for Business profile.

## SYNTAX

### ByValue (Default)
```
Get-CMOneDriveBusinessProfile [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMOneDriveBusinessProfile [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMOneDriveBusinessProfile [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION

Get a policy for a OneDrive for Business profile. For more information, see [OneDrive for Business profiles](/mem/configmgr/compliance/deploy-use/onedrive-profile).

## EXAMPLES

### Example 1

```powershell
Get-CMOneDriveBusinessProfile -Id 584750
```

## PARAMETERS

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

Specify the **CI ID** of the OneDrive for Business policy to get. The format is a five- to seven-digit number, for example `403823`.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the OneDrive for Business policy to get.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMOneDriveBusinessProfile](New-CMOneDriveBusinessProfile.md)

[Set-CMOneDriveBusinessProfile](Set-CMOneDriveBusinessProfile.md)

[OneDrive for Business profiles](/mem/configmgr/compliance/deploy-use/onedrive-profile)
