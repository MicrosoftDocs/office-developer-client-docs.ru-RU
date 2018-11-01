---
title: Прежде чем удалить макрос события
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0ee4878a742454eb1b02f4b9a45c14ad79097c46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876262"
---
# <a name="before-delete-macro-event"></a>Прежде чем удалить макрос события

**Применимо к**: Access 2013, Office 2013

**Прежде чем удалить** событие происходит при удалении записи, но перед сохранением изменений.

> [!NOTE]
> **Прежде чем удалить** событие доступна только в макросов данных.

## <a name="remarks"></a>Замечания

С помощью события **До удаления** для выполнения действий, которые следует выполнить перед записью удаляется. **До изменения** обычно используется для выполнения проверки и повысить пользовательские сообщения об ошибках.

Можно получить доступ к значение записи, чтобы удалить с помощью следующего синтаксиса:

`[Old].[Field Name]`

Например для доступа к значение поля QuantityInStock в записи для удаления, используйте следующий синтаксис:

`[Old].[QuantityInStock]`

Значения, содержащиеся в записи к удалению удаляется без возможности восстановления при окончания события **До удаления** .

**Прежде чем удалить** событие можно отменить с помощью действия **RaiseError** . Когда возникает ошибка, изменения, содержащиеся в событии **Прежде чем удалять** будут удалены.

В следующей таблице перечислены команды макросов, которые можно использовать в событии **До удаления** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип команды</p></th>
<th><p>Команда</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Выполнение программы</p></td>
<td><p><a href="comment-macro-statement.md">Оператор комментария макросов</a></p></td>
</tr>
<tr class="even">
<td><p>Выполнение программы</p></td>
<td><p><a href="group-macro-statement.md">Оператор группы макросов</a></p></td>
</tr>
<tr class="odd">
<td><p>Выполнение программы</p></td>
<td><p><a href="if-then-else-macro-block.md">If... Затем... Блок else макросов</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="lookuprecord-data-block.md">Действия макрокомандой НайтиЗапись, после макроса</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Действия макроса ClearMacroError</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="onerror-macro-action.md">Действия макроса OnError</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="raiseerror-macro-action.md">Действия макроса RaiseError</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="setlocalvar-macro-action.md">Действия макроса SetLocalVar</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="stopmacro-macro-action.md">Действия ОстановитьМакрос макроса</a></p></td>
</tr>
</tbody>
</table>


Чтобы создать макрос данных, который захватывает событие **Прежде чем удалять** , выполните следующие действия.

1.  Откройте таблицу для записи события **До удаления** .

2.  На вкладке **таблицы** в группе **События перед** выберите **До удаления**.

