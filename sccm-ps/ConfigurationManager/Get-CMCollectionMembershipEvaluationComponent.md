---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Get-CMCollectionMembershipEvaluationComponent
---

# Get-CMCollectionMembershipEvaluationComponent

## SYNOPSIS

Get the site component that evaluates collection membership.

## SYNTAX

```
Get-CMCollectionMembershipEvaluationComponent [-SiteCode <String>] [-SiteSystemServerName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the site component that evaluates collection membership. This component controls how often collection membership is incrementally evaluated. Incremental evaluation updates a collection membership with only new or changed resources.

For more information, see [Site components for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-components#bkmk_colleval).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an evaluation period for the site

This example first gets the **XYZ** site component for collection membership evaluation and stores the object in the **$component** variable.
The next command looks at the **Props** property on the component object (`$component`), looks for the embedded property for the **Incremental Interval**, and displays the **Value**. By default, this value is 5 minutes.

```powershell
$component = Get-CMCollectionMembershipEvaluationComponent -SiteCode "XYZ"

$component.Props | Where-Object { $_.PropertyName -eq "Incremental Interval" } | Select-Object Value
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

### -SiteCode

Specify the three-character site code to query for this component.

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

### -SiteSystemServerName

This parameter is deprecated, don't use it.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### IResultObject[]#SMS_SCI_Component
### IResultObject#SMS_SCI_Component

## NOTES

For more information on this return object and its properties, see [SMS_SCI_Component server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_component-server-wmi-class).

## RELATED LINKS

[Set-CMCollectionMembershipEvaluationComponent](Set-CMCollectionMembershipEvaluationComponent.md)

[Get-CMSiteComponent](Get-CMSiteComponent.md)

[Site components for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-components#bkmk_colleval)
[Collection evaluation in Configuration Manager](/mem/configmgr/core/clients/manage/collections/collection-evaluation)
