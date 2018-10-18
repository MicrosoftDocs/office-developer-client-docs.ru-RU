---
<span data-ttu-id="5512d-101"><<<<<<< Название HEAD: PrimaryKey и TOCTitle пример уникальные свойства (VB): PrimaryKey и пример уникальные свойства (VB) === название: пример свойства PrimaryKey и Unique (VB) TOCTitle: PrimaryKey и Unique пример свойств (VB)</span><span class="sxs-lookup"><span data-stu-id="5512d-101"><<<<<<< HEAD title: PrimaryKey and Unique Properties Example (VB) TOCTitle: PrimaryKey and Unique Properties Example (VB) ======= title: PrimaryKey and Unique properties example (VB) TOCTitle: PrimaryKey and Unique properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="5512d-102">главные ms:assetid: 888f1a35-b883-2449-3b70-103e5116b29f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249597(v=office.15) ms:contentKeyID: 48546137 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="5512d-102">master ms:assetid: 888f1a35-b883-2449-3b70-103e5116b29f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249597(v=office.15) ms:contentKeyID: 48546137 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5512d-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="5512d-103"><<<<<<< HEAD</span></span>
# <a name="primarykey-and-unique-properties-example-vb"></a><span data-ttu-id="5512d-104">PrimaryKey and Unique Properties Example (VB)</span><span class="sxs-lookup"><span data-stu-id="5512d-104">PrimaryKey and Unique Properties Example (VB)</span></span>
=======
# <a name="primarykey-and-unique-properties-example-vb"></a><span data-ttu-id="5512d-105">Пример свойства PrimaryKey и Unique (VB)</span><span class="sxs-lookup"><span data-stu-id="5512d-105">PrimaryKey and Unique properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="5512d-106">master</span><span class="sxs-lookup"><span data-stu-id="5512d-106">master</span></span>


<span data-ttu-id="5512d-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5512d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5512d-108">В этом примере свойства [PrimaryKey](primarykey-property-adox.md) и [Уникальный](unique-property-adox.md) [индекс](index-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5512d-108">This example demonstrates the [PrimaryKey](primarykey-property-adox.md) and [Unique](unique-property-adox.md) properties of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="5512d-109">Код создает новую таблицу с двумя столбцами.</span><span class="sxs-lookup"><span data-stu-id="5512d-109">The code creates a new table with two columns.</span></span> <span data-ttu-id="5512d-110">Свойства **PrimaryKey** и **Unique** используются для сделать один столбец первичного ключа, для которого не разрешены повторяющиеся значения.</span><span class="sxs-lookup"><span data-stu-id="5512d-110">The **PrimaryKey** and **Unique** properties are used to make one column the primary key for which duplicate values are not allowed.</span></span>

```vb 
 
' BeginPrimaryKeyVB 
Sub Main() 
 On Error GoTo PrimaryKeyXError 
 
 Dim catNorthwind As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 Dim idxNew As New ADOX.Index 
 Dim idxLoop As New ADOX.Index 
 Dim colLoop As New ADOX.Column 
 
 ' Connect the catalog 
 catNorthwind.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append new Primary Key index on NumField column 
 ' to new table 
 idxNew.Name = "NumIndex" 
 idxNew.Columns.Append "NumField" 
 idxNew.PrimaryKey = True 
 idxNew.Unique = True 
 tblNew.Indexes.Append idxNew 
 
 ' Append an index on Textfield to new table. 
 ' Note the different technique: Specifying index and 
 ' column name as parameters of the Append method 
 tblNew.Indexes.Append "TextIndex", "TextField" 
 
 ' Append the new table 
 catNorthwind.Tables.Append tblNew 
 
 With tblNew 
 Debug.Print tblNew.Indexes.Count & " Indexes in " & _ 
 tblNew.Name & " Table" 
 
 ' Enumerate Indexes collection. 
 For Each idxLoop In .Indexes 
 With idxLoop 
 Debug.Print "Index " & .Name 
 Debug.Print " Primary key = " & .PrimaryKey 
 Debug.Print " Unique = " & .Unique 
 
 ' Enumerate Columns collection of each Index 
 ' object. 
 Debug.Print " Columns" 
 For Each colLoop In .Columns 
 Debug.Print " " & colLoop.Name 
 Next colLoop 
 End With 
 Next idxLoop 
 
 End With 
 
 ' Delete new table as this is a demonstration. 
 catNorthwind.Tables.Delete tblNew.Name 
 
 'Clean up 
 Set catNorthwind.ActiveConnection = Nothing 
 Set catNorthwind = Nothing 
 Set tblNew = Nothing 
 Set idxNew = Nothing 
 Set idxLoop = Nothing 
 Set colLoop = Nothing 
 Exit Sub 
 
PrimaryKeyXError: 
 
 Set catNorthwind = Nothing 
 Set tblNew = Nothing 
 Set idxNew = Nothing 
 Set idxLoop = Nothing 
 Set colLoop = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndPrimaryKeyVB 
```

