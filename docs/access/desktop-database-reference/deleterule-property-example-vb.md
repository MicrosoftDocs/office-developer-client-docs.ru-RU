---
title: Пример использования свойства DeleteRule (VB)
TOCTitle: DeleteRule property example (VB)
ms:assetid: 354e00b6-cecb-1132-6923-fc9e8853fa0e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249114(v=office.15)
ms:contentKeyID: 48544142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02e0ab742a49408c3bd68b9e48d1ce52aeed82cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293975"
---
# <a name="deleterule-property-example-vb"></a><span data-ttu-id="08b4a-102">Пример использования свойства DeleteRule (VB)</span><span class="sxs-lookup"><span data-stu-id="08b4a-102">DeleteRule property example (VB)</span></span>


<span data-ttu-id="08b4a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08b4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08b4a-104">В этом примере показано [свойство DeleteRule](deleterule-property-adox.md) объекта [Key.](key-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="08b4a-104">This example demonstrates the [DeleteRule](deleterule-property-adox.md) property of a [Key](key-object-adox.md) object.</span></span> <span data-ttu-id="08b4a-105">Код appends a new [Table](table-object-adox.md) and then defines a new primary key, setting **DeleteRule** to **adRICascade**.</span><span class="sxs-lookup"><span data-stu-id="08b4a-105">The code appends a new [Table](table-object-adox.md) and then defines a new primary key, setting **DeleteRule** to **adRICascade**.</span></span>

```vb 
 
' BeginDeleteRuleVB 
Sub Main() 
 On Error GoTo DeleteRuleXError 
 
 Dim kyPrimary As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "data source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append the new table 
 cat.Tables.Append tblNew 
 
 ' Define the Primary key 
 kyPrimary.Name = "NumField" 
 kyPrimary.Type = adKeyPrimary 
 kyPrimary.RelatedTable = "Customers" 
 kyPrimary.Columns.Append "NumField" 
 kyPrimary.Columns("NumField").RelatedColumn = "CustomerId" 
 kyPrimary.DeleteRule = adRICascade 
 
 ' Append the primary key 
 cat.Tables("NewTable").Keys.Append kyPrimary 
 Debug.Print "The primary key is appended." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tblNew.Name 
 Debug.Print "The primary key is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 Exit Sub 
 
DeleteRuleXError: 
 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndDeleteRuleVB 
```

