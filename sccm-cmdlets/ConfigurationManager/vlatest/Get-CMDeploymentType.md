---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833591
schema: 2.0.0
ms.assetid: C79E32F6-CBDA-4F7D-A88C-B52EA286CF49
---

# Get-CMDeploymentType

## SYNOPSIS
Gets the deployment type of an application.

## SYNTAX

### SearchByName (Default)
```
Get-CMDeploymentType [-DeploymentTypeName <String>] -ApplicationName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDeploymentType -DeploymentTypeId <Int32> -ApplicationName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDTValue
```
Get-CMDeploymentType [-DeploymentTypeName <String>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeploymentType** cmdlet gets the deployment type of an application.
A deployment type is contained within an application and contains the information that Microsoft System Center Configuration Manager requires to install software.
A deployment type also contains rules that specify if and how the software is deployed.

## EXAMPLES

### Example 1: Get the deployment type of an application
```
PS C:\>Get-CMDeploymentType -ApplicationName "CenterApp"
```

This command gets the deployment type for the application named CenterApp.

### Example 2: Get the deployment type of an application by name
```
PS C:\>Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows app package (.appx file)"
```

This command gets the deployment type for the application named CenterApp that has a deployment type named InterDept - Windows app package (.appx file).

### Example 3: Get the deployment type of an application by ID
```
PS C:\>Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeID "16777457"
```

This command gets the deployment type for the application named CenterApp that has a deployment type that has the ID 16777457.

## PARAMETERS

### -ApplicationName
Specifies the name of an application that is associated with the deployment type.

```yaml
Type: String
Parameter Sets: SearchByName, SearchByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeId
Specifies the ID of a deployment type.

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

### -DeploymentTypeName
Specifies the name of a deployment type.

```yaml
Type: String
Parameter Sets: SearchByName, SearchByDTValue
Aliases: LocalizedDisplayName
Required: False
Position: Named
Default value: None
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


```yaml
Type: IResultObject
Parameter Sets: SearchByDTValue
Aliases: Application
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMDeploymentType](./Add-CMDeploymentType.md)

[Get-CMDeployment](./Get-CMDeployment.md)

[Get-CMDeploymentPackage](./Get-CMDeploymentPackage.md)

[Get-CMDeploymentStatus](./Get-CMDeploymentStatus.md)

[Remove-CMDeploymentType](./Remove-CMDeploymentType.md)

[Set-CMDeploymentType](./Set-CMDeploymentType.md)


