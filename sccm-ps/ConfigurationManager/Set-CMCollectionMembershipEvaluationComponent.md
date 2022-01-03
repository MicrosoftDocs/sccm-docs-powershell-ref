---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Set-CMCollectionMembershipEvaluationComponent
---

# Set-CMCollectionMembershipEvaluationComponent

## SYNOPSIS

Configure the site component that evaluates collection membership.

## SYNTAX

```
Set-CMCollectionMembershipEvaluationComponent -EvaluationMins <Int32> [-PassThru] [-SiteCode <String>]
 [-SiteSystemServerName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the site component that evaluates collection membership. This component controls how often collection membership is incrementally evaluated. Incremental evaluation updates a collection membership with only new or changed resources.

For more information, see [Site components for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-components#bkmk_colleval).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set an evaluation interval

This command sets the collection membership incremental evaluation interval to `10` minutes for the **XYZ** site.

```powershell
Set-CMCollectionMembershipEvaluationComponent -EvaluationMins 10 -SiteCode "XYZ"
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

### -EvaluationMins

Specify an integer value for the number of minutes for the evaluation interval. By default, this value is 5 minutes.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinutesInterval

Required: True
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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

Specify the three-character site code to configure this component.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_SCI_Component

## NOTES

For more information on this return object and its properties, see [SMS_SCI_Component server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_component-server-wmi-class).

## RELATED LINKS

[Get-CMCollectionMembershipEvaluationComponent](Get-CMCollectionMembershipEvaluationComponent.md)

[Get-CMSiteComponent](Get-CMSiteComponent.md)

[Site components for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-components#bkmk_colleval)
[Collection evaluation in Configuration Manager](/mem/configmgr/core/clients/manage/collections/collection-evaluation)
