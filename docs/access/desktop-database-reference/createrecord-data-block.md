---
title: CreateRecord Data Block
TOCTitle: CreateRecord Data Block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62c6902cc57c210d617b71da3ca42a2a52bdd4f6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481228"
---
# <a name="createrecord-data-block"></a>CreateRecord Data Block


**Применимо к**: Access 2013 | Office 2013

Блок данных **СоздатьЗапись** можно использовать для создания новой записи в указанную таблицу.

> [!NOTE]
> Блок данных **СоздатьЗапись** доступна только в макросов данных.

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
<th><p>Argument</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Создание записи в</strong></p></td>
<td><p>Да</p></td>
<td><p>Имя таблицы для создания новой записи в.</p></td>
</tr>
<tr class="even">
<td><p><strong>Alias</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строка, идентифицирующая эту запись. Можно использовать эту запись псевдонима для идентификации</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Записи, созданной **СоздатьЗапись** автоматически становится текущей.

После оператора **СоздатьЗапись** можно вставить блок команды, которые будут выполняться перед сохранением новую запись. В блоке данных **СоздатьЗапись** доступны следующие действия.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Comment Macro Statement</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Group Macro Statement</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">If... Затем... Оператор Else макросов</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">SetField Macro Action</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></p></td>
</tr>
</tbody>
</table>


После **СоздатьЗапись** действие создает запись, используйте действие **SetField** для указания значения поля в новую запись.

**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия.

Чтобы отменить создание записи, используйте действие **CancelRecordChange** . Это предотвращает фиксации изменений и выполняет выход из блока **СоздатьЗапись** данных.

После фиксации новую запись локальной переменной **LastCreateRecordIdentity** можно использовать для работы с записью. Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи.

`[LastCreateRecordIdentity].[AssignedTo]`

Блок данных **СоздатьЗапись** можно использовать только **[После вставки](after-insert-macro-event.md)**, **[После обновления](after-update-macro-event.md)** и событий макрос данных **[После обновления](after-update-macro-event.md)** .
