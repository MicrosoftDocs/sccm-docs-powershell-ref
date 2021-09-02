---
description: Changes the properties of an alert subscription.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMAlertSubscription
---

# Set-CMAlertSubscription

## SYNOPSIS
Changes the properties of an alert subscription.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMAlertSubscription [-AddEmailAddress <String[]>] [-AlertId <Int32[]>] [-EmailAddress <String[]>]
 -InputObject <IResultObject> [-LocaleId <Int32>] [-NewName <String>] [-PassThru]
 [-RemoveEmailAddress <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMAlertSubscription [-AddEmailAddress <String[]>] [-AlertId <Int32[]>] [-EmailAddress <String[]>]
 -Id <String> [-LocaleId <Int32>] [-NewName <String>] [-PassThru] [-RemoveEmailAddress <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMAlertSubscription [-AddEmailAddress <String[]>] [-AlertId <Int32[]>] [-EmailAddress <String[]>]
 [-LocaleId <Int32>] -Name <String> [-NewName <String>] [-PassThru] [-RemoveEmailAddress <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAlertSubscription** cmdlet changes the properties of an alert subscription object in Configuration Manager.
You can change the name of an alert subscription, the email address of the recipient of an alert notification, the Windows locale ID, and the alert ID.
You can also change the security scope membership of an alert subscription by adding it to or removing it from a specified security scope.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the properties of an alert subscription by subscription ID
```
PS XYZ:\> Set-CMAlertSubscription -Id "16777217" -NewName "Subscription02" -EmailAddress "evan.narvaez@contoso.com" -LocaleId 2057 -AlertIds 16777240
```

This command changes the name, email address, Windows locale ID, and alert ID of an alert subscription that has the ID 16777217.

### Example 2: Change the properties of an alert subscription by subscription name
```
PS XYZ:\> Set-CMAlertSubscription -Name "Subscription01" -NewName "Subscription02" -EmailAddress "elisa.daugherty@contoso.com" -LocaleId 2057 -AlertIds 16777240
```

This command changes the name, email address, Windows locale ID, and alert ID of an alert subscription named Subscription01.

### Example 3: Change the properties of an alert subscription by using the output from another cmdlet as input
```
PS XYZ:\> $SubObj = Get-CMAlertSubscription -Id "16777310"
PS XYZ:\> Set-CMAlertSubscription -AlertSubscription $SubObj -NewName "Subscription02" -EmailAddress "patti.fuller@contoso.com" -LocaleId 3081 -AlertIds 16777240
```

The first command gets an alert subscription object that has the ID 16777310, and then stores the object in the $SubObj variable.

The second command changes the properties of the alert subscription object, which include the subscription name, email recipient, locale ID, and alert ID, for the alert notification stored in the $SubObj variable.

### Example 4: Add an alert subscription to a security scope
```
PS XYZ:\> Set-CMAlertSubscription -SecurityScopeAction AddMembership -SecurityScopeName "Test" -Name "Subscription01"
```

This command adds the alert subscription named Subscription01 to the security scope named Test.

### Example 5: Remove an alert subscription from a security scope
```
PS XYZ:\> Set-CMAlertSubscription -SecurityScopeAction RemoveMembership -SecurityScopeName "Test" -Name "Subscription01"
```

This command removes the alert subscription named Subscription01 from the security scope named Test.

## PARAMETERS

### -AddEmailAddress
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddEmailAddresses

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AlertId
Specifies an array of alert IDs for subscriptions.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: AlertIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -EmailAddress
Specifies an email address where you want to send an alert notification.
You can separate multiple email addresses by using a semicolon.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: EmailAddresses

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

### -Id
Specifies the identifier for a subscription object.

```yaml
Type: String
Parameter Sets: SetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an alert notification object in Configuration Manager.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LocaleId
Specifies a locale for alert messages.
For more information and a list of locale identifiers, see [Appendix A: Product Behavior](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

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

### -Name
Specifies the name of an alert subscription object.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for an alert subscription object.

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

### -RemoveEmailAddress
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveEmailAddresses

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMAlertSubscription](New-CMAlertSubscription.md)

[Get-CMAlertSubscription](Get-CMAlertSubscription.md)

[Remove-CMAlertSubscription](Remove-CMAlertSubscription.md)

[Set-CMSecurityScope](Set-CMSecurityScope.md)
