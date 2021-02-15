---
title: BoF, EOF properties (ADO)
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
# <a name="bof-eof-properties-ado"></a>BoF, EOF properties (ADO)


**Область применения**: Access 2013, Office 2013

**BOF** — указывает, что текущая позиция записи находится перед первой записью в [объекте Recordset.](recordset-object-ado.md)

**EOF** — указывает, что текущая позиция записи находится после последней записи в **объекте Recordset.**

## <a name="return-value"></a>Возвращаемое значение

Свойства **BOF** и **EOF** возвращают **boolean** значения.

## <a name="remarks"></a>Заметки

Используйте свойства **BOF** и **EOF,** чтобы определить, содержит ли объект **Recordset** записи или выходите за пределы объекта **Recordset** при переходе от записи к записи.

Свойство **BOF** возвращает true (-1), если текущая позиция записи находится перед первой записью, и **False** (0), если текущая запись находится в первой записи или после нее. 

Свойство **EOF** возвращает  true, если текущая позиция записи находится после последней записи, и **False,** если текущая запись находится в последней записи или до нее.

Если любое из свойств **BOF** или **EOF** имеет значение **True**, то текущей записи нет.

Если открыть объект  **Recordset** без записей, свойства **BOF** и **EOF** будут заданы как **True** (дополнительные сведения об этом состоянии набора записей см. в свойстве [RecordCount).](recordcount-property-ado.md) Когда вы открываете объект **Recordset,** содержащий хотя бы одну запись, первая запись является текущей записью, а свойства **BOF** и **EOF** — **False.**

Если удалить последнюю оставшуюся запись в объекте **Recordset**, свойства **BOF** и **EOF** могут по-прежнему иметь значение **False**, пока вы не попытаетесь изменить позицию текущей записи.

В этой таблице показано, какие методы **Move** разрешены с различными сочетаниями свойств **BOF** и **EOF.**

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


Разрешение метода **Move** не гарантирует, что метод успешно наймет запись; Это означает, что вызов указанного метода **Move** не будет создавать ошибку.

В следующей таблице показано, что происходит с настройками свойств **BOF** и **EOF** при вызове различных методов **Move,** но не удается найти запись.

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
<td><p>Установите <strong>true</strong></p></td>
<td><p>Установите <strong>true</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Без изменений</p></td>
<td><p>Без изменений</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</p></td>
<td><p>Установите <strong>true</strong></p></td>
<td><p>Без изменений</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</p></td>
<td><p>Без изменений</p></td>
<td><p>Установите <strong>true</strong></p></td>
</tr>
</tbody>
</table>

