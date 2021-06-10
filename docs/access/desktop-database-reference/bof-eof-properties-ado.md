---
title: Свойства BOF, EOF (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d36a65ce8a6808f2128749bd7fbc6e468acbd279
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296789"
---
# <a name="bof-eof-properties-ado"></a>Свойства BOF, EOF (ADO)


**Область применения**: Access 2013, Office 2013

**BOF** — указывает, что текущая позиция записи находится перед первой записью в [объекте Recordset.](recordset-object-ado.md)

**EOF** — указывает, что текущая позиция записи находится после последней записи объекта **Recordset.**

## <a name="return-value"></a>Возвращаемое значение

Свойства **BOF** и **EOF** возвращают **значения Boolean.**

## <a name="remarks"></a>Примечания

Используйте свойства **BOF** и **EOF,** чтобы определить, содержит ли объект **Recordset** записи или вы выходите за пределы объекта **Recordset** при переходе от записи к записи.

Свойство **BOF** возвращает **True** (-1), если текущая позиция записи находится перед первой записью и **False** (0), если текущая позиция записи находится на уровне или после первой записи.

Свойство **EOF** возвращает **True,** если текущая позиция записи находится после последней записи и false, если текущая позиция записи находится на последней записи или до нее. 

Если любое из свойств **BOF** или **EOF** имеет значение **True**, то текущей записи нет.

Если вы открываете объект **Recordset,** не содержащий записей, свойства **BOF** и **EOF** заданы для **True** (см. свойство [RecordCount](recordcount-property-ado.md) для получения дополнительных сведений об этом состоянии **набора записей).** Когда вы открываете объект **Recordset,** содержащий хотя бы одну запись, первая запись — текущая запись, а свойства **BOF** и **EOF** являются **false**.

Если удалить последнюю оставшуюся запись в объекте **Recordset**, свойства **BOF** и **EOF** могут по-прежнему иметь значение **False**, пока вы не попытаетесь изменить позицию текущей записи.

В этой таблице показано, какие методы **Move** разрешены с различными комбинациями свойств **BOF** и **EOF.**

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Move &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Move &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF=True,</strong><br />
<strong>EOF=False</strong></p></td>
<td><p>Разрешено</p></td>
<td><p>Ошибка</p></td>
<td><p>Ошибка</p></td>
<td><p>Разрешено</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF=False,</strong><br />
<strong>EOF=True</strong></p></td>
<td><p>Разрешено</p></td>
<td><p>Разрешено</p></td>
<td><p>Ошибка</p></td>
<td><p>Ошибка</p></td>
</tr>
<tr class="odd">
<td><p>Оба свойства имеют значение <strong>True</strong></p></td>
<td><p>Ошибка</p></td>
<td><p>Ошибка</p></td>
<td><p>Ошибка</p></td>
<td><p>Ошибка</p></td>
</tr>
<tr class="even">
<td><p>Оба свойства имеют значение <strong>False</strong></p></td>
<td><p>Разрешено</p></td>
<td><p>Разрешено</p></td>
<td><p>Разрешено</p></td>
<td><p>Разрешено</p></td>
</tr>
</tbody>
</table>


Разрешение метода **Move** не гарантирует успешное обнаружение записи. это означает, что вызов указанного метода **Move** не создает ошибку.

В следующей таблице показано, что происходит с настройками **свойств BOF** и **EOF** при вызове различных методов **Move,** но не удается успешно найти запись.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p>Настройка <strong>true</strong></p></td>
<td><p>Настройка <strong>true</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Без изменений</p></td>
<td><p>Без изменений</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</p></td>
<td><p>Настройка <strong>true</strong></p></td>
<td><p>Без изменений</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</p></td>
<td><p>Без изменений</p></td>
<td><p>Настройка <strong>true</strong></p></td>
</tr>
</tbody>
</table>

