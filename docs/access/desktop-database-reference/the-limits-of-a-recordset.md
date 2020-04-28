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

Используйте свойства **BOF** и **EOF** , чтобы определить, содержит ли объект **Recordset** записи или вы не превысили ограничения объекта **Recordset** при переходе с записи на запись. **BOF** и **EOF** должны рассматриваться как "фантомные" записи, расположенные в начале и конце **набора записей**. При создании примера **набора записей** из [проверки данных](chapter-3-examining-data.md)он теперь выглядит следующим образом:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ProductID</p></th>
<th><p>Здесь</p></th>
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
<td><p>Ункле Марии Дриед груши</p></td>
<td><p>30,0000</p></td>
</tr>
<tr class="odd">
<td><p>14 </p></td>
<td><p>тофу</p></td>
<td><p>23,2500</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>Рссле Сауеркраут</p></td>
<td><p>45,6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Манжимуп Дриед яблоки</p></td>
<td><p>53,0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Лонглифе тофу</p></td>
<td><p>10,0000</p></td>
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


Свойство **BOF** возвращает **значение true** (-1), если положение текущей записи находится перед первой записью, и **false** (0), если текущая позиция записи находится в или после первой записи.

Свойство **EOF** возвращает **значение true** , если текущая позиция записи находится после последней записи, и **значение false** , если текущая позиция записи находится в или до последней записи.

Если свойство **BOF** или **EOF** имеет **значение true**, текущая запись отсутствует, как показано в следующем коде:

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

При открытии объекта **Recordset** , не содержащего записей, свойству **BOF** и **EOF** присвоено значение **true** , а значение свойства **RecordCount** объекта **Recordset** зависит от типа курсора. значение-1 будет возвращено для динамических курсоров (**CursorType** = **адопендинамик**), а для других курсоров будет возвращено значение 0.

При открытии объекта **Recordset** , содержащего по крайней мере одну запись, первая запись является текущей, а свойство **BOF** и **EOF** имеет **значение false**.

При удалении последней оставшейся записи в объекте **Recordset** курсор остается в неопределенном состоянии. Свойства **BOF** и **EOF** могут иметь **значение false** до тех пор, пока вы не попытаетесь изменить положение текущей записи в зависимости от поставщика.

