---
title: Удаление пользователя или группы оператора (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f9662c4f0cb691136a556faa32cb0d5a1c775268
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936835"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>Удаление пользователя или группы оператора (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Удаляет один или несколько существующих *пользователей* или *групп*, или удаляет одного или нескольких существующих *пользователей* из существующей *группы*.

## <a name="syntax"></a>Синтаксис

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Удаление одного или нескольких пользователей или удалить один или несколько пользователей из группы

Удаление пользователя *пользователя*\[, *пользователь*... \] \[Из *группы*\]

### <a name="delete-one-or-more-groups"></a>Удаление одного или нескольких групп

ГРУППА РАЗМЕЩЕНИЯ *группы*\[, *Группа*...\]

Оператор удаление пользователя или группы состоит из следующих частей:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>user</em></p></td>
<td><p>Имя пользователя для удаления из файла рабочей группы.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Имя группы для удаления из файла рабочей группы.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

При использовании этого ключевого слова в инструкции DROP USER каждого из *пользователей* , перечисленных в инструкции будет удален из *группы* указанной после этого ключевого слова. Тем не менее, *Пользователи* сами не будут удалены.

Инструкция DROP GROUP удаляет указанный *группы*(s). *Пользователи* , которые входят в *группу*(s) не удаляются, но они больше не входят удаленные *группы*(s).

