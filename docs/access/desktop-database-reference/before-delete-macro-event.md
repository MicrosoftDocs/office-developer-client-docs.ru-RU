---
title: Событие макроса Before Delete
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296915"
---
# <a name="before-delete-macro-event"></a>Событие макроса Before Delete

**Область применения**: Access 2013, Office 2013

Событие **before Delete** происходит при удалении записи, но до внося изменения.

> [!NOTE]
> Событие **Before Delete** доступно только в макросах данных.

## <a name="remarks"></a>Заметки

Используйте событие **Before Delete** для выполнения любых действий, которые необходимо выполнить перед удалением записи. Обычно **перед изменением** выполняется проверка и вызываются пользовательские сообщения об ошибках.

Для доступа к значению записи, которая будет удалена, используется следующий синтаксис:

`[Old].[Field Name]`

Например, чтобы получить доступ к значению поля QuantityIn Разнесен в удаляемой записи, используйте следующий синтаксис:

`[Old].[QuantityInStock]`

Значения, содержащиеся в удаляемой записи, удаляются окончательно после окончания события **"До** удаления".

Вы можете отменить событие **Before Delete** с помощью **действия RaiseError.** При ошибке изменения, содержащиеся в событии **Before Delete,** удаляются.

В следующей таблице перечислены команды макроса, которые можно использовать в событии **Before Delete.**

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
<td><p>Управление</p></td>
<td><p><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></p></td>
</tr>
<tr class="even">
<td><p>Управление</p></td>
<td><p><a href="group-macro-statement.md">Оператор макроса "Группа"</a></p></td>
</tr>
<tr class="odd">
<td><p>Управление</p></td>
<td><p><a href="if-then-else-macro-block.md">Макроблок Если... То... Иначе</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="lookuprecord-data-block.md">Макрокод LookupRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></p></td>
</tr>
</tbody>
</table>


Чтобы создать макрос data, который захватывает событие **Before Delete,** используйте следующие действия.

1.  Откройте таблицу, для которой необходимо зафиксировать событие **Before Delete.**

2.  На **вкладке "Таблица"** в группе **"События** до" выберите **"Перед удалением".**

