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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720543"
---
# <a name="chapter-3-examining-data"></a>Глава 3. Изучение данных

**Применимо к**: Access 2013, Office 2013

Глава 2 объясняется порядок извлечения данных из источника данных в качестве объекта **набора записей** . В этой главе рассматриваются **записей** более подробно, в том числе как перейти по **записей** и просматривать данные.

**Наборы записей** имеют методы и свойства, предназначенные для упрощения их перемещение по ним и просматривать их содержимое. В зависимости от функциональных возможностей, поддерживаемых поставщиком некоторые из **набора записей** методов и свойств не становятся доступны. Чтобы продолжить изучение объекта **набора записей** , рассмотрите **набора записей** , возвращаемого из образца базы данных Northwind на Microsoft SQL Server 2000, используйте следующий код:

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

Этот запрос SQL возвращает **набора записей** с помощью пяти строк (записей) и три столбца (поля). В следующей таблице показаны значения для каждой строки.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ПОЛЕ 0<br />
Имя = ProductID</p></th>
<th><p>ПОЛЕ 1<br />
Имя = имя продукта</p></th>
<th><p>ПОЛЕ 2<br />
Имя = цена</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>7</p></td>
<td><p>Боб ячейку органических высохла Груши</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="even">
<td><p>14</p></td>
<td><p>Диаграмме</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p>Квашеная капуста Rssle</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Сушеные "apples"</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Longlife диаграмме</p></td>
<td><p>10.0000</p></td>
</tr>
</tbody>
</table>


Следующем разделе объясняется, как найти текущей позиции курсора в этом примере **набора записей**.

В этой главе рассматриваются следующие темы:

- [Поиск текущей записи (ADO)](locating-the-current-record.md)
- [Переход между данными (ADO)](navigating-through-the-data.md)
- [Общие сведения о структуре набора записей (ADO)](understanding-recordset-structure.md)
