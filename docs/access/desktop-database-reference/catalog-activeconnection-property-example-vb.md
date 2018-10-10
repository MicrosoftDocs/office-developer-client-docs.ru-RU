---
title: Catalog ActiveConnection Property Example (VB)
TOCTitle: Catalog ActiveConnection Property Example (VB)
ms:assetid: 12a34091-e451-dbd1-e7f3-f794b84ee5b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248901(v=office.15)
ms:contentKeyID: 48543348
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3615932258524aedc2b81dbb5a7c88d71eff727e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481252"
---
# <a name="catalog-activeconnection-property-example-vb"></a><span data-ttu-id="823ad-102">Catalog ActiveConnection Property Example (VB)</span><span class="sxs-lookup"><span data-stu-id="823ad-102">Catalog ActiveConnection Property Example (VB)</span></span>

<span data-ttu-id="823ad-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="823ad-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="823ad-104">Установка для свойства [ActiveConnection](activeconnection-property-adox.md) допустимый, откройте подключение «открывает» каталог.</span><span class="sxs-lookup"><span data-stu-id="823ad-104">Setting the [ActiveConnection](activeconnection-property-adox.md) property to a valid, open connection "opens" the catalog.</span></span> <span data-ttu-id="823ad-105">Открытие каталога можно приступить к объекты схемы, содержащиеся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="823ad-105">From an open catalog, you can access the schema objects contained within that catalog.</span></span>

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

<span data-ttu-id="823ad-106">Установка для свойства **ActiveConnection** это допустимая строка подключения также «открывает» каталог.</span><span class="sxs-lookup"><span data-stu-id="823ad-106">Setting the **ActiveConnection** property to a valid connection string also "opens" the catalog.</span></span>

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
