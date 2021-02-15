---
title: Пример использования свойства ActiveConnection объекта Catalog (VB)
TOCTitle: Catalog ActiveConnection property example (VB)
ms:assetid: 12a34091-e451-dbd1-e7f3-f794b84ee5b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248901(v=office.15)
ms:contentKeyID: 48543348
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2e409a7d158ba04e79d300eaacf9edf8cf5622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296621"
---
# <a name="catalog-activeconnection-property-example-vb"></a><span data-ttu-id="6596d-102">Пример использования свойства ActiveConnection объекта Catalog (VB)</span><span class="sxs-lookup"><span data-stu-id="6596d-102">Catalog ActiveConnection property example (VB)</span></span>

<span data-ttu-id="6596d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6596d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6596d-104">Установка для [свойства ActiveConnection](activeconnection-property-adox.md) допустимого открытого подключения "открывает" каталог.</span><span class="sxs-lookup"><span data-stu-id="6596d-104">Setting the [ActiveConnection](activeconnection-property-adox.md) property to a valid, open connection "opens" the catalog.</span></span> <span data-ttu-id="6596d-105">Из открытого каталога можно получить доступ к объектам схемы, которые содержатся в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="6596d-105">From an open catalog, you can access the schema objects contained within that catalog.</span></span>

```vb 
 
    ' BeginOpenConnectionVB 
    Sub OpenConnection() 
    On Error GoTo OpenConnectionError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Debug.Print cat.Tables(0).Type 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    OpenConnectionError: 
    
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndOpenConnectionVB 
```

<span data-ttu-id="6596d-106">Установка для **свойства ActiveConnection** допустимой строки подключения также "открывает" каталог.</span><span class="sxs-lookup"><span data-stu-id="6596d-106">Setting the **ActiveConnection** property to a valid connection string also "opens" the catalog.</span></span>

```vb
    ' BeginOpenConnection2VB 
    Sub Main() 
     On Error GoTo OpenConnectionWithStringError 
     Dim cat As New ADOX.Catalog 
     
     cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source='c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Debug.Print cat.Tables(0).Type 
     
     'Clean up 
     Set cat.ActiveConnection = Nothing 
     Exit Sub 
     
    OpenConnectionWithStringError: 
     Set cat = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndOpenConnection2VB
```
