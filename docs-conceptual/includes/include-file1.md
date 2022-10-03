---
ms.author: banreetkaur
author: Banreet
ms.prod: configuration-manager
ms.topic: include
ms.date: 10/27/2020
---
<!--include file for testing-->

## <a name="bkmk_pod-psh"></a> New cmdlets for phased deployments

Configuration Manager now supports cmdlets for phased deployments. You can configure your phased deployment scenarios using the following new cmdlets:
<!--6104290-->
- [New-CMSoftwareUpdatePhase](#new-cmsoftwareupdatephase)

### New-CMSoftwareUpdatePhase

Use this cmdlet to create a deployment phase for software update.

``` PowerShell
New-CMSoftwareUpdatePhase `
 -CollectionName "MyCollection" `
 -PhaseName "MySUPhase"`
 -UserNotificationOption DisplaySoftwareCenterOnly
```

- [Configuration Manager technical preview](configmgr/core/get-started/technical-preview)
- [Configuration Manager PowerShell](../overview.md)
