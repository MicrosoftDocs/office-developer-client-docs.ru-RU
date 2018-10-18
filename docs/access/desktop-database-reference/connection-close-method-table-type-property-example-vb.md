---
<<<<<<< Название HEAD: метод Close подключения, пример свойства типа таблица (VB) TOCTitle: метод Close подключения, пример свойства типа таблица (VB) === название: метод Close подключения, пример свойства типа таблица (VB) TOCTitle: Метод Close подключения, пример свойства типа таблица (VB)
>>>>>>> главные ms:assetid: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15) ms:contentKeyID: 48547754 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="connection-close-method-table-type-property-example-vb"></a>Connection Close Method, Table Type Property Example (VB)
=======
# <a name="connection-close-method-table-type-property-example-vb"></a>Метод Close подключения, пример свойства типа таблица (VB)
>>>>>>> master

**Применимо к**: Access 2013 | Office 2013

Для свойства [ActiveConnection](activeconnection-property-adox.md) значение **Nothing** «закрыть» каталог. Связанные коллекции будет пустым. Любые объекты, которые были созданы на основе схемы объектам в каталоге будут изолированы. Любые свойства на те объекты, которые были кэшированы по-прежнему доступны, но при чтении свойства, которые требуют вызова к поставщику завершится с ошибкой.

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

Закрытие объект [подключения](connection-object-ado.md) , который использовался для «открыть» каталог должен иметь тот же эффект, что для свойства **ActiveConnection** значение **Nothing**.

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
