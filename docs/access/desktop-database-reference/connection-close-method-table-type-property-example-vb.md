---
title: Метод Close подключения, пример свойства типа таблица (VB)
TOCTitle: Connection Close Method, Table Type property example (VB)
ms:assetid: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15)
ms:contentKeyID: 48547754
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 388e601d7267eabd01843640ab795fd0ea914a05
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868317"
---
# <a name="connection-close-method-table-type-property-example-vb"></a><span data-ttu-id="d17ad-102">Метод Close подключения, пример свойства типа таблица (VB)</span><span class="sxs-lookup"><span data-stu-id="d17ad-102">Connection Close Method, Table Type property example (VB)</span></span>

<span data-ttu-id="d17ad-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d17ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d17ad-104">Для свойства [ActiveConnection](activeconnection-property-adox.md) значение **Nothing** «закрыть» каталог.</span><span class="sxs-lookup"><span data-stu-id="d17ad-104">Setting the [ActiveConnection](activeconnection-property-adox.md) property to **Nothing** should "close" the catalog.</span></span> <span data-ttu-id="d17ad-105">Связанные коллекции будет пустым.</span><span class="sxs-lookup"><span data-stu-id="d17ad-105">Associated collections will be empty.</span></span> <span data-ttu-id="d17ad-106">Любые объекты, которые были созданы на основе схемы объектам в каталоге будут изолированы.</span><span class="sxs-lookup"><span data-stu-id="d17ad-106">Any objects that were created from schema objects in the catalog will be orphaned.</span></span> <span data-ttu-id="d17ad-107">Любые свойства на те объекты, которые были кэшированы по-прежнему доступны, но при чтении свойства, которые требуют вызова к поставщику завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d17ad-107">Any properties on those objects that have been cached will still be available, but attempting to read properties that require a call to the provider will fail.</span></span>

```vb 
 
    ' BeginCloseConnectionVB 
    Sub Main() 
    On Error GoTo CloseConnectionByNothingError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    Dim tbl As ADOX.Table 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Set tbl = cat.Tables(0) 
    Debug.Print tbl.Type ' Cache tbl.Type info 
    Set cat.ActiveConnection = Nothing 
    Debug.Print tbl.Type ' tbl is orphaned 
    ' Previous line will succeed if this was cached 
    Debug.Print tbl.Columns(0).DefinedSize 
    ' Previous line will fail if this info has not been cached 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    CloseConnectionByNothingError: 
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndCloseConnectionVB 
```

<br/>

<span data-ttu-id="d17ad-108">Закрытие объект [подключения](connection-object-ado.md) , который использовался для «открыть» каталог должен иметь тот же эффект, что для свойства **ActiveConnection** значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="d17ad-108">Closing a [Connection](connection-object-ado.md) object that was used to "open" the catalog should have the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

```vb
    Sub CloseConnection() 
     On Error GoTo CloseConnectionError 
     
     Dim cnn As New ADODB.Connection 
     Dim cat As New ADOX.Catalog 
     Dim tbl As ADOX.Table 
     
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Set cat.ActiveConnection = cnn 
     Set tbl = cat.Tables(0) 
     Debug.Print tbl.Type ' Cache tbl.Type info 
     cnn.Close 
     Debug.Print tbl.Type ' tbl is orphaned 
     ' Previous line will succeed if this was cached 
     Debug.Print tbl.Columns(0).DefinedSize 
     ' Previous line will fail if this info has not been cached 
     
     'Clean up 
     Set cat = Nothing 
     Set cnn = Nothing 
     Exit Sub 
     
    CloseConnectionError: 
     
     Set cat = Nothing 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndCloseConnection2VB
```
