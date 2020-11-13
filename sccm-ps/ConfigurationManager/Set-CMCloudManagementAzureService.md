---
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMCloudManagementAzureService

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMCloudManagementAzureService [-AddGroupName <String[]>] [-DeleteGroupName <String[]>]
 [-Description <String>] [-EnableAADGroupSync <Boolean>] [-EnableGroupDeltaDiscovery <Boolean>]
 [-EnableGroupDiscovery <Boolean>] [-EnableUserDeltaDiscovery <Boolean>] [-EnableUserDiscovery <Boolean>]
 [-GroupDeltaDiscoveryMins <Int32>] [-GroupDiscoverySchedule <IResultObject>] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-UserDeltaDiscoveryMins <Int32>] [-UserDiscoverySchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMCloudManagementAzureService [-AddGroupName <String[]>] [-DeleteGroupName <String[]>]
 [-Description <String>] [-EnableAADGroupSync <Boolean>] [-EnableGroupDeltaDiscovery <Boolean>]
 [-EnableGroupDiscovery <Boolean>] [-EnableUserDeltaDiscovery <Boolean>] [-EnableUserDiscovery <Boolean>]
 [-GroupDeltaDiscoveryMins <Int32>] [-GroupDiscoverySchedule <IResultObject>] -Id <Int32> [-NewName <String>]
 [-PassThru] [-UserDeltaDiscoveryMins <Int32>] [-UserDiscoverySchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMCloudManagementAzureService [-AddGroupName <String[]>] [-DeleteGroupName <String[]>]
 [-Description <String>] [-EnableAADGroupSync <Boolean>] [-EnableGroupDeltaDiscovery <Boolean>]
 [-EnableGroupDiscovery <Boolean>] [-EnableUserDeltaDiscovery <Boolean>] [-EnableUserDiscovery <Boolean>]
 [-GroupDeltaDiscoveryMins <Int32>] [-GroupDiscoverySchedule <IResultObject>] -Name <String>
 [-NewName <String>] [-PassThru] [-UserDeltaDiscoveryMins <Int32>] [-UserDiscoverySchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -AddGroupName
{{ Fill AddGroupName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddGroupNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteGroupName
{{ Fill DeleteGroupName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DeleteGroupNames

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

### -EnableAADGroupSync
{{ Fill EnableAADGroupSync Description }}

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

### -EnableGroupDeltaDiscovery
{{ Fill EnableGroupDeltaDiscovery Description }}

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

### -EnableGroupDiscovery
{{ Fill EnableGroupDiscovery Description }}

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

### -EnableUserDeltaDiscovery
{{ Fill EnableUserDeltaDiscovery Description }}

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

### -EnableUserDiscovery
{{ Fill EnableUserDiscovery Description }}

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

### -GroupDeltaDiscoveryMins
{{ Fill GroupDeltaDiscoveryMins Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupDiscoverySchedule
{{ Fill GroupDiscoverySchedule Description }}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
{{ Fill Id Description }}

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: AzureService

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: AzureServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
{{ Fill NewName Description }}

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

### -UserDeltaDiscoveryMins
{{ Fill UserDeltaDiscoveryMins Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDiscoverySchedule
{{ Fill UserDiscoverySchedule Description }}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

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
