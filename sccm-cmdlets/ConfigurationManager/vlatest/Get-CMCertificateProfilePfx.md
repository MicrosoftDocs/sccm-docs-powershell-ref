---
external help file: AdminUI.PS.Dcm-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834166
schema: 2.0.0
ms.assetid: C2319974-8CEA-4FA1-99D0-24DA994351AE
---

# Get-CMCertificateProfilePfx

## SYNOPSIS
Gets a PFX certificate profile.

## SYNTAX

### ByValue (Default)
```
Get-CMCertificateProfilePfx [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMCertificateProfilePfx [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMCertificateProfilePfx [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificateProfilePfx** function gets a PFX certificate profile.

## EXAMPLES

### Example 1: Get a PFX certificate profile by name
```
PS C:\> Get-CMCertificateProfilePfx -Name "Test1"
```

This command gets the PFX certificate profile object named Test1.

### Example 2: Get a PFX certificate profile by ID
```
PS C:\> Get-CMcertificateprofilePfx -Id 16777499
```

This command gets the PFX certificate profile object with the ID of 16777499.

## PARAMETERS

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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
Specifies the ID of a PFX certificate profile.

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
Specifies the name of a PFX certificate profile.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
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

[New-CMCertificateProfilePfx](./New-CMCertificateProfilePfx.md)

[Set-CMCertificateProfilePfx](./Set-CMCertificateProfilePfx.md)


