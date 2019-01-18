---
title: Пример использования свойства IndexNulls (VB)
TOCTitle: IndexNulls property example (VB)
ms:assetid: 69b5661c-931e-3a1c-d60e-96a0f93b9494
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249414(v=office.15)
ms:contentKeyID: 48545417
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 488e37f53218a7dabfa6248ea1da7630f82818a6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699690"
---
# <a name="indexnulls-property-example-vb"></a><span data-ttu-id="24624-102">Пример использования свойства IndexNulls (VB)</span><span class="sxs-lookup"><span data-stu-id="24624-102">IndexNulls property example (VB)</span></span>

<span data-ttu-id="24624-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24624-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24624-104">В этом примере демонстрируется свойство [IndexNulls](indexnulls-property-adox.md) [индекса](index-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="24624-104">This example demonstrates the [IndexNulls](indexnulls-property-adox.md) property of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="24624-105">Код создает новый индекс и задает значение **IndexNulls** на основе ввода пользователя (из поля со списком с именем List1).</span><span class="sxs-lookup"><span data-stu-id="24624-105">The code creates a new index and sets the value of **IndexNulls** based on user input (from a list box named List1).</span></span> <span data-ttu-id="24624-106">Затем **индекс** добавляется **сотрудников** [в таблице](table-object-adox.md) в [каталог](catalog-object-adox.md) *"Борей"* .</span><span class="sxs-lookup"><span data-stu-id="24624-106">Then, the **Index** is appended to the **Employees** [Table](table-object-adox.md) in the *Northwind* [Catalog](catalog-object-adox.md).</span></span> <span data-ttu-id="24624-107">Новый **индекс** применяется к [набору записей](recordset-object-ado.md) , основанного на таблице **Employees** и открывается **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="24624-107">The new **Index** is applied to a [Recordset](recordset-object-ado.md) based on the **Employees** table, and the **Recordset** is opened.</span></span> <span data-ttu-id="24624-108">Новая запись добавляется к таблице **Employees** **нулевое** значение в индексированных полей.</span><span class="sxs-lookup"><span data-stu-id="24624-108">A new record is added to the **Employees** table, with a **Null** value in the indexed field.</span></span> <span data-ttu-id="24624-109">Отображение этой новой записи зависит от значения свойства **IndexNulls** .</span><span class="sxs-lookup"><span data-stu-id="24624-109">Whether this new record is displayed depends on the setting of the **IndexNulls** property.</span></span>

```vb
    ' IndexNullsVB 
    Sub Main() 
     On Error GoTo IndexNullsXError 
     
     Dim cnn As New ADODB.Connection 
     Dim catNorthwind As New ADOX.Catalog 
     Dim idxNew As New ADOX.Index 
     Dim rstEmployees As New ADODB.Recordset 
     Dim varBookmark As Variant 
     
     ' Connect the catalog. 
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source='c:\Program Files\" & _ 
     "Microsoft Office\Office\Samples\Northwind.mdb';" 
     
     Set catNorthwind.ActiveConnection = cnn 
     
     ' Append Country column to new index 
     idxNew.Columns.Append "Country" 
     idxNew.Name = "NewIndex" 
     
     Dim Response 
     Response = MsgBox("Allow 'Null' index? Otherwise ignore 'Null' index.", vbYesNo) 
     '"Allow 'Null' index? Otherwise ignore 'Null' index." 
     ', vbYesNo + vbCritical + vbDefaultButton2,,,, 
     If Response = vbYes Then ' User chose Yes. 
     idxNew.IndexNulls = adIndexNullsAllow 
     Else ' User chose No. 
     idxNew.IndexNulls = adIndexNullsIgnore 
     End If 
     
     'Append new index to Employees table 
     catNorthwind.Tables("Employees").Indexes.Append idxNew 
     
     rstEmployees.Index = idxNew.Name 
     rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
     adLockOptimistic, adCmdTableDirect 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Bookmark the newly added record 
     varBookmark = .Bookmark 
     
     ' Use the new index to set the order of the records. 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IndexNulls = " & idxNew.IndexNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IndexNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = varBookmark 
     .Delete 
     
     .Close 
     End With 
     
     'Clean up 
     Set rstEmployees = Nothing 
     catNorthwind.Tables("Employees").Indexes.Delete idxNew.Name 
     cnn.Close 
     Set cnn = Nothing 
     Set catNorthwind = Nothing 
     Set idxNew = Nothing 
     Exit Sub 
     
    IndexNullsXError: 
     
     If Not rstEmployees Is Nothing Then 
     If rstEmployees.State = adStateOpen Then rstEmployees.Close 
     End If 
     Set rstEmployees = Nothing 
     
     ' Delete new Index because this is a demonstration. 
     If Not catNorthwind Is Nothing Then 
     catNorthwind.Tables("Employees").Indexes.Delete idxNew.Name 
     End If 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     Set catNorthwind = Nothing 
     Set idxNew = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
     
    End Sub 
    ' EndIndexNullsVB
```
