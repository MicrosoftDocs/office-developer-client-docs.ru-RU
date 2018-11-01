---
title: The Limits of a Recordset
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 953e6c030c8ca4155b17603c03921e97fe3748e0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887287"
---
# <a name="the-limits-of-a-recordset"></a>The Limits of a Recordset


**Применимо к**: Access 2013, Office 2013

Используйте свойства **BOF** и **EOF** , чтобы определить, содержит ли объект **набора записей** записей или ли вы уменьшилось за пределы ограничения объекта **набора записей** , при перемещении между записями. Считайте **BOF** и **EOF** «фантомных» записей, размещенный в начало и конец **набора записей**. Основываясь на пример **набора записей** на основе [Данных проверки](chapter-3-examining-data.md), она теперь выглядит следующим образом:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ProductID</p></th>
<th><p>Имя продукта</p></th>
<th><p>Цена</p></th>
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
<td><p>7</p></td>
<td><p>Боб ячейку органических высохла Груши</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td><p>Диаграмме</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="even">
<td><p>28</p></td>
<td><p>Квашеная капуста Rssle</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Сушеные "apples"</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Longlife диаграмме</p></td>
<td><p>10.0000</p></td>
</tr>
<tr class="odd">
<td><p>ФУНКЦИЯ EOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


Свойство **BOF** возвращает **значение True** (значение -1) при текущей позиции записи перед первой записи и **значение False** (0) Если в настоящее время записи на или после первой записи.

Свойство **EOF** возвращает **значение True** , если в настоящее время записи после последней записи и **значение False** , если текущей позиции записи не позднее последней записи.

Если свойство **BOF** или **EOF** имеет **значение True**, отсутствует текущий запись, как показано в следующем коде:

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

При открытии объекта **набора записей** , содержащий записи не **BOF** и **EOF** свойства, как значение **True** , так и значения параметра свойства **RecordCount** объекта **набора записей** зависит от типа курсора. -1, будут возвращены для динамических курсоров (**CursorType** = **adOpenDynamic**) и 0 для других курсоров возвращается.

При открытии объекта **набора записей** , который содержит по крайней мере одна запись первая запись является текущей записи и свойства **BOF** и **EOF** — **значение False**.

При удалении последней оставшиеся записи в объекте **набора записей** , курсор остается в неопределенное состояние. Свойства **BOF** и **EOF** может оставаться **значение False** , пока вы пытаетесь изменить положение текущей записи в зависимости от поставщика.

