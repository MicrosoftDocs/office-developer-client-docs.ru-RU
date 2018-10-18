---
<<<<<<< Название HEAD: DateCreated и DateModified свойства пример (VB) TOCTitle: DateCreated и DateModified свойства пример (VB) === название: пример Свойства DateCreated и DateModified (VB) TOCTitle: DateCreated и Пример: свойства DateModified (VB)
>>>>>>> главные ms:assetid: 5afdb5a9-394f-c38f-83a4-ae7017673c5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249316(v=office.15) ms:contentKeyID: 48545063 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="datecreated-and-datemodified-properties-example-vb"></a>DateCreated and DateModified Properties Example (VB)
=======
# <a name="datecreated-and-datemodified-properties-example-vb"></a>Пример свойства DateCreated и DateModified (VB)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

В этом примере демонстрируется свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) путем добавления нового [столбца](column-object-adox.md) к существующей [таблице](table-object-adox.md) и путем создания новой **таблицы**. Процедура DateOutput является обязательным для выполнения этого примера.

```vb 
 
' BeginDateCreatedVB 
Sub Main() 
 On Error GoTo DateCreatedXError 
 
 Dim cat As New ADOX.Catalog 
 Dim tblEmployees As ADOX.Table 
 Dim tblNewTable As ADOX.Table 
 
 ' Connect the catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 With cat 
 Set tblEmployees = .Tables("Employees") 
 
 ' Print current information about the Employees table. 
 DateOutput "Current properties", tblEmployees 
 
 ' Create and append column to the Employees table. 
 tblEmployees.Columns.Append "NewColumn", adInteger 
 .Tables.Refresh 
 
 ' Print new information about the Employees table. 
 DateOutput "After creating a new column", tblEmployees 
 
 ' Delete new column because this is a demonstration. 
 tblEmployees.Columns.Delete "NewColumn" 
 
 ' Create and append new Table object to the Northwind database. 
 Set tblNewTable = New ADOX.Table 
 tblNewTable.Name = "NewTable" 
 tblNewTable.Columns.Append "NewColumn", adInteger 
 .Tables.Append tblNewTable 
 .Tables.Refresh 
 
 ' Print information about the new Table object. 
 DateOutput "After creating a new table", .Tables("NewTable") 
 
 ' Delete new Table object because this is a demonstration. 
 .Tables.Delete tblNewTable.Name 
 End With 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
DateCreatedXError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
 
Sub DateOutput(strTemp As String, tblTemp As ADOX.Table) 
 ' Print DateCreated and DateModified information about 
 ' specified Table object. 
 Debug.Print strTemp 
 Debug.Print " Table: " & tblTemp.Name 
 Debug.Print " DateCreated = " & tblTemp.DateCreated 
 Debug.Print " DateModified = " & tblTemp.DateModified 
 Debug.Print 
End Sub 
' EndDateCreatedVB 
```

