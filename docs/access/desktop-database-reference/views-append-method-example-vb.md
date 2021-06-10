---
title: Пример использования метода Append для коллекции Views (VB)
TOCTitle: Views Append method example (VB)
ms:assetid: 24536276-7da9-6ee8-2e27-39531b12b30f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249016(v=office.15)
ms:contentKeyID: 48543752
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3816e1699865b1e58c745e9fb466c37885833802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312049"
---
# <a name="views-append-method-example-vb"></a>Пример использования метода Append для коллекции Views (VB)


**Область применения**: Access 2013, Office 2013

В следующем коде показано, как использовать [](append-method-adox-views.md) объект [Command](command-object-ado.md) и метод приложения коллекции [Просмотры](views-collection-adox.md) для создания нового представления в основном источнике данных.

```vb 
 
' BeginCreateViewVB 
Sub Main() 
 On Error GoTo CreateViewError 
 
 Dim cmd As New ADODB.Command 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog 
 cat.ActiveConnection = _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Create the command representing the view. 
 cmd.CommandText = "Select * From Customers" 
 
 ' Create the new View 
 cat.Views.Append "AllCustomers", cmd 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set cmd = Nothing 
 Exit Sub 
 
CreateViewError: 
 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateViewVB 
```

