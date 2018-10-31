---
title: Пример использования метода Refresh для коллекции Views (VB)
TOCTitle: Views Refresh method example (VB)
ms:assetid: 607b78d6-1b26-d643-9f97-f47b5f5cffc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249352(v=office.15)
ms:contentKeyID: 48545182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 953e12d808c5023e7f0c3d20d46be47ab44ad901
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863418"
---
# <a name="views-refresh-method-example-vb"></a><span data-ttu-id="94fc9-102">Пример использования метода Refresh для коллекции Views (VB)</span><span class="sxs-lookup"><span data-stu-id="94fc9-102">Views Refresh method example (VB)</span></span>


<span data-ttu-id="94fc9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="94fc9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="94fc9-104">Приведенный ниже код показано, как обновить коллекцию [представлений](views-collection-adox.md) [каталога](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="94fc9-104">The following code shows how to refresh the [Views](views-collection-adox.md) collection of a [Catalog](catalog-object-adox.md).</span></span> <span data-ttu-id="94fc9-105">Это необходимо, чтобы получить доступ к объектам [представления](view-object-adox.md) из **каталога** .</span><span class="sxs-lookup"><span data-stu-id="94fc9-105">This is required before [View](view-object-adox.md) objects from the **Catalog** can be accessed.</span></span>

```vb 
 
' BeginViewsRefreshVB 
Sub Main() 
 On Error GoTo ProcedureViewsRefreshError 
 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Refresh the Procedures collection 
 cat.Views.Refresh 
 
 'Clean up 
 Set cat = Nothing 
 Exit Sub 
 
ProcedureViewsRefreshError: 
 
 If Not cat Is Nothing Then 
 Set cat = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndViewsRefreshVB 
```

