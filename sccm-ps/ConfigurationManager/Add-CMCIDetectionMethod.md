---
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Add-CMCIDetectionMethod

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
Add-CMCIDetectionMethod [-InputObject] <IResultObject> -DetectionOption <ApplicationDetectionMethod>
 [-MsiFilePath <String>] [-IsPerUserInstallation <Boolean>] [-ScriptFile <String>]
 [-ScriptLanguage <ScriptingLanguage>] [-ScriptText <String>] [-ApplicationName <String>]
 [-DeploymentTypeId <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -ApplicationName
{{ Fill ApplicationName Description }}

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
{{ Fill DeploymentTypeId Description }}

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
{{ Fill DetectionOption Description }}

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
{{ Fill DisableWildcardHandling Description }}

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
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill InputObject Description }}

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
{{ Fill IsPerUserInstallation Description }}

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
{{ Fill MsiFilePath Description }}

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
{{ Fill PassThru Description }}

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
{{ Fill ScriptFile Description }}

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
{{ Fill ScriptLanguage Description }}

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
{{ Fill ScriptText Description }}

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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
