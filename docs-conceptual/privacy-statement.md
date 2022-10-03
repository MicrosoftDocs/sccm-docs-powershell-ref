---
title: Privacy statement for cmdlets
titleSuffix: Configuration Manager
description: Learn about how Microsoft collects and uses data related to the Configuration Manager cmdlets
ms.date: 07/14/2020
ms.prod: configuration-manager
ms.technology: configmgr-sdk
ms.topic: conceptual
ms.localizationpriority: low
ms.author: banreetkaur
author: Banreet
manager: apoorvseth
--- 

# Configuration Manager cmdlet library privacy statement

This privacy statement covers the features for the Configuration Manager PowerShell cmdlet library.

## Usage data

The Configuration Manager PowerShell cmdlet library lets you manage a Configuration Manager hierarchy by using Windows PowerShell cmdlets and scripts. The cmdlet library collects information about how you use the cmdlets in the library to identify trends and usage patterns. The cmdlet library also collects the types and numbers of errors that you receive when you use the cmdlets.

## Information collected, processed, or transmitted

The collected usage data includes starting, stopping, and terminating of cmdlets, running of deprecated cmdlets, and activity metrics for SMS Provider operations that are related to the cmdlets. This information isn't personally identifiable. Collected error information includes errors that cmdlets return and error details for exception errors. Some error detail reports might inadvertently include individual identifiers, like a serial number for a device that is connected to your computer. The cmdlet library filters and anonymizes information that's in the error reports to remove individual identifiers before transmission to Microsoft.

## Use of information

Microsoft uses this information to improve the quality, security, and integrity of the products and services they offer.

## Choice and control

The Configuration Manager cmdlet library enables this usage data feature by default. There are two registry keys that control this functionality.

To fully opt out, set the `CeipLevel` entry to `0` in the following two registry keys. They're for each of the Event Tracing for Windows (ETW) providers:

- `HKLM\Software\Microsoft\ConfigMgr10\PowerShell\Microsoft.ConfigurationManagement.PowerShell.Provider`: opts out of usage data for the drive provider

- `HKLM\Software\Microsoft\ConfigMgr10\PowerShell\Microsoft.ConfigurationManagement.PowerShell.Cmdlets`: opts out of usage data for the cmdlets

Changes to the usage data settings are specific to the local computer.
