---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/04/2020
online version:
schema: 2.0.0
---

# Get-CMMicrosoftEdgeBrowserProfiles

## SYNOPSIS

Get a policy for a Microsoft Edge Legacy browser profile.

## SYNTAX

### ByValue (Default)
```
Get-CMMicrosoftEdgeBrowserProfiles [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMMicrosoftEdgeBrowserProfiles [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMMicrosoftEdgeBrowserProfiles [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION

Get a policy for a Microsoft Edge Legacy browser profile. This policy only applies to clients on Windows 10, version 1703 or later, and Microsoft Edge Legacy version 45 and earlier. For more information, see [Configure Microsoft Edge Legacy settings in Configuration Manager](/mem/configmgr/compliance/deploy-use/browser-profiles).

For more information on managing Microsoft Edge version 77 or later with Configuration Manager, see [Deploy Microsoft Edge, version 77 and later](/mem/configmgr/apps/deploy-use/deploy-edge). For more information on configuring policies for Microsoft Edge version 77 or later, see [Microsoft Edge - Policies](/DeployEdge/microsoft-edge-policies).

## EXAMPLES

### Example 1

This example uses the **Fast** parameter to quickly get an object by its ID without loading lazy properties, and then only displays the policy name.

```powershell
Get-CMMicrosoftEdgeBrowserProfiles -Id 88156 -Fast | Select-Object LocalizedDisplayName
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

Specify the **CI ID** of the browser profile to get. The format is a five- to seven-digit number, for example `403823`.

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

Specify the name of the browser profile to get.

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

[New-CMMicrosoftEdgeBrowserProfiles](New-CMMicrosoftEdgeBrowserProfiles.md)

[Set-CMMicrosoftEdgeBrowserProfiles](Set-CMMicrosoftEdgeBrowserProfiles.md)

[Configure Microsoft Edge Legacy settings in Configuration Manager](/mem/configmgr/compliance/deploy-use/browser-profiles)
