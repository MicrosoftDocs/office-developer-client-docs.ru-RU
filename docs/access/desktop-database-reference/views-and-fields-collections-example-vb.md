---
title: Пример представления и коллекции полей (VB)
TOCTitle: Views and Fields Collections example (VB)
ms:assetid: 7c166bea-d6a3-0a9d-5220-af72996a76fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249518(v=office.15)
ms:contentKeyID: 48545828
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13b81a2bc6b40ae8ad8904b53095164749e49847
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944790"
---
# <a name="views-and-fields-collections-example-vb"></a>Пример коллекций Views и Fields (VB)


**Применимо к**: Access 2013, Office 2013

Следующий код демонстрирует использование свойства [команды](command-property-adox.md) и объекта [набора записей](recordset-object-ado.md) для получения сведений поля для представления.

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

