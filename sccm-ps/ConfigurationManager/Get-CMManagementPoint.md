---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 72166BF0-B4CD-4571-92FC-D42CF98BC1AE
online version: https://go.microsoft.com/fwlink/?linkid=833741
schema: 2.0.0
---

# Get-CMManagementPoint

## SYNOPSIS
Gets a management point.

## SYNTAX

### SearchByName (Default)
```
Get-CMManagementPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-AllSite]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMManagementPoint [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMManagementPoint** cmdlet gets a management point.
A management point is a site system role that provides policy and service location information to clients and receives configuration data from clients.

## EXAMPLES

### Example 1: Get a management point
```
PS C:\> Get-CMManagementPoint -SiteSystemServerName "cmcen-dist02.tsqa.contoso.com" -SiteCode "CM1" >>\CMmgmt01\Get-CMManagementPoint_data.txt
```

This command gets a management point that is associated with the site system named cmcen-dist02.tsqa.contoso.com and the site code CM1.
The command directs the output to the file Get-CMOutOfBandServicePoint_data.txt.

## PARAMETERS

### -AllSite
 

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AllSites

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName

Required: False
Position: 0
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

[Add-CMManagementPoint](Add-CMManagementPoint.md)

[Remove-CMManagementPoint](Remove-CMManagementPoint.md)

[Get-CMManagementPointComponent](Get-CMManagementPointComponent.md)


