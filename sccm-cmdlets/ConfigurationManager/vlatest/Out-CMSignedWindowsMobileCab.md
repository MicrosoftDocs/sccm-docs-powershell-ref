---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 51DF5E48-B29A-4A17-9DBD-29DAB1D5B1B8
---

# Out-CMSignedWindowsMobileCab

## SYNOPSIS
Signs a Windows Mobile CAB file.

## SYNTAX

```
Out-CMSignedWindowsMobileCab [-ContentLocation] <String> -PfxPassword <SecureString> -PfxFilePath <String>
 -OutputPath <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Out-CMSignedWindowsMobileCab** cmdlet signs a Windows Mobile cabinet file and places the signed file in the specified location.

## EXAMPLES

### Example 1: Sign a Windows Mobile CAB file
```
PS C:\>Out-CMSignedWindowsMobileCab -ContentLocation "\\Server1\Applications\Cab\Test.CAB" -PfxFilePath "\\Server1\Applications\sign\sign3.pfx" -PfxPassword $SecureString -OutputPath "\\Server1\Applications\Cab\TestSigned.CAB"
```

This command signs the Windows Mobile CAB file named Test.CAB using the provided certificate and password.
The signed CAB file is placed in the specified output path.

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

### -ContentLocation
Specifies the path of the content.
The site system server requires permissions to read the content files.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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

### -OutputPath
Specifies the output file path for the signed Windows Mobile CAB file.

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

### -PfxFilePath
Specifies the path of a PFX file.

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

### -PfxPassword
Specifies the PFX password as a secured string.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

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


