---
title: 'Пример: свойства RelatedColumn метод, тип ключа (VB) добавьте ключи'
TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)
ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15)
ms:contentKeyID: 48547871
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a81c457187d53abac6aedbf382605a349c3c812
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481616"
---
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a>Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)


**Применимо к**: Access 2013 | Office 2013

Следующий код демонстрирует создание нового внешнего ключа. Предполагается, что существуют две таблицы (**клиентов** и **Заказы**).

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
