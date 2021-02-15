---
title: Пример использования свойств NumericScale и Precision (VB)
TOCTitle: NumericScale and Precision properties example (VB)
ms:assetid: 728a76a3-1f80-935b-b6c7-94255ffe0160
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249462(v=office.15)
ms:contentKeyID: 48545610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e067c2ae893d19efdbcdc160fc7a7d54b9682297
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288548"
---
# <a name="numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="77081-102">Пример использования свойств NumericScale и Precision (VB)</span><span class="sxs-lookup"><span data-stu-id="77081-102">NumericScale and Precision properties example (VB)</span></span>


<span data-ttu-id="77081-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77081-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77081-104">В этом примере демонстрируются свойства [NumericScale](numericscale-property-adox.md) и [Precision](precision-property-adox.md) объекта [Column.](column-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="77081-104">This example demonstrates the [NumericScale](numericscale-property-adox.md) and [Precision](precision-property-adox.md) properties of the [Column](column-object-adox.md) object.</span></span> <span data-ttu-id="77081-105">Этот код отображает их значение для **таблицы "Сведения** о заказе" базы данных *Northwind.*</span><span class="sxs-lookup"><span data-stu-id="77081-105">This code displays their value for the **Order Details** table of the *Northwind* database.</span></span>

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

