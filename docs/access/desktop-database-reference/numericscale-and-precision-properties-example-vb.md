---
<span data-ttu-id="37a4d-101"><<<<<<< Название HEAD: NumericScale и TOCTitle пример свойства точности (VB): NumericScale и пример свойства точности (VB) === название: пример свойства NumericScale и точность (VB) TOCTitle: NumericScale и Пример: свойства точности (VB)</span><span class="sxs-lookup"><span data-stu-id="37a4d-101"><<<<<<< HEAD title: NumericScale and Precision Properties Example (VB) TOCTitle: NumericScale and Precision Properties Example (VB) ======= title: NumericScale and Precision properties example (VB) TOCTitle: NumericScale and Precision properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="37a4d-102">главные ms:assetid: 728a76a3-1f80-935b-b6c7-94255ffe0160 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249462(v=office.15) ms:contentKeyID: 48545610 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="37a4d-102">master ms:assetid: 728a76a3-1f80-935b-b6c7-94255ffe0160 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249462(v=office.15) ms:contentKeyID: 48545610 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="37a4d-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="37a4d-103"><<<<<<< HEAD</span></span>
# <a name="numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="37a4d-104">NumericScale and Precision Properties Example (VB)</span><span class="sxs-lookup"><span data-stu-id="37a4d-104">NumericScale and Precision Properties Example (VB)</span></span>
=======
# <a name="numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="37a4d-105">Пример свойства NumericScale и точность (VB)</span><span class="sxs-lookup"><span data-stu-id="37a4d-105">NumericScale and Precision properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="37a4d-106">master</span><span class="sxs-lookup"><span data-stu-id="37a4d-106">master</span></span>


<span data-ttu-id="37a4d-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37a4d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37a4d-108">В этом примере показано [NumericScale](numericscale-property-adox.md) и [точность](precision-property-adox.md) свойства объекта [столбца](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="37a4d-108">This example demonstrates the [NumericScale](numericscale-property-adox.md) and [Precision](precision-property-adox.md) properties of the [Column](column-object-adox.md) object.</span></span> <span data-ttu-id="37a4d-109">Этот код отображает значения для таблицы **Сведения о заказе** из базы данных *Northwind* .</span><span class="sxs-lookup"><span data-stu-id="37a4d-109">This code displays their value for the **Order Details** table of the *Northwind* database.</span></span>

```vb 
 
' BeginNumericScalePrecVB 
Sub Main() 
 On Error GoTo NumericScalePrecXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tblOD As ADOX.Table 
 Dim colLoop As ADOX.Column 
 
 ' Connect the catalog. 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "data source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 ' Retrieve the Order Details table 
 Set tblOD = cat.Tables("Order Details") 
 
 ' Display numeric scale and precision of 
 ' small integer fields. 
 For Each colLoop In tblOD.Columns 
 If colLoop.Type = adSmallInt Then 
 MsgBox "Column: " & colLoop.Name & vbCr & _ 
 "Numeric scale: " & _ 
 colLoop.NumericScale & vbCr & _ 
 "Precision: " & colLoop.Precision 
 End If 
 Next colLoop 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
NumericScalePrecXError: 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndNumericScalePrecVB 
```

