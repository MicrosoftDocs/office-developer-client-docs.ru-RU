---
title: Procedures Delete Method Example (VB)
TOCTitle: Procedures Delete Method Example (VB)
ms:assetid: 1cbae0a2-0035-d03f-b9c6-5453ddd51ec4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248964(v=office.15)
ms:contentKeyID: 48543576
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1933efe1beafff3211632a11348af6779715372
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480290"
---
# <a name="procedures-delete-method-example-vb"></a><span data-ttu-id="891d4-102">Procedures Delete Method Example (VB)</span><span class="sxs-lookup"><span data-stu-id="891d4-102">Procedures Delete Method Example (VB)</span></span>


<span data-ttu-id="891d4-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="891d4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="891d4-104">Приведенный ниже код показано, как удалить процедуры с помощью [процедуры](procedures-collection-adox.md) коллекции метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="891d4-104">The following code demonstrates how to delete a procedure using the [Procedures](procedures-collection-adox.md) collection [Delete](delete-method-adox-collections.md) method.</span></span>

```vb 
 
' BeginDeleteProcedureVB 
Sub Main() 
 On Error GoTo DeleteProcedureError 
 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog. 
 cat.ActiveConnection = _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Delete the Procedure. 
 cat.Procedures.Delete "CustomerById" 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
DeleteProcedureError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndDeleteProcedureVB 
```

