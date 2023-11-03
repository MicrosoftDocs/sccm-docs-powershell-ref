---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/18/2023
online version:
schema: 2.0.0
---

# Set-UpdateServerApplication

## SYNOPSIS

Use the console to update the server app or use this cmdlet to add the missing URL http://localhost to your existing server app.

## DESCRIPTION

This cmdlet is for existing customer who is using pre-existing old Server App and it has missing URL http://localhost. These customers have to add this URL to their Server App in both database (Table:AAD_Application_Ex) and in Microsoft Entra ID in Azure portal where Server Apps reside. Customers can use console to update the server app or this cmdlet.

## EXAMPLES

### Example 1

```powershell
SET-UpdateServerApplication -TenantId 1E7C0B63-1DAB-4754-8433-AF8F9CFFCF38
```

## PARAMETERS

### -TenantId

It's a mandatory parameter that user has to provide.

```yaml
Type: String
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## NOTES

## RELATED LINKS

[About upgrading windows version in Configuration Manager](/mem/configmgr/compliance/deploy-use/upgrade-windows-version)
