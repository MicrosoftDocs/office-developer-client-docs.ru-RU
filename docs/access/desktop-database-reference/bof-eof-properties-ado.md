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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726129"
---
# <a name="bof-eof-properties-ado"></a>Свойства BOF, EOF (ADO)


**Применимо к**: Access 2013, Office 2013

**BOF** — указывает, что положение текущей записи — перед первой записи в объекте [набора записей](recordset-object-ado.md) .

**Функция EOF** — указывает, что положение текущей записи после последней записи в объекте **набора записей** .

## <a name="return-value"></a>Возвращаемое значение

**Логические** значения, возвращаемые свойства **BOF** и **EOF** .

## <a name="remarks"></a>Замечания

Используйте свойства **BOF** и **EOF** , чтобы определить, содержит ли объект **набора записей** записей или ли вы уменьшилось за пределы ограничения объекта **набора записей** , при перемещении между записями.

Свойство **BOF** возвращает **значение True** (значение -1) при текущей позиции записи перед первой записи и **значение False** (0) Если в настоящее время записи на или после первой записи.

Свойство **EOF** возвращает **значение True** , если в настоящее время записи после последней записи и **значение False** , если текущей позиции записи не позднее последней записи.

Если параметр **BOF** или **EOF** свойство имеет **значение True**, нет нет текущей записи.

При открытии объекта **набора записей** , содержащий записи не **BOF** и **EOF** задано значение **True** (см. свойство [RecordCount](recordcount-property-ado.md) Дополнительные сведения об этом состоянии **набора записей**). При открытии объекта **набора записей** , который содержит по крайней мере одна запись первая запись является текущей записи и свойства **BOF** и **EOF** — **значение False**.

При удалении последней оставшиеся записи в объекте **набора записей** , свойства **BOF** и **EOF** может оставаться **значение False,** пока вы пытаетесь изменить положение текущей записи.

Этой таблице показано, какие методы **перемещения** может использоваться с разные сочетания свойства **BOF** и **EOF** .

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
<th><p>MoveFirst<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Перемещение &lt; 0</p></th>
<th><p><br />
Перемещение 0</p></th>
<th><p>MoveNext,<br />
Перемещение &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = True,</strong><br />
<strong>Функция EOF = False</strong></p></td>
<td><p>Разрешено</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>Разрешено</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = False,</strong><br />
<strong>Функция EOF = True</strong></p></td>
<td><p>Разрешено</p></td>
<td><p>Разрешено</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
</tr>
<tr class="odd">
<td><p>Оба <strong>значение True</strong></p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
<td><p>Error</p></td>
</tr>
<tr class="even">
<td><p>Оба <strong>False</strong></p></td>
<td><p>Разрешено</p></td>
<td><p>Разрешено</p></td>
<td><p>Разрешено</p></td>
<td><p>Разрешено</p></td>
</tr>
</tbody>
</table>


Позволяет **переместить** метод не гарантирует, что метод будет успешно найдите запись; только это означает, что вызов **Перемещение** указанный метод не возникнет ошибка.

В следующей таблице показаны, что происходит с **BOF** или **EOF** параметров при вызове различные методы **перемещения** , но не удается найти запись успешно.

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
<td><p><strong>MoveFirst</strong> <strong>MoveLast</strong></p></td>
<td><p>Значение <strong>True</strong></p></td>
<td><p>Значение <strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Перемещение</strong> 0</p></td>
<td><p>Без изменений</p></td>
<td><p>Без изменений</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Переместите</strong> &lt; 0</p></td>
<td><p>Значение <strong>True</strong></p></td>
<td><p>Без изменений</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Переместите</strong> &gt; 0</p></td>
<td><p>Без изменений</p></td>
<td><p>Значение <strong>True</strong></p></td>
</tr>
</tbody>
</table>

