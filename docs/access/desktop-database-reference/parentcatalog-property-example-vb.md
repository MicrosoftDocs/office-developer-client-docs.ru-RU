---
title: Пример использования свойства ParentCatalog (VB)
TOCTitle: ParentCatalog property example (VB)
ms:assetid: 3bd01153-40b5-1a45-67e2-eb8154c3fe33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249152(v=office.15)
ms:contentKeyID: 48544295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e76d40a02aa70bcf977a34f1db378e8d83e5d1e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867764"
---
# <a name="parentcatalog-property-example-vb"></a><span data-ttu-id="50e41-102">Пример использования свойства ParentCatalog (VB)</span><span class="sxs-lookup"><span data-stu-id="50e41-102">ParentCatalog property example (VB)</span></span>


<span data-ttu-id="50e41-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50e41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50e41-104">Следующий код демонстрирует использование свойства [ParentCatalog](parentcatalog-property-adox.md) для доступа к свойству от поставщика перед добавлением таблицы в каталоге.</span><span class="sxs-lookup"><span data-stu-id="50e41-104">The following code demonstrates how to use the [ParentCatalog](parentcatalog-property-adox.md) property to access a provider-specific property prior to appending a table to a catalog.</span></span> <span data-ttu-id="50e41-105">Является ли данное свойство AutoIncrement, которая создает поле AutoIncrement базы данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="50e41-105">The property is AutoIncrement, which creates an AutoIncrement field in a Microsoft Jet database.</span></span>

```vb 
 
' BeginCreateAutoIncrColumnVB 
Sub Main() 
 On Error GoTo CreateAutoIncrColumnError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tbl As New ADOX.Table 
 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 With tbl 
 .Name = "MyContacts" 
 Set .ParentCatalog = cat 
 ' Create fields and append them to the new Table object. 
 .Columns.Append "ContactId", adInteger 
 ' Make the ContactId column and auto incrementing column 
 .Columns("ContactId").Properties("AutoIncrement") = True 
 .Columns.Append "CustomerID", adVarWChar 
 .Columns.Append "FirstName", adVarWChar 
 .Columns.Append "LastName", adVarWChar 
 .Columns.Append "Phone", adVarWChar, 20 
 .Columns.Append "Notes", adLongVarWChar 
 End With 
 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyContacts' is added." 
 
 ' Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyContacts' is delete." 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
CreateAutoIncrColumnError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateAutoIncrColumnVB 
```

