---
title: Пример коллекции представлений и полей (VB)
TOCTitle: Views and Fields Collections example (VB)
ms:assetid: 7c166bea-d6a3-0a9d-5220-af72996a76fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249518(v=office.15)
ms:contentKeyID: 48545828
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 619795b0911462ec46800a29080a50c9ea889c5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306000"
---
# <a name="views-and-fields-collections-example-vb"></a><span data-ttu-id="64794-102">Пример коллекций Views и Fields (VB)</span><span class="sxs-lookup"><span data-stu-id="64794-102">Views and Fields collections example (VB)</span></span>


<span data-ttu-id="64794-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64794-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64794-104">В следующем коде показано, как использовать свойство [Command](command-property-adox.md) и объект [Recordset](recordset-object-ado.md) для получения сведений о поле для представления.</span><span class="sxs-lookup"><span data-stu-id="64794-104">The following code demonstrates how to use the [Command](command-property-adox.md) property and the [Recordset](recordset-object-ado.md) object to retrieve field information for the view.</span></span>

```vb 
 
' BeginViewFieldsVB 
Sub ViewFields() 
 On Error GoTo ViewFieldsError 
 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim fld As ADODB.Field 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Set the Source for the Recordset 
 Set rst.Source = cat.Views("AllCustomers").Command 
 
 ' Retrieve Field information 
 rst.Fields.Refresh 
 For Each fld In rst.Fields 
 Debug.Print fld.Name & ":" & fld.Type 
 Next 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set rst = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ViewFieldsError: 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 
 Set cat = Nothing 
 Set rst = Nothing 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndViewFieldsVB 
```

