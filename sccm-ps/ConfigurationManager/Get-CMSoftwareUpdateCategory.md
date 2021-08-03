---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/29/2021
schema: 2.0.0
title: Get-CMSoftwareUpdateCategory
---

# Get-CMSoftwareUpdateCategory

## SYNOPSIS

Get a software update classification or product.

## SYNTAX

### ByName (Default)
```
Get-CMSoftwareUpdateCategory [-Fast] [-Name <String>] [-TypeName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMSoftwareUpdateCategory [-Fast] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByUniqueId
```
Get-CMSoftwareUpdateCategory [-Fast] -UniqueId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get an object for a software update classification or product. Software updates metadata is retrieved during the synchronization process in Configuration Manager based on the settings that you specify in the software update point component properties. For more information, see [Configure classifications and products to synchronize](/mem/configmgr/sum/get-started/configure-classifications-and-products).

To filter the results that this cmdlet returns, use the **CategoryTypeName** and **IsSubscribed** properties. The category types include **UpdateClassification**, **Company**, **ProductFamily**, and **Product**. When the **IsSubscribed** property is **True**, the site is configured to synchronize that category.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Show subscribed classifications

This example queries the site for all software update classifications that it's synchronizing.

```powershell
Get-CMSoftwareUpdateCategory -Fast -TypeName "UpdateClassification" | Where-Object { $_.IsSubscribed } | Select-Object LocalizedCategoryInstanceName
```

To change this command to return the list of classifications that the site isn't synchronizing, add the **not** operator (`!`) before the reference to the **IsSubscribed** property. For example, `!$_.IsSubscribed`

### Example 2: Count categories by type

This example counts how many categories the site has for each type. This count can help you determine if the software update point is out of sync with the upstream source.

```powershell
Get-CMSoftwareUpdateCategory -Fast | Group-Object -Property CategoryTypeName
```

```output
Count Name
----- ----
   13 UpdateClassification
    7 Company
   59 ProductFamily
  338 Product
```

### Example 3: Show products for Office product family

This example first gets the product family category for **Office**, and then uses its instance ID to get all child categories.

```powershell
$officeFamily = Get-CMSoftwareUpdateCategory -Fast -TypeName "ProductFamily" | Where-Object { $_.LocalizedCategoryInstanceName -eq "Office" }

Get-CMSoftwareUpdateCategory -Fast | Where-Object ParentCategoryInstanceId -eq $officeFamily.CategoryInstanceID | Select-Object LocalizedCategoryInstanceName,CategoryTypeName
```

```output
LocalizedCategoryInstanceName         CategoryTypeName
-----------------------------         ----------------
Dictionary Updates for Microsoft IMEs Product
New Dictionaries for Microsoft IMEs   Product
Office 2002/XP                        Product
Office 2003                           Product
Office 2007                           Product
Office 2010                           Product
Office 2013                           Product
Office 2016                           Product
Office 365 Client                     Product
Office 2019                           Product
```

### Example 4: Get all software updates in Office 365 Client category

This example first gets the product category for **Office 365 Client**, and then gets all software updates in that category.

```powershell
$cat = Get-CMSoftwareUpdateCategory -Fast -TypeName "Product" | Where-Object { $_.LocalizedCategoryInstanceName -eq "Office 365 Client" }

Get-CMSoftwareUpdate -Fast -Category $cat | Select-Object ArticleID,LocalizedDisplayName,IsDeployed,IsSuperseded,NumTotal,NumMissing
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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

### -Id

Specify the ID of the category to get.

```yaml
Type: String
Parameter Sets: ById
Aliases: CategoryInstanceID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the category to get.

```yaml
Type: String
Parameter Sets: ByName
Aliases: LocalizedCategoryInstanceName, CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -TypeName

Specify the type of category to get. Common values include the following types:

- UpdateClassification
- Company
- ProductFamily
- Product

```yaml
Type: String
Parameter Sets: ByName
Aliases: CategoryTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -UniqueId

Specify the unique ID for the category to get. This value is the type name with a GUID for the category. For example, `UpdateClassification:77835c8d-62a7-41f5-82ad-f28d1af1e3b1`

```yaml
Type: String
Parameter Sets: ByUniqueId
Aliases: CategoryInstance_UniqueID

Required: True
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

### IResultObject[]#SMS_UpdateCategoryInstance
### IResultObject#SMS_UpdateCategoryInstance
## NOTES

For more information on this return object and its properties, see [SMS_UpdateCategoryInstance server WMI class](/mem/configmgr/develop/reference/sum/sms_updatecategoryinstance-server-wmi-class).

## RELATED LINKS

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)
