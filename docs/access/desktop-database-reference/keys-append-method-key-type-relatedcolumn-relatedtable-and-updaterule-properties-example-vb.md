---
title: Метод Append с ключами, тип ключа, свойства RelatedColumn пример (VB)
TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)
ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15)
ms:contentKeyID: 48547871
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9120fa718544a0d1d7a132b197517aac955f5fc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290633"
---
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a><span data-ttu-id="7753c-102">Пример: метод Append, тип ключа, свойство RelatedColumn, RelatedTable и UpdateRule (VB)</span><span class="sxs-lookup"><span data-stu-id="7753c-102">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)</span></span>


<span data-ttu-id="7753c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7753c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7753c-104">В приведенном ниже коде показано, как создать новый внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="7753c-104">The following code demonstrates how to create a new foreign key.</span></span> <span data-ttu-id="7753c-105">Предполагается, что существуют\*\*\*\* две таблицы (Customers и **Orders**).</span><span class="sxs-lookup"><span data-stu-id="7753c-105">It assumes two tables (**Customers** and **Orders**) exist.</span></span>

```vb 
 
' BeginCreateKeyVB 
Sub Main() 
 On Error GoTo CreateKeyError 
 
 Dim kyForeign As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Define the foreign key 
 kyForeign.Name = "CustOrder" 
 kyForeign.Type = adKeyForeign 
 kyForeign.RelatedTable = "Customers" 
 kyForeign.Columns.Append "CustomerId" 
 kyForeign.Columns("CustomerId").RelatedColumn = "CustomerId" 
 kyForeign.UpdateRule = adRICascade 
 
 ' Append the foreign key 
 cat.Tables("Orders").Keys.Append kyForeign 
 
 'Delete the Key as this is a demonstration 
 cat.Tables("Orders").Keys.Delete kyForeign.Name 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 Exit Sub 
 
CreateKeyError: 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateKeyVB 
```

