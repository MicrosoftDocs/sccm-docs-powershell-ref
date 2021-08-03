---
description: Get the details of a SEDO lock for an object.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/05/2021
schema: 2.0.0
title: Get-CMObjectLockDetails
---

# Get-CMObjectLockDetails

## SYNOPSIS

Get the details of a SEDO lock for an object.

## SYNTAX

```
Get-CMObjectLockDetails [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the SEDO lock details for an object. Configuration Manager SEDO (Serialized Editing of Distributed Objects) is a mechanism to assign locks to globally replicated objects. If a user wants to edit and save an object, they have to get a lock from the site. The site assigns a lock to the user for that object, on their computer, and in the site. While the user has the lock, no one else can edit the object.

For more information, see [Configuration Manager SEDO](/mem/configmgr/develop/core/understand/sedo).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get object lock details for an application

This example shows the output for the lock details of an application.

```powershell
PS XYZ:\> Get-CMApplication -Name "Central app" | Get-CMObjectLockDetails


SmsProviderObjectPath     : __PARAMETERS
AssignedMachine           : DESKTOP-VKJQV9N
AssignedObjectLockContext : 36b0ab13-ebe3-4977-8aab-19a701b1c1b6
AssignedSiteCode          : XYZ
AssignedTimeUTC           : 1/5/2021 08:08:39
AssignedUser              : CONTOSO\jqpublic
LockState                 : 1
ReturnValue               : 0
```

When there's no lock on the object, the output is similar but many of the properties are blank. The values aren't `$null`, but an empty string `""`.

### Example 2: Check for a lock before editing an object

This example first uses the **Get-CMApplication** cmdlet to get an app object. It then uses the **Get-CMObjectLockDetails** cmdlet for that app, and assigns the **AssignedUser** property to the variable **lockUser**. If that value is blank, then it uses the **Set-CMApplication** cmdlet to change the name of the app. If the **lockUser** variable isn't blank, it writes a warning.

```powershell
$app617 = Get-CMApplication -ApplicationName "LOB app v6.17"
$lockUser = ($app617 | Get-CMObjectLockDetails).AssignedUser

if ( $lockUser -eq "" ) {
  Set-CMApplication -InputObject $app617 -NewName "Central app v6.17"
} else {
  Write-Warning "There's a SEDO lock on app $($app617.LocalizedDisplayName)"
}
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

### -InputObject

Specify a Configuration Manager object that's output from another cmdlet. For example, to get an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

For a list of objects that are SEDO-enabled, see [Configuration Manager SEDO](/mem/configmgr/develop/core/understand/sedo).

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

[Lock-CMObject](Lock-CMObject.md)

[Unlock-CMObject](Unlock-CMObject.md)

[Configuration Manager SEDO](/mem/configmgr/develop/core/understand/sedo)
