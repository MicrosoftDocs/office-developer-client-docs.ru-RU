---
title: Глава 3. Изучение данных
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcf837a02c40d11fecfa56b8aa34ac80a848411
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296460"
---
# <a name="chapter-3-examining-data"></a>Глава 3. Изучение данных

**Область применения**: Access 2013, Office 2013

В главе 2 описывается извлечение данных из источника данных в качестве объекта **Recordset** . В этой главе описывается более подробное описание объекта **Recordset** , в том числе перемещение по **набору записей** и просмотр его данных.

**Наборы записей** имеют методы и свойства, предназначенные для упрощения их перемещения и проверки их содержимого. В зависимости от функциональных возможностей, поддерживаемых поставщиком, некоторые методы или свойства **набора записей** могут быть недоступны. Чтобы продолжить изучение объекта **Recordset** , рассмотрим **набор записей** , который будет возвращен из учебной базы данных Northwind в Microsoft SQL Server 2000, используя следующий код:

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

Этот запрос SQL возвращает объект **Recordset** с пятью строками (записями) и тремя столбцами (полями). Значения для каждой строки показаны в следующей таблице.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ПОЛЕ 0<br />
Name = ProductID</p></th>
<th><p>ПОЛЕ 1<br />
Name = ProductName</p></th>
<th><p>ПОЛЕ 2<br />
Name = UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>см</p></td>
<td><p>Ункле Марии Дриед груши</p></td>
<td><p>30,0000</p></td>
</tr>
<tr class="even">
<td><p>14</p></td>
<td><p>Тофу</p></td>
<td><p>23,2500</p></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
<td><p>Рссле Сауеркраут</p></td>
<td><p>45,6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Манжимуп Дриед яблоки</p></td>
<td><p>53,0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Лонглифе тофу</p></td>
<td><p>10,0000</p></td>
</tr>
</tbody>
</table>


В следующем разделе рассказывается, как определить расположение текущего положения курсора в этом примере **набора записей**.

В этой главе рассматриваются следующие темы:

- [Поиск текущей записи (ADO)](locating-the-current-record.md)
- [Навигация по данным (ADO)](navigating-through-the-data.md)
- [Общие сведения о структуре Recordset (ADO)](understanding-recordset-structure.md)
