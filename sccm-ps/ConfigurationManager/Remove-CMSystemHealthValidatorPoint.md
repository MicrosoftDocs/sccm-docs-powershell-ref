---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834244
schema: 2.0.0
ms.assetid: 5698669F-6E97-49CB-9F0E-561CED6FE3E0
---

# Remove-CMSystemHealthValidatorPoint

## SYNOPSIS
Removes a system health validator point from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMSystemHealthValidatorPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSystemHealthValidatorPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSystemHealthValidatorPoint** cmdlet removes a system health validator point from a Microsoft System Center Configuration Manager site.
This site system role validates statements of health from a server that is running Network Policy Server (NPS).
You can specify a validator point by site system name or site code or both or you can use the Get-CMSystemHealthValidatorPoint cmdlet.

Before you remove a system health validator point, make sure that there is another system health validator point for the site, or that the server that is running NPS has policies that grant network access and do not reference the System Center Configuration Manager.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove a validator point
```
PS XYZ:\> Remove-CMSystemHealthValidatorPoint -SiteCode "CM1" -SiteSystemServerName "Test01.TSQA.Contoso.com"
```

This command removes a system health validator point.
The command specifies the site code and the name of the server that hosts that system role.

### Example 2: Remove a validator point by using a variable
```
PS XYZ:\> $CMSHVP = Get-CMSystemHealthValidatorPoint -SiteCode "CM1" -SiteSystemServerName "Test01.TSQA.Contoso.com" 
PS XYZ:\> Remove-CMSystemHealthValidatorPoint -InputObject $CMSHVP
```

The first command gets the system role that has the specified site code and host name and stores it in the $CMSHVP variable.

The second command removes the system health validator point stored in the $CMSHVP variable.

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
Specifies a system health validator point object.
To obtain a system health validator point object, use **Get-CMSystemHealthValidatorPoint**.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: SystemHealthValidatorPoint
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

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
Specifies the host name for a system health validator point.

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

[Add-CMSystemHealthValidatorPoint](Add-CMSystemHealthValidatorPoint.md)

[Get-CMSystemHealthValidatorPoint](Get-CMSystemHealthValidatorPoint.md)


