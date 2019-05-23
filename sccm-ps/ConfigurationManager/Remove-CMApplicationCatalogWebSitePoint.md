---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 5FFC0EF0-B499-4511-B2B0-FF6D69D84E6F
online version: https://go.microsoft.com/fwlink/?linkid=833899
schema: 2.0.0
---

# Remove-CMApplicationCatalogWebsitePoint

## SYNOPSIS
Removes a Configuration Manager Application Catalog website point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMApplicationCatalogWebsitePoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMApplicationCatalogWebsitePoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMApplicationCatalogWebSitePoint** cmdlet removes an Application Catalog website point in Microsoft System Center Configuration Manager.
This site system role supports the Application Catalog website and the Software Library.

You can specify a website point to remove by site code and name of the server that hosts the role, or you can use the Get-CMApplicationCatalogWebsitePoint cmdlet to get a website point to remove.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove an Application Catalog website point
```
PS XYZ:\> Remove-CMApplicationCatalogWebsitePoint -SiteCode "CM2" -SiteSystemServerName "WesternACWP.Contoso.com"
```

This command removes an Application Catalog website point that belongs to the site that has the site code CM2.
The computer named WesternACWP.Contoso.com hosts the point that the cmdlet removes.

### Example 2: Remove an Application Catalog website point by variable
```
PS XYZ:\> $CMACWP= Get-CMApplicationCatalogWebsitePoint -SiteCode "CM2" -SiteSystemServerName"WesternACWP.Contoso.com" 
PS XYZ:\> Remove-CMApplicationCatalogWebsitePoint -InputObject $CMACWP -Force
```

The first command uses the **Get-CMApplicationCatalogWebsitePoint** cmdlet to get an Application Catalog website point hosted by the computer named WesternACWP.Contoso.com in the site that has the site code CM2, and stores it in the $CMACWP variable.

The second command removes the Application Catalog website point stores in the $CMACWP variable.
The command includes the *Force* parameter.
Therefore, the command does not prompt you for confirmation.

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
Specifies an Application Catalog website point object.
To get an Application Catalog website point object, use the Get-CMApplicationCatalogWebsitePoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ApplicationCatalogWebSitePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server that hosts a site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName

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

[Add-CMApplicationCatalogWebsitePoint](Add-CMApplicationCatalogWebsitePoint.md)

[Get-CMApplicationCatalogWebsitePoint](Get-CMApplicationCatalogWebsitePoint.md)

[Set-CMApplicationCatalogWebsitePoint](Set-CMApplicationCatalogWebsitePoint.md)


