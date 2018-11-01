---
title: Блок данных EditRecord
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c4d5a5a1565aeda41e5a52127e9f82b5304e686
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876885"
---
# <a name="editrecord-data-block"></a>Блок данных EditRecord

**Применимо к**: Access 2013, Office 2013

Чтобы изменить значения, содержащиеся в существующей записи можно использовать блок данных **ИзменитьЗапись** .

> [!NOTE]
> Блок данных **ИзменитьЗапись** доступна только в макросов данных.


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
<td><p>Строка, идентифицирующая записи для редактирования. Если аргумент <em>псевдоним</em> не задан, изменяется текущей записи.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Замечания

После оператора **ИзменитьЗапись** можно вставить блок команды, которые будут выполняться перед comitted изменений в запись. В блоке данных **ИзменитьЗапись** доступны следующие действия.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">Действия макроса CancelRecordChange</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Оператор комментария макросов</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Оператор группы макросов</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">If... Затем... Оператор Else макросов</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">Действия SetField макроса</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">Действия макроса SetLocalVar</a></p></td>
</tr>
</tbody>
</table>

Действие **SetField** используется для указания нового значения поля в измененной записи.

**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия.

Чтобы отменить редактирование записи, используйте действие **CancelRecordChange** . Это предотвращает фиксации изменений и выполняет выход из блока данных **ИзменитьЗапись** .

Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** . Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи:

`[LastCreateRecordIdentity].[AssignedTo]`

Блок данных СоздатьЗапись можно использовать только **[После вставки](after-insert-macro-event.md)**, **[После обновления](after-update-macro-event.md)** и событий макрос данных **[После обновления](after-update-macro-event.md)** .

