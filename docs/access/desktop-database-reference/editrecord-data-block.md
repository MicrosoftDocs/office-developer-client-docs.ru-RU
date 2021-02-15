---
title: Блок данных EditRecord
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ddfbbf21e62d5967fa1f2f31bab0222664eb39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293597"
---
# <a name="editrecord-data-block"></a>Блок данных EditRecord

**Область применения**: Access 2013, Office 2013

Блок данных **EditRecord можно использовать** для изменения значений, содержащихся в существующей записи.

> [!NOTE]
> Блок **данных EditRecord** доступен только в макросах данных.


## <a name="setting"></a>Setting

Блок **данных EditRecord** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргументация</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Строка, идентифицирует запись, которую необходимо изменить. Если <em>аргумент Alias</em> не указан, то текущая запись будет изменена.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Заметки

После **выполнения команды EditRecord** можно вставить блок команд, которые будут выполняться до того, как будут запятые изменения записи. В блоке данных **EditRecord** доступны следующие действия.

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

Используйте действие **SetField,** чтобы указать новые значения поля в измененной записи.

Вы можете использовать **if... Затем... Заявление Else** для выполнения операций на основе условия.

Чтобы отменить редактирование записи, используйте действие **CancelRecordChange.** Это предотвращает зафиксирование изменений и выход из блока данных **EditRecord.**

Локализованную переменную **LastCreateRecordIdentity** можно использовать для работы с последней записью, созданной в блоке данных **CreateRecord.** Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи:

`[LastCreateRecordIdentity].[AssignedTo]`

Блок данных CreateRecord можно использовать **[](after-insert-macro-event.md)** только в макросах "После вставки", **["После](after-update-macro-event.md)** обновления" и **["После](after-update-macro-event.md)** обновления".

