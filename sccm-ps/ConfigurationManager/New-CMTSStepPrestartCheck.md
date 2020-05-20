---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMTSStepPrestartCheck

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
New-CMTSStepPrestartCheck [-CheckSpace <Boolean>] [-DiskSpace <Int32>] [-CheckPowerState <Boolean>]
 [-CheckNetworkConnected <Boolean>] [-CheckNetworkWired <Boolean>] [-CheckMemory <Boolean>] [-Memory <Int32>]
 [-CheckOSLanguageId <Boolean>] [-OSLanguageId <Int32>] [-CheckOS <Boolean>] [-OS <OSType>]
 [-CheckOSArchitecture <Boolean>] [-OSArchitecture <OSArch>] [-CheckMinOSVersion <Boolean>]
 [-MinOSVersion <String>] [-CheckMaxOSVersion <Boolean>] [-MaxOSVersion <String>]
 [-CheckCMClientMinVersion <Boolean>] [-CMClientMinVersion <String>] [-CheckSpeed <Boolean>] [-Speed <Int32>]
 -Name <String> [-Description <String>] [-ContinueOnError] [-Disable] [-Condition <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -CheckCMClientMinVersion
{{ Fill CheckCMClientMinVersion Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CheckClientMinVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckMaxOSVersion
{{ Fill CheckMaxOSVersion Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckMaxOSVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckMemory
{{ Fill CheckMemory Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckMemory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckMinOSVersion
{{ Fill CheckMinOSVersion Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckMinOSVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckNetworkConnected
{{ Fill CheckNetworkConnected Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: NetworkConnected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckNetworkWired
{{ Fill CheckNetworkWired Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: NetworkWired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckOS
{{ Fill CheckOS Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckOSType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckOSArchitecture
{{ Fill CheckOSArchitecture Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckOSArchitecture

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckOSLanguageId
{{ Fill CheckOSLanguageId Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableOSLanguageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckPowerState
{{ Fill CheckPowerState Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: NotBattery

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckSpace
{{ Fill CheckSpace Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckFreeDiskSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckSpeed
{{ Fill CheckSpeed Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckProcessorSpeed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CMClientMinVersion
{{ Fill CMClientMinVersion Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClientMinVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Condition
{{ Fill Condition Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Conditions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinueOnError
{{ Fill ContinueOnError Description }}

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

### -Description
{{ Fill Description Description }}

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

### -Disable
{{ Fill Disable Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableThisStep

Required: False
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

### -DiskSpace
{{ Fill DiskSpace Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinimumFreeDiskSpace

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

### -MaxOSVersion
{{ Fill MaxOSVersion Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: CurrentMaxOSVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Memory
{{ Fill Memory Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinimumMemory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinOSVersion
{{ Fill MinOSVersion Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: CurrentMinOSVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OS
{{ Fill OS Description }}

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: CurrentOSType
Accepted values: Client, Server

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSArchitecture
{{ Fill OSArchitecture Description }}

```yaml
Type: OSArch
Parameter Sets: (All)
Aliases: CurrentOSArchitecture
Accepted values: Arch32, Arch64

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSLanguageId
{{ Fill OSLanguageId Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: LanguageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Speed
{{ Fill Speed Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinimumProcessorSpeed

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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_PrestartCheckAction

## NOTES

## RELATED LINKS
