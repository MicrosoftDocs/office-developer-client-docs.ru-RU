---
title: The Limits of a Recordset
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d0da48080b64e43cc39b9567275e1a8755a8881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314115"
---
# <a name="limits-of-a-recordset"></a>Ограничения набора записей


**Область применения**: Access 2013, Office 2013

Используйте свойства **BOF** и **EOF,** чтобы определить, содержит ли объект **Recordset** записи или вы выходите за пределы объекта **Recordset** при переходе от записи к записи. Думайте **о BOF** и **EOF** как о "фантомных" записях, которые находятся в начале и конце **recordset.** В примере **Recordset** из [Examining Data](chapter-3-examining-data.md)теперь будет выглядеть так:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ProductID</p></th>
<th><p>ProductName</p></th>
<th><p>UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p>7 </p></td>
<td><p>Органические сушеные груши дяди Боба</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="odd">
<td><p>14 </p></td>
<td><p>Тофу</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="even">
<td><p>28</p></td>
<td><p>Rssle Sauerkraut</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Сушеные яблоки Manjimup</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Longlife Tofu</p></td>
<td><p>10.0000</p></td>
</tr>
<tr class="odd">
<td><p>EOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


Свойство **BOF** возвращает **True** (-1), если текущая позиция записи находится перед первой записью и **False** (0), если текущая позиция записи находится на уровне или после первой записи.

Свойство **EOF** возвращает **True,** если текущая позиция записи находится после последней записи и false, если текущая позиция записи находится на последней записи или до нее. 

Если свойство **BOF или** **EOF** является **True,** текущая запись не отображается, как показано в следующем коде:

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

Если вы откроете объект  **Recordset,** не содержащий записей, свойства **BOF** и **EOF** заданы как true, так и значение параметра свойства **RecordCount объекта RecordCount** зависит от типа курсора.  -1 будет возвращен для динамических курсоров **(CursorType**  =  **adOpenDynamic)** и 0 будет возвращен для других курсоров.

Когда вы открываете объект **Recordset,** содержащий хотя бы одну запись, первая запись — текущая запись, а свойства **BOF** и **EOF** являются **false**.

При удалении последней оставшейся записи в **объекте Recordset** курсор остается в неопределяемом состоянии. Свойства **BOF** и **EOF**  могут оставаться false до тех пор, пока вы не попытайтесь изменить текущую запись в зависимости от поставщика.

