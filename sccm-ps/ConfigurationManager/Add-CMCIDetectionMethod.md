---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2020
online version:
schema: 2.0.0
---

# Add-CMCIDetectionMethod

## SYNOPSIS

Specify how the client detects an application.

## SYNTAX

```
Add-CMCIDetectionMethod [-InputObject] <IResultObject> -DetectionOption <ApplicationDetectionMethod>
 [-MsiFilePath <String>] [-IsPerUserInstallation <Boolean>] [-ScriptFile <String>]
 [-ScriptLanguage <ScriptingLanguage>] [-ScriptText <String>] [-ApplicationName <String>]
 [-DeploymentTypeId <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet specifies how the client detects an application on the device. There are three detection methods: Windows Installer detection, detection by a specific application and deployment type, and a custom script to detect the application.

## EXAMPLES

### Example 1: Windows Installer detection

```powershell
$ci = Get-CMConfigurationItem -Name "testCI"

$msiFilePath = "C:\tools\CCMTools\Orca.Msi"

$ci | Add-CMCIDetectionMethod -DetectionOption Msi -MsiFilePath $msiFilePath
```

### Example 2: Specific app and deployment type

```powershell
$ci = Get-CMConfigurationItem -Name "testCI"

$ci | Add-CMCIDetectionMethod -DetectionOption DeploymentType -ApplicationName "testApp" -DeploymentTypeId "392672"
```

### Example 3: Custom script detection

```powershell
$ci = Get-CMConfigurationItem -Name "testCI"

$scriptFile  = "C:\share\testScript.ps1"

$ci | Add-CMCIDetectionMethod -DetectionOption Script -ScriptLanguage PowerShell -ScriptFile $scriptFile
```

## PARAMETERS

### -ApplicationName

When you set the **DetectionOption** to `DeploymentType`, use this parameter to specify the name of a Configuration Manager application. Use this parameter with **DeploymentTypeID**.

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

### -DeploymentTypeId

When you set the **DetectionOption** to `DeploymentType`, use this parameter to specify the ID of deployment type of the Configuration Manager application. Use this parameter with **ApplicationName**.

To get the deployment type ID, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet, and reference the **CI_ID** property.

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

### -DetectionOption

Specify the method of detection to use.

```yaml
Type: ApplicationDetectionMethod
Parameter Sets: (All)
Aliases:
Accepted values: None, Msi, Script, DeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InputObject

Specify a configuration item object for an application deployment type. To get this object, use [Get-CMConfigurationItem](Get-CMConfigurationItem.md).

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsPerUserInstallation

Set this parameter to `$true` to specify that it's installed per user.

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

### -MsiFilePath

When you set **DetectionOption** to `Msi`, use this parameter to specify the path to the Windows Installer file.

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

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -ScriptFile

When you set **DetectionOption** to `Script`, use this parameter to specify the path to the script. Use this parameter with **ScriptLanguage**.

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

### -ScriptLanguage

When you set **DetectionOption** to `Script`, use this parameter to specify the language of the script. Use this parameter with **ScriptFile** and **ScriptText**.

```yaml
Type: ScriptingLanguage
Parameter Sets: (All)
Aliases: ScriptType
Accepted values: PowerShell, VBScript, JScript

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptText

When you set **DetectionOption** to `Script`, use this parameter to specify the text of the script. Use this parameter with **ScriptLanguage**.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ScriptContent

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)
[Get-CMDeploymentType](Get-CMDeploymentType.md)
