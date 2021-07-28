---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
online version:
schema: 2.0.0
---

# Get-CMConfigurationPlatform

## SYNOPSIS

Get an OS platform for a requirement rule.

## SYNTAX

### SearchByName (Default)
```
Get-CMConfigurationPlatform [-Fast] [-IsSupported <Boolean>] [[-Name] <String>]
 [-PlatformOption <PlatformType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMConfigurationPlatform [-Fast] [-Id] <Int32> [-IsSupported <Boolean>] [-PlatformOption <PlatformType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get an OS platform to use with an OS requirement rule for an application deployment type. You can use the output object of this cmdlet with the **New-CMRequirementRuleOperatingSystemValue** cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a requirement rule for an OS by platform

This example first uses the **Get-CMGlobalCondition** cmdlet to get the default **Operating system** global condition for non-mobile Windows devices. It then defines variables for two platforms for Windows Server 2016 and Windows Server 2019. Next it uses the **New-CMRequirementRuleOperatingSystemValue** cmdlet to create the requirement rule object to include these two platforms. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

```powershell
$myGC = Get-CMGlobalCondition -Name "Operating System" | Where-Object PlatformType -eq 1

$platformA = Get-CMConfigurationPlatform -Name "All Windows Server 2019 and higher (64-bit)"

$platformB = Get-CMConfigurationPlatform -Name "All Windows Server 2016 and higher (64-bit)"

$myRule = $myGC | New-CMRequirementRuleOperatingSystemValue -RuleOperator OneOf -Platform $platformA, $platformB

Set-CMScriptDeploymentType -ApplicationName "Central App" -DeploymentTypeName "Install" -AddRequirement $myRule
```

## PARAMETERS

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

Specify the integer value for the **CI_ID** of the platform. For example, the **CI_ID** for the platform **All Windows Server 2019 and higher (64-bit)** is `287650`.

Use a command similar to the following to discover the CI_ID for a platform:

`Get-CMConfigurationPlatform -Name "*Server 2019*" | Select-Object LocalizedDisplayName, CI_ID`

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsSupported

Configuration Manager still defines legacy platforms for backward compatibility. Set this parameter to `$true` to filter the results to only platforms that are currently supported.

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

Specify the name of the OS platform. You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlatformOption

Use this parameter to filter the results by platform type.

```yaml
Type: PlatformType
Parameter Sets: (All)
Aliases:
Accepted values: None, Windows, Mobile, Mac, MixedPlatform

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_ConfigurationPlatform
### IResultObject#SMS_ConfigurationPlatform
## NOTES

For more information on this return object and its properties, see [SMS_ConfigurationPlatform server WMI class](/mem/configmgr/develop/reference/compliance/sms_configurationplatform-server-wmi-class).

This cmdlet is different from the similar **Get-CMSupportedPlatform** cmdlet.

## RELATED LINKS

[New-CMRequirementRuleOperatingSystemValue](New-CMRequirementRuleOperatingSystemValue.md)
