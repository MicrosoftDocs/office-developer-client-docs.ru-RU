---
<<<<<<< Заголовок HEAD: кластерные примере свойство (VB) TOCTitle: кластерные примере свойство (VB) === заголовок: пример кластерные свойства (VB) TOCTitle: пример кластерные свойства (VB)
>>>>>>> главные ms:assetid: 1065622d-9473-209a-95be-c4b0ab5b687a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248872(v=office.15) ms:contentKeyID: 48543293 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="clustered-property-example-vb"></a>Clustered Property Example (VB)
=======
# <a name="clustered-property-example-vb"></a>Пример свойства кластерные (VB)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

В этом примере демонстрируется свойство [Clustered](clustered-property-adox.md) [индекса](index-object-adox.md). Обратите внимание, что баз данных Microsoft Jet не поддерживают кластеризованных индексов, поэтому этот пример возвращает **значение False** для свойства **Clustered** всех индексов в базе *данных "Борей"* .

```vb 
 
' BeginClusteredVB 
Sub Main() 
 On Error GoTo ClusteredXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tblLoop As ADOX.Table 
 Dim idxLoop As ADOX.Index 
 Dim strCnn As String 
 
 strCnn = "Provider='SQLOLEDB';Data Source='MySqlServer';Initial Catalog='pubs';" & _ 
 "Integrated Security='SSPI';" 
 ' Connect the catalog. 
 cnn.Open strCnn 
 cat.ActiveConnection = cnn 
 
 ' Enumerate Tables 
 For Each tblLoop In cat.Tables 
 'Enumerate Indexes 
 For Each idxLoop In tblLoop.Indexes 
 Debug.Print tblLoop.Name & " " & _ 
 idxLoop.Name & " " & idxLoop.Clustered 
 Next idxLoop 
 Next tblLoop 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ClusteredXError: 
 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndClusteredVB 
```

