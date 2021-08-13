---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2021
online version:
schema: 2.0.0
---

# New-CMTSStepJoinDomainWorkgroup

## SYNOPSIS

Create an **Join Domain or Workgroup** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepJoinDomainWorkgroup [-DomainName <String>] [-OU <String>] [-UserName <String>]
 [-UserPassword <SecureString>] [-WorkgroupName <String>] [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Join Domain or Workgroup** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Join Domain or Workgroup](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_JoinDomainorWorkgroup).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **ConvertTo-SecureString** built-in cmdlet to create a secure string for the user password. This method is used here as a simple example, but not the most secure since the plain text password is in the script. For more information on this cmdlet and other options, see [ConvertTo-SecureString](/powershell/module/microsoft.powershell.security/convertto-securestring).

The next line creates an object for the **Join Domain or Workgroup** step, using the secure string password variable.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$Secure_String_Pwd = ConvertTo-SecureString "P@ssW0rD!" -AsPlainText -Force

$step = New-CMTSStepJoinDomainWorkgroup -Name "Join Domain or Workgroup" -DomainName "na.corp.contoso.com" -OU "LDAP://OU=Ops,OU=ITS,DC=na,DC=corp,DC=contoso,DC=com" -UserName "contoso\_cmosdjoin" -UserPassword $Secure_String_Pwd

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -Condition

Specify a condition object to use with this step. To get this object, use one of the task sequence condition cmdlets. For example, [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md).

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Conditions

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

### -ContinueOnError

Add this parameter to enable the step option **Continue on error**. When you enable this option, if the step fails, the task sequence continues.

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

### -Description

Specify an optional description for this task sequence step.

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

### -Disable

Add this parameter to disable this task sequence step.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableThisStep

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

### -DomainName

To configure this step to have the computer join a domain, use this parameter to specify the name of a domain to join. Then use the following other parameters:

- **DomainOU**: Optionally specify an organizational unit in which to create the new computer account.
- **UserName**: Specify the user account with permissions to join a computer to the domain.
- **UserPassword**: Specify the password for the user account.

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

### -Name

Specify a name for this step to identify it in the task sequence.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OU

When you use the **DomainName** parameter, you can also specify the path to an organizational unit (OU). When the computer joins the domain, if it creates a new computer account, that account will be in this OU.

For example, `LDAP://OU=MyOu,DC=MyDom,DC=MyCompany,DC=com`

```yaml
Type: String
Parameter Sets: (All)
Aliases: OrganizationalUnit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName

When you use the **DomainName** parameter, use this parameter to specify the domain user account that's used to add the destination computer to the domain. Use the **UserPassword** parameter to specify the account password.

For more information, see the [task sequence domain joining account](/mem/configmgr/core/plan-design/hierarchy/accounts#task-sequence-domain-join-account).

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

### -UserPassword

Specify the password as a secure string for the **UserName** parameter.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkgroupName

To configure this step to have the computer join a workgroup, use this parameter to specify the workgroup name.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_JoinDomainWorkgroupAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_JoinDomainWorkgroupAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_joindomainworkgroupaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepJoinDomainWorkgroup](Get-CMTSStepJoinDomainWorkgroup.md)
[Remove-CMTSStepJoinDomainWorkgroup](Remove-CMTSStepJoinDomainWorkgroup.md)
[Set-CMTSStepJoinDomainWorkgroup](Set-CMTSStepJoinDomainWorkgroup.md)

[About task sequence steps: Join Domain or Workgroup](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_JoinDomainorWorkgroup)
