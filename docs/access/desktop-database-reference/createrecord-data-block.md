---
title: Блок данных CreateRecord
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295354"
---
# <a name="createrecord-data-block"></a>Блок данных CreateRecord


**Область применения**: Access 2013, Office 2013

Блок данных **CreateRecord можно использовать** для создания новой записи в указанной таблице.

> [!NOTE]
> Блок **данных CreateRecord** доступен только в макросах данных.

## <a name="setting"></a>Setting

Блок **данных CreateRecord** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Создание записи</strong></p></td>
<td><p>Да</p></td>
<td><p>Имя таблицы для создания новой записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>Alias</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строка, идентифицирует запись. Псевдоним записи можно использовать для идентификации</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Запись, созданная **с помощью CreateRecord,** автоматически становится текущей записью.

После **записи CreateRecord** можно вставить блок команд, которые будут выполняться до того, как будет зафиксирована новая запись. В блоке данных **CreateRecord** доступны следующие действия.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">Макрокоманда "ОтменитьИзменениеЗаписи"</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Оператор макроса "Группа"</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">If... Затем... Макрос Else</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></p></td>
</tr>
</tbody>
</table>


После создания записи с помощью действия **CreateRecord** используйте действие **SetField,** чтобы указать значение поля в новой записи.

Вы можете использовать **if... Затем... Заявление Else** для выполнения операций на основе условия.

Чтобы отменить создание записи, используйте действие **CancelRecordChange.** Это предотвращает внесение изменений и выход из блока **данных CreateRecord.**

После записи можно использовать локализованную переменную **LastCreateRecordIdentity** для работы с записью. Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи.

`[LastCreateRecordIdentity].[AssignedTo]`

Блок **данных CreateRecord** можно использовать только в макросах "После вставки", **[](after-insert-macro-event.md)** **["После](after-update-macro-event.md)** обновления" и **["После](after-update-macro-event.md)** обновления".

