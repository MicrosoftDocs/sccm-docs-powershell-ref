---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834098
schema: 2.0.0
ms.assetid: 101E23A6-5318-4AA7-81EF-59AA9CE44B67
---

# Remove-CMEnrollmentProxyPoint

## SYNOPSIS
Removes an enrollment proxy point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMEnrollmentProxyPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMEnrollmentProxyPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMEnrollmentProxyPoint** cmdlet removes an enrollment proxy point in Microsoft System Center Configuration Manager.
An enrollment proxy point is a site system role that manages enrollment requests from mobile devices.
After you remove an enrollment proxy point, mobile devices must use a different enrollment proxy point.

## EXAMPLES

### Example 1: Remove an enrollment proxy point
```
PS C:\>Remove-CMEnrollmentProxyPoint -SiteCode "CM1" -SiteSystemServerName "SiteServer01.Contoso.com"
```

This command removes an enrollment proxy point.

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

### -InputObject
Specifies the input to this cmdlet.
You can get an input object by using the Get-CMEnrollmentProxyPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: EnrollmentProxyPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName

Required: True
Position: 0
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

[Add-CMEnrollmentProxyPoint](./Add-CMEnrollmentProxyPoint.md)

[Get-CMEnrollmentProxyPoint](./Get-CMEnrollmentProxyPoint.md)


