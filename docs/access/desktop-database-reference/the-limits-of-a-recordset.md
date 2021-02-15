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

Используйте свойства **BOF** и **EOF,** чтобы определить, содержит ли объект **Recordset** записи или выходите за пределы объекта **Recordset** при переходе от записи к записи. Думайте **о BOF** и **EOF** как "дозорные" записи, которые находятся в начале и конце **recordset**. На основе примера **recordset** из [изучения данных](chapter-3-examining-data.md)он будет выглядеть так:

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
<td><p>Органичное замеченное "По-разное" Боба</p></td>
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
<td><p>Manjimup : Apples</p></td>
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


Свойство **BOF** возвращает true (-1), если текущая позиция записи находится перед первой записью, и **False** (0), если текущая запись находится в первой записи или после нее. 

Свойство **EOF** возвращает  true, если текущая позиция записи находится после последней записи, и **False,** если текущая запись находится в последней записи или до нее.

Если свойство **BOF или** **EOF** имеет **true,** текущая запись не существует, как показано в следующем коде:

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

Если открыть объект **Recordset** без записей, свойства **BOF** и **EOF** будут одновременно заданы как true, так и значение свойства  **RecordCount** объекта **Recordset** зависит от типа курсора. Для динамических курсоров возвращается -1 **(CursorType**  =  **adOpenDynamic),** а для других — 0.

Когда вы открываете объект **Recordset,** содержащий хотя бы одну запись, первая запись является текущей записью, а свойства **BOF** и **EOF** — **False.**

При удалении последней оставшейся записи в **объекте Recordset** курсор остается в неустановленном состоянии. Свойства **BOF** и **EOF** могут оставаться **false,** пока вы не попытались изменить положение текущей записи в зависимости от поставщика.

