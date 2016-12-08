---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833893
schema: 2.0.0
ms.assetid: FCD17E0C-355E-4AE5-87E4-2ADA5754A7C3
---

# Remove-CMApplication

## SYNOPSIS
Removes an application from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMApplication -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMApplication [-Name] <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMApplication -Id <Int32> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByModelName
```
Remove-CMApplication -ModelName <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMApplication** cmdlet removes an application from Microsoft System Center Configuration Manager so that it cannot be installed by clients.
This cmdlet does not remove any existing client installations.

## EXAMPLES

### Example 1: Get an application and remove it
```
PS C:\> Get-CMApplication -Name "Application1" | Remove-CMApplication -Force
```

The first command gets the application object named Application1 and uses the pipeline operator to pass the object to **Remove-CMApplication**, which removes the application.
Specifying the *Force* parameter indicates that the user is not prompted before the application is removed.

### Example 2: Remove an application by model name
```
PS C:\> Remove-CMApplication -ModelName "ScopeId_5E88BBB4-B1D1-4B74-8A4F-9E8B03BC1EB0/Application_7aa0ed27-6240-4070-a098-3edc9281dd96" -Force
```

This command removes the application object with the specified model name.
Specifying the *Force* parameter indicates that the user is not prompted before the application is removed.

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

### -Id
Specifies the CI_ID and ModelID properties (the same value) of an application.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an application object.
To obtain an application object, use the [Get-CMApplication](./Get-CMApplication.md) cmdlet.

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

### -ModelName
Specifies the model name of the application.

```yaml
Type: String
Parameter Sets: SearchByModelName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the application.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName, ApplicationName
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

[Convert-CMApplication](./Convert-CMApplication.md)

[ConvertFrom-CMApplication](./ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](./ConvertTo-CMApplication.md)

[Get-CMApplication](./Get-CMApplication.md)

[Export-CMApplication](./Export-CMApplication.md)

[Import-CMApplication](./Import-CMApplication.md)

[New-CMApplication](./New-CMApplication.md)

[Resume-CMApplication](./Resume-CMApplication.md)

[Set-CMApplication](./Set-CMApplication.md)

[Suspend-CMApplication](./Suspend-CMApplication.md)


