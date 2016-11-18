---
external help file: AdminUI.PS.Dcm-help.xml
online version: 
schema: 2.0.0
ms.assetid: E9001728-AB67-49A6-BFBA-5CDC37B64185
---

# Get-CMEmailProfile

## SYNOPSIS
Gets an email profile.

## SYNTAX

### ByValue (Default)
```
Get-CMEmailProfile [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMEmailProfile [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMEmailProfile [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEmailProfile** function gets an Exchange ActiveSync email profile.

## EXAMPLES

### Example 1: Get an email profile by name
```
PS C:\> Get-CMEmailProfile -Name "EmailProfile1"
```

This command gets the Exchange ActiveSync email profile with the name EmailProfile1.

### Example 2: Get an email profile by ID
```
PS C:\> Get-CMEmailProfile -ID 16795653
```

This command gets the Exchange ActiveSync email profile with the CI_ID of 16795653.

### Example 3: Get all email profiles
```
PS C:\> Get-CMEmailProfile -Fast
```

This command gets all Exchange ActiveSync email profiles.
The command does not return lazy properties.

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
Specifies the CI_ID of an email profile.

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
Specifies the name of an email profile.

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

[New-CMEmailProfile](./New-CMEmailProfile.md)

[Set-CMEmailProfile](./Set-CMEmailProfile.md)


