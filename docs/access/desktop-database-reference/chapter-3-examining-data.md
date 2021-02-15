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

В главе 2 объясняется, как получить данные из источника данных в качестве объекта **Recordset.** В этой главе более **подробно рассматривается** набор записей, в том числе по навигации по набору **записей** и просмотру его данных.

**Записи имеют** методы и свойства, предназначенные для у прощего перемещения по ним и проверки их содержимого. В зависимости от функций, поддерживаемых поставщиком, некоторые методы или свойства **recordset** могут быть недоступны. Чтобы продолжить изучение объекта **Recordset,** рассмотрите объект **Recordset,** который будет возвращен из примера базы данных Northwind на Microsoft SQL Server 2000, используя следующий код:

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

Этот SQL возвращает набор **записей** с пятью строками (записями) и тремя столбцами (полями). Значения для каждой строки показаны в следующей таблице.

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
<td><p>7 </p></td>
<td><p>Органичное замеченное "По-разное" Боба</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="even">
<td><p>14 </p></td>
<td><p>Тофу</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p>Rssle Sauerkraut</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Manjimup : Apples</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Longlife Tofu</p></td>
<td><p>10.0000</p></td>
</tr>
</tbody>
</table>


В следующем разделе объясняется, как найти текущее положение курсора в этом примере **Recordset**.

В этой главе освещались следующие темы:

- [Locating the current record (ADO)](locating-the-current-record.md)
- [Навигация по данным (ADO)](navigating-through-the-data.md)
- [Understanding Recordset structure (ADO)](understanding-recordset-structure.md)
