---
<span data-ttu-id="7d872-101"><<<<<<< Название HEAD: TOCTitle примере свойство ParentCatalog (VB): пример свойства ParentCatalog (VB) === название: пример свойства ParentCatalog (VB) TOCTitle: пример свойства ParentCatalog (VB)</span><span class="sxs-lookup"><span data-stu-id="7d872-101"><<<<<<< HEAD title: ParentCatalog Property Example (VB) TOCTitle: ParentCatalog Property Example (VB) ======= title: ParentCatalog property example (VB) TOCTitle: ParentCatalog property example (VB)</span></span>
>>>>>>> <span data-ttu-id="7d872-102">главные ms:assetid: 3bd01153-40b5-1a45-67e2-eb8154c3fe33 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249152(v=office.15) ms:contentKeyID: 48544295 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="7d872-102">master ms:assetid: 3bd01153-40b5-1a45-67e2-eb8154c3fe33 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249152(v=office.15) ms:contentKeyID: 48544295 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="7d872-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7d872-103"><<<<<<< HEAD</span></span>
# <a name="parentcatalog-property-example-vb"></a><span data-ttu-id="7d872-104">ParentCatalog Property Example (VB)</span><span class="sxs-lookup"><span data-stu-id="7d872-104">ParentCatalog Property Example (VB)</span></span>
=======
# <a name="parentcatalog-property-example-vb"></a><span data-ttu-id="7d872-105">Пример свойства ParentCatalog (VB)</span><span class="sxs-lookup"><span data-stu-id="7d872-105">ParentCatalog property example (VB)</span></span>
>>>>>>> <span data-ttu-id="7d872-106">master</span><span class="sxs-lookup"><span data-stu-id="7d872-106">master</span></span>


<span data-ttu-id="7d872-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d872-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7d872-108">Следующий код демонстрирует использование свойства [ParentCatalog](parentcatalog-property-adox.md) для доступа к свойству от поставщика перед добавлением таблицы в каталоге.</span><span class="sxs-lookup"><span data-stu-id="7d872-108">The following code demonstrates how to use the [ParentCatalog](parentcatalog-property-adox.md) property to access a provider-specific property prior to appending a table to a catalog.</span></span> <span data-ttu-id="7d872-109">Является ли данное свойство AutoIncrement, которая создает поле AutoIncrement базы данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="7d872-109">The property is AutoIncrement, which creates an AutoIncrement field in a Microsoft Jet database.</span></span>

```vb 
 
' BeginCreateAutoIncrColumnVB 
Sub Main() 
 On Error GoTo CreateAutoIncrColumnError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tbl As New ADOX.Table 
 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 With tbl 
 .Name = "MyContacts" 
 Set .ParentCatalog = cat 
 ' Create fields and append them to the new Table object. 
 .Columns.Append "ContactId", adInteger 
 ' Make the ContactId column and auto incrementing column 
 .Columns("ContactId").Properties("AutoIncrement") = True 
 .Columns.Append "CustomerID", adVarWChar 
 .Columns.Append "FirstName", adVarWChar 
 .Columns.Append "LastName", adVarWChar 
 .Columns.Append "Phone", adVarWChar, 20 
 .Columns.Append "Notes", adLongVarWChar 
 End With 
 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyContacts' is added." 
 
 ' Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyContacts' is delete." 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
CreateAutoIncrColumnError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateAutoIncrColumnVB 
```

