---
title: Пример использования методов GetObjectOwner и SetObjectOwner (VB)
TOCTitle: GetObjectOwner and SetObjectOwner methods example (VB)
ms:assetid: 0a30cce1-7626-8db3-4af4-84098c284db0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248833(v=office.15)
ms:contentKeyID: 48543146
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daecca6a8d2997fefdca4736cc8325733a2b9188
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292302"
---
# <a name="getobjectowner-and-setobjectowner-methods-example-vb"></a><span data-ttu-id="1d002-102">Пример использования методов GetObjectOwner и SetObjectOwner (VB)</span><span class="sxs-lookup"><span data-stu-id="1d002-102">GetObjectOwner and SetObjectOwner methods example (VB)</span></span>


<span data-ttu-id="1d002-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d002-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d002-104">В этом примере демонстрируются методы [GetObjectOwner](getobjectowner-method-adox.md) и [SetObjectOwner.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox)</span><span class="sxs-lookup"><span data-stu-id="1d002-104">This example demonstrates the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) methods.</span></span> <span data-ttu-id="1d002-105">В этом коде предполагается, что существует группа Accounting (см. пример с методами Groups [и Users Append и ChangePassword (VB),](groups-and-users-append-changepassword-methods-example-vb.md) чтобы узнать, как добавить эту группу в систему.</span><span class="sxs-lookup"><span data-stu-id="1d002-105">This code assumes the existence of the group Accounting (see the [Groups and Users Append, ChangePassword methods example (VB)](groups-and-users-append-changepassword-methods-example-vb.md) to see how to add this group to the system).</span></span> <span data-ttu-id="1d002-106">Для владельца таблицы "Категории" установлено "Бухгалтерия".</span><span class="sxs-lookup"><span data-stu-id="1d002-106">The owner of the Categories table is set to Accounting.</span></span>

```vb 
 
' BeginOwnersVB 
Sub Main() 
 On Error GoTo OwnersXError 
 
 Dim tblLoop As New ADOX.Table 
 Dim cat As New ADOX.Catalog 
 Dim strOwner As String 
 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" & _ 
 "jet oledb:system database=" & _ 
 "'c:\Program Files\Microsoft Office\Office\system.mdw'" 
 
 ' Print the original owner of Categories 
 strOwner = cat.GetObjectOwner("Categories", adPermObjTable) 
 Debug.Print "Owner of Categories: " & strOwner 
 
 ' Set the owner of Categories to Accounting 
 cat.SetObjectOwner "Categories", adPermObjTable, "Accounting" 
 
 ' List the owners of all tables and columns in the catalog. 
 For Each tblLoop In cat.Tables 
 Debug.Print "Table: " & tblLoop.Name 
 Debug.Print " Owner: " & _ 
 cat.GetObjectOwner(tblLoop.Name, adPermObjTable) 
 Next tblLoop 
 
 ' Restore the original owner of Categories 
 cat.SetObjectOwner "Categories", adPermObjTable, strOwner 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
OwnersXError: 
 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndOwnersVB 
```

