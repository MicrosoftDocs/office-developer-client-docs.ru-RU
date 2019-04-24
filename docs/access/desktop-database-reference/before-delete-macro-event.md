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

Событие **перед удалением** возникает при удалении записи, но до фиксации изменения.

> [!NOTE]
> Событие " **перед удалением** " доступно только в макросах данных.

## <a name="remarks"></a>Замечания

Используйте событие **перед удалением** для выполнения действий, которые должны выполняться перед удалением записи. Для выполнения проверки и порождения настраиваемых сообщений об ошибках обычно используется значение **Before Change** .

Можно получить доступ к значению в записи, которую необходимо удалить, используя следующий синтаксис:

`[Old].[Field Name]`

Например, чтобы получить доступ к значению поля Куантитинстокк в удаляемой записи, используйте следующий синтаксис:

`[Old].[QuantityInStock]`

Значения, которые хранятся в удаляемой записи, удаляются навсегда при завершении события **перед удалением** .

Вы можете отменить событие " **перед удалением** " с помощью действия **раисиррор** . При возникновении ошибки изменения, которые включены в событие **before delete** , отбрасываются.

В следующей таблице перечислены команды макросов, которые можно использовать в событии **перед удалением** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип команды</p></th>
<th><p>Command</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Program Flow</p></td>
<td><p><a href="comment-macro-statement.md">Оператор макроса Comment</a></p></td>
</tr>
<tr class="even">
<td><p>Program Flow</p></td>
<td><p><a href="group-macro-statement.md">Оператор макроса Group</a></p></td>
</tr>
<tr class="odd">
<td><p>Program Flow</p></td>
<td><p><a href="if-then-else-macro-block.md">Блок макросов If...Then...Else</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="lookuprecord-data-block.md">Макрокоманда LookupRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Макрокоманда ClearMacroError</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="onerror-macro-action.md">Макрокоманда OnError</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="raiseerror-macro-action.md">Макрокоманда RaiseError</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда SetLocalVar</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="stopmacro-macro-action.md">Макрокоманда StopMacro</a></p></td>
</tr>
</tbody>
</table>


Чтобы создать макрос данных, захватывающий событие **перед удалением** , выполните указанные ниже действия.

1.  Откройте таблицу, для которой необходимо записать событие **перед удалением** .

2.  На вкладке **Таблица** в группе **события перед** удалением выберите **перед удалением**.

