---
<span data-ttu-id="e582c-101"><<<<<<< Название HEAD: столбцов и таблиц добавьте методы, TOCTitle примере свойство имя (VB): столбцов и таблиц добавьте методы, пример свойства имя (VB) === название: столбцов и таблиц добавьте методы, пример свойства Name (VB) TOCTitle: Столбцы и методы добавления таблиц, пример свойства Name (VB)</span><span class="sxs-lookup"><span data-stu-id="e582c-101"><<<<<<< HEAD title: Columns and Tables Append Methods, Name Property Example (VB) TOCTitle: Columns and Tables Append Methods, Name Property Example (VB) ======= title: Columns and Tables Append Methods, Name property example (VB) TOCTitle: Columns and Tables Append Methods, Name property example (VB)</span></span>
>>>>>>> <span data-ttu-id="e582c-102">главные ms:assetid: 39458400-f30c-0636-19f2-c2c2788a6534 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249140(v=office.15) ms:contentKeyID: 48544238 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e582c-102">master ms:assetid: 39458400-f30c-0636-19f2-c2c2788a6534 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249140(v=office.15) ms:contentKeyID: 48544238 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e582c-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e582c-103"><<<<<<< HEAD</span></span>
# <a name="columns-and-tables-append-methods-name-property-example-vb"></a><span data-ttu-id="e582c-104">Columns and Tables Append Methods, Name Property Example (VB)</span><span class="sxs-lookup"><span data-stu-id="e582c-104">Columns and Tables Append Methods, Name Property Example (VB)</span></span>
=======
# <a name="columns-and-tables-append-methods-name-property-example-vb"></a><span data-ttu-id="e582c-105">Столбцы и методы добавления таблиц, пример свойства Name (VB)</span><span class="sxs-lookup"><span data-stu-id="e582c-105">Columns and Tables Append Methods, Name property example (VB)</span></span>
>>>>>>> <span data-ttu-id="e582c-106">master</span><span class="sxs-lookup"><span data-stu-id="e582c-106">master</span></span>


<span data-ttu-id="e582c-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e582c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e582c-108">Следующий код демонстрирует создайте новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="e582c-108">The following code demonstrates how to create a new table.</span></span>

```vb 
 
' BeginCreateTableVB 
Sub Main() 
 On Error GoTo CreateTableError 
 
 Dim tbl As New Table 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 tbl.Name = "MyTable" 
 tbl.Columns.Append "Column1", adInteger 
 tbl.Columns.Append "Column2", adInteger 
 tbl.Columns.Append "Column3", adVarWChar, 50 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyTable' is added." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyTable' is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set tbl = Nothing 
 Exit Sub 
 
CreateTableError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateTableVB 
```

