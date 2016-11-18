---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: EFF80160-0FF7-4F76-A09A-2C55C29D7972
---

# Get-CMSoftwareUpdateLicense

## SYNOPSIS
Gets a EULA or SLT for a software update in Configuration Manager.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateLicense [-Name <String>] [-EulaAcceptance <EulaAcceptance>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMSoftwareUpdateLicense -InputObject <IResultObject> [-EulaAcceptance <EulaAcceptance>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateLicense** cmdlet gets an End User License Agreement (EULA) or Software License Terms (SLT) for a software update in Microsoft System Center Configuration Manager.
You can specify a software update by ID or by name or use the Get-CMSoftwareUpdate cmdlet to obtain one.
If you specify an ID or name, you can further specify a security scope membership.

## EXAMPLES

### Example 1: Get a EULA or SLT for a software update
```
PS C:\>Get-CMSoftwareUpdateLicense -Name "UpdatePkg01" -SecuredScopeNames "SecScope02"
```

This command gets the EULA or SLT for a software update named UpdatePkg01 for the security scope named SecScope02.

## PARAMETERS

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

### -EulaAcceptance


```yaml
Type: EulaAcceptance
Parameter Sets: (All)
Aliases: 
Accepted values: Declined, Accepted, Unknown

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
Specifies a software update object.
To obtain a software update object, use the **Get-CMSoftwareUpdate** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software updates.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru


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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdate](./Get-CMSoftwareUpdate.md)


