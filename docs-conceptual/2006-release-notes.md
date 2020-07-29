---
title: Version 2006 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2006. 
ms.date: 07/31/2020
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Configuration Manager cmdlet library changes for version 2006

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2006.

> [!NOTE]  
> Configuration Manager current branch version 2002 is the baseline for these changes. For more information, see [Configuration Manager Cmdlet Library changes for version 2002](https://docs.microsoft.com/powershell/sccm/2002-release-notes).

## Important changes

### New cmdlets

#### New-CMSoftwareUpdatePhase <!-- example to remove -->

Use this cmdlet to create a deployment phase for software update.

``` PowerShell
New-CMSoftwareUpdatePhase `
 -CollectionName "MyCollection" `
 -PhaseName "MySUPhase"`
 -UserNotificationOption DisplaySoftwareCenterOnly
```

### Deprecated cmdlets

None

## Known issues

None

## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To submit bug reports, use [send a smile in the Configuration Manager console](https://docs.microsoft.com/sccm/core/understand/find-help#product-feedback). For new feature requests, use [UserVoice](https://configurationmanager.uservoice.com).
