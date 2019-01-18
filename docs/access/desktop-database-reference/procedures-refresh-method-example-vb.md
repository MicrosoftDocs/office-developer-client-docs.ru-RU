---
title: Пример использования метода Refresh для коллекции Procedures (VB)
TOCTitle: Procedures Refresh method example (VB)
ms:assetid: fd6d71cf-7a6b-49d7-220b-dd5b815a92ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250300(v=office.15)
ms:contentKeyID: 48548916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9d4e9aef26967cdfe052ef37959d5aceff2b29
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726241"
---
# <a name="procedures-refresh-method-example-vb"></a>Пример использования метода Refresh для коллекции Procedures (VB)


**Применимо к**: Access 2013, Office 2013

Приведенный ниже код показано, как обновить коллекцию [процедур](procedures-collection-adox.md) [каталога](catalog-object-adox.md). Это необходимо, чтобы получить доступ к объектам [процедуры](procedure-object-adox.md) из **каталога** .

```vb 
 
' BeginProceduresRefreshVB 
Sub Main() 
 On Error GoTo ProcedureRefreshError 
 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog 
 cat.ActiveConnection = _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Refresh the Procedures collection 
 cat.Procedures.Refresh 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
ProcedureRefreshError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndProceduresRefreshVB 
```

