---
title: Свойство Recordset.EOF (DAO)
TOCTitle: EOF Property
ms:assetid: aa82c6f9-89da-1061-437c-8ffb000744b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821459(v=office.15)
ms:contentKeyID: 48546950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 931de7dfc2cfb80726aafe7077c6107ec65d2f40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300611"
---
# <a name="recordseteof-property-dao"></a>Свойство Recordset.EOF (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает, находится ли позиция текущей записи после последней записи в объекте **Recordset**. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение*.EOF

*выражение* Переменная, которая представляет объект **Recordset**.

## <a name="remarks"></a>Комментарии

С помощью свойств **BOF** и **EOF** можно определить, содержит ли объект **Recordset** записи и не вышли ли вы за пределы объекта **Recordset** при переходе от записи к записи.

Значения, возвращаемые свойствами **BOF** и **EOF**, определяются расположением указателя текущей записи.

Если любое из свойств **BOF** или **EOF** имеет значение **True**, то текущей записи нет.

Если открыть объект **Recordset**, не содержащий записей, свойства **BOF** и **EOF** будут иметь значение **True**, а свойство **RecordCount** объекта **Recordset** — значение 0. Если открыть объект **Recordset**, содержащий хотя бы одну запись, первая запись будет текущей записью, а свойства **BOF** и **EOF** будут иметь значение **False**; они будут иметь значение **False** до тех пор, пока вы не переместитесь за начало или конец объекта **Recordset** с помощью метода **MovePrevious** или **MoveNext** соответственно. Если вы переместитесь за начало или конец объекта **Recordset**, то не будет ни текущей, ни другой записи.

Если удалить последнюю оставшуюся запись в объекте **Recordset**, свойства **BOF** и **EOF** могут по-прежнему иметь значение **False**, пока вы не попытаетесь изменить позицию текущей записи.

Если использовать метод **MoveLast** для объекта **Recordset**, содержащего записи, последняя запись станет текущей записью; если затем воспользоваться методом **MoveNext**, текущая запись станет недопустимой, и свойству **EOF** будет присвоено значение **True**. И наоборот, если использовать метод **MoveFirst** для объекта **Recordset**, содержащего записи, первая запись станет текущей записью; если затем воспользоваться методом **MovePrevious**, текущей записи не будет, и свойству **BOF** будет присвоено значение **True**.

Обычно при работе со всеми записями в объекте **Recordset** код проходит через все записи с помощью метода **MoveNext**, пока значение свойства **EOF** не станет равно **True**.

Если вы воспользуетесь методом **MoveNext**, когда свойство **EOF** имеет значение **True**, или методом **MovePrevious**, когда свойство **BOF** имеет значение **True**, возникнет ошибка.

В этой таблице показано, какие методы Move разрешено использовать при различных сочетаниях свойств **BOF** и **EOF**.

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


Разрешение использовать метод Move не означает, что этот метод успешно найдет запись. Это всего лишь значит, что попытки выполнить указанный метод Move разрешены и не приведут к возникновению ошибки. В результате выполнения методов Move состояние свойств **BOF** и **EOF** может изменяться.

Метод **OpenRecordset** внутренним образом вызывает метод **MoveFirst**. Таким образом, при использовании метода **OpenRecordset** для пустого набора записей свойствам **BOF** и **EOF** будет присвоено значение **True**. (Сведения о том, как ведет себя метод **MoveFirst** при его неудачном выполнении, см. в приведенной ниже таблице.)

Если любой метод Move успешно находит запись, свойствам **BOF** и **EOF** присваивается значение **False**.

Если в рабочей области Microsoft Access вы добавите запись в пустой объект **Recordset**, свойству **BOF** будет присвоено значение **False**, а свойство **EOF** будет по-прежнему иметь значение **True**, указывая на то, что текущая позиция находится в конце объекта **Recordset**.

Любой метод **Delete**, даже если он удаляет единственную оставшуюся запись из объекта **Recordset**, не изменяет значений свойств **BOF** и **EOF**.

В приведенной ниже таблице показано, как методы Move, которым не удалось найти запись, влияют на значения свойств **BOF** и **EOF**.

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
<td><p><strong>True</strong></p></td>
<td><p><strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Без изменений</p></td>
<td><p>Без изменений</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>Без изменений</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</p></td>
<td><p>Без изменений</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>

