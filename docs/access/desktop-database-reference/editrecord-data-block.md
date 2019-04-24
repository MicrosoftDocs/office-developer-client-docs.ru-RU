---
title: Блок данных ИзменитьЗапись
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
# <a name="editrecord-data-block"></a>Блок данных ИзменитьЗапись

**Область применения**: Access 2013, Office 2013

Вы можете использовать блок данных **ИзменитьЗапись** , чтобы изменить значения, хранящиеся в существующей записи.

> [!NOTE]
> Блок данных **ИзменитьЗапись** доступен только в макросах данных.


## <a name="setting"></a>Параметр

Блок данных **ИзменитьЗапись** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Строка, определяющая изменяемую запись. Если аргумент <em>Alias</em> не указан, текущая запись редактируется.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Замечания

После оператора **ИзменитьЗапись** вы можете вставить блок команд, который будет выполняться до отправки изменений записи. Следующие действия доступны в блоке данных **ИзменитьЗапись** .

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">Макрокоманда CancelRecordChange</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Оператор макроса Comment</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Оператор макроса Group</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">If... Then... Оператор else макроса</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">Макрокоманда SetField</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда SetLocalVar</a></p></td>
</tr>
</tbody>
</table>

Используйте действие **SetField** для указания новых значений поля в измененной записи.

Можно использовать выражение **If... Then... Else** для выполнения операций на основе условия.

Чтобы отменить редактирование записи, используйте действие **канцелрекордчанже** . Это предотвращает фиксацию изменений и выход из блока данных **ИзменитьЗапись** .

Локальную переменную **ласткреатерекордидентити** можно использовать для работы с последней записью, созданной в блоке данных **СоздатьЗапись** . Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи:

`[LastCreateRecordIdentity].[AssignedTo]`

Блок данных СоздатьЗапись можно использовать только в случаях **[после вставки](after-insert-macro-event.md)**, **[после обновления](after-update-macro-event.md)** и **[после обновления](after-update-macro-event.md)** событий макросов данных.

