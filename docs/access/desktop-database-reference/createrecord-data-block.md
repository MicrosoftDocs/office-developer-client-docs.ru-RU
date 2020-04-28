---
title: Блок данных СоздатьЗапись
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
# <a name="createrecord-data-block"></a>Блок данных СоздатьЗапись


**Область применения**: Access 2013, Office 2013

Вы можете использовать блок данных **СоздатьЗапись** для создания новой записи в указанной таблице.

> [!NOTE]
> Блок данных **СоздатьЗапись** доступен только в макросах данных.

## <a name="setting"></a>Параметр

Блок данных **СоздатьЗапись** имеет следующие аргументы.

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
<td><p><strong>Создание записи в</strong></p></td>
<td><p>Да</p></td>
<td><p>Имя таблицы, в которой создается новая запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>Alias</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строка, определяющая запись. Псевдоним записи можно использовать для определения</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Запись, созданная с помощью **макрокоманды СоздатьЗапись** , автоматически становится текущей записью.

После оператора **СоздатьЗапись** вы можете вставить блок команд, который будет выполняться перед фиксацией новой записи. Следующие действия доступны в блоке данных **СоздатьЗапись** .

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
<td><p><a href="if-then-else-macro-block.md">If... Then... Оператор else макроса</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></p></td>
</tr>
</tbody>
</table>


После того как действие **СоздатьЗапись** создаст запись, используйте действие **SetField** , чтобы указать значение поля в новой записи.

Можно использовать выражение **If... Then... Else** для выполнения операций на основе условия.

Чтобы отменить создание записи, используйте действие **канцелрекордчанже** . Это предотвращает фиксацию изменений и выход из блока данных **СоздатьЗапись** .

После фиксации новой записи можно использовать локальную переменную **ласткреатерекордидентити** для работы с записью. Например, используйте следующий синтаксис, чтобы сослаться на поле AssignedTo недавно созданной записи.

`[LastCreateRecordIdentity].[AssignedTo]`

Блок данных **СоздатьЗапись** можно использовать только в случаях **[после вставки](after-insert-macro-event.md)**, **[после обновления](after-update-macro-event.md)** и **[после обновления](after-update-macro-event.md)** событий макросов данных.

