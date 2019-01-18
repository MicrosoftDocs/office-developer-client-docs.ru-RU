---
title: Пример свойства ADO NumericScale и точность (VB)
TOCTitle: NumericScale and Precision properties example (VB)
ms:assetid: 060394b1-0c2c-3726-92a0-0f350bbaa3d5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248814(v=office.15)
ms:contentKeyID: 48543044
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2c234de05db031790f7241ed686fe4d86d83dc7d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704198"
---
# <a name="ado-numericscale-and-precision-properties-example-vb"></a>Пример свойства ADO NumericScale и точность (VB)


**Применимо к**: Access 2013, Office 2013

В этом примере с помощью свойства [NumericScale](numericscale-property-ado.md) и [точность](precision-property-ado.md) для отображения числовых масштаб и точность поля в таблице ***скидок*** базы данных ***Pubs*** .

```vb 
 
'BeginNumericScaleVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim rstDiscounts As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim fldTemp As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLDiscounts As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset 
 Set rstDiscounts = New ADODB.Recordset 
 strSQLDiscounts = "Discounts" 
 rstDiscounts.Open strSQLDiscounts, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 
 ' Display numeric scale and precision of 
 ' numeric and small integer fields 
 For Each fldTemp In rstDiscounts.Fields 
 If fldTemp.Type = adNumeric Or fldTemp.Type = adSmallInt Then 
 MsgBox "Field: " & fldTemp.Name & vbCr & _ 
 "Numeric scale: " & _ 
 fldTemp.NumericScale & vbCr & _ 
 "Precision: " & fldTemp.Precision 
 End If 
 Next fldTemp 
 
 ' clean up 
 rstDiscounts.Close 
 Cnxn.Close 
 Set rstDiscounts = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstDiscounts Is Nothing Then 
 If rstDiscounts.State = adStateOpen Then rstDiscounts.Close 
 End If 
 Set rstDiscounts = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndNumericScaleVB 
```

