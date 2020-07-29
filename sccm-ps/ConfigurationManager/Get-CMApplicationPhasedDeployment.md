---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMApplicationPhasedDeployment

## SYNOPSIS

Use this cmdlet to get a phased deployment for an application.

## SYNTAX

### SearchByApplication
```
Get-CMApplicationPhasedDeployment -Application <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByApplicationId
```
Get-CMApplicationPhasedDeployment -ApplicationId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByApplicationName
```
Get-CMApplicationPhasedDeployment -ApplicationName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMApplicationPhasedDeployment -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMApplicationPhasedDeployment -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to get a phased deployment for an application.

## EXAMPLES

### Example 1: Get phased deployment by name

This example gets the object by the name of the phased deployment.

```powershell
Get-CMApplicationPhasedDeployment -Name "myPhasedDeploymentName"
```

### Example 2: Get phased deployment by app name

This example gets the object by the name of the application.

```powershell
Get-CMApplicationPhasedDeployment -ApplicationName "myApplicationName"
```

## PARAMETERS

### -Application

Specify an object for the application.

```yaml
Type: IResultObject
Parameter Sets: SearchByApplication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ApplicationId

Specify the application ID.

```yaml
Type: String
Parameter Sets: SearchByApplicationId
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName

Specify the application name.

```yaml
Type: String
Parameter Sets: SearchByApplicationName
Aliases: ApplicationLocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

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

Specify the ID of the phased deployment.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: PhasedDeploymentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the phased deployment.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: True
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

### IResultObject#SMS_PhasedDeployment

### IResultObject[]#SMS_PhasedDeployment

## NOTES

## RELATED LINKS
