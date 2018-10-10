---
title: DROP USER or GROUP Statement (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480287"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER or GROUP Statement (Microsoft Access SQL)


**Применимо к**: Access 2013 | Office 2013

Удаляет один или несколько существующего *пользователя*или *группы*, или удаляет существующие s *пользователей*из существующей *группы*.

## <a name="syntax"></a>Синтаксис

Удаление одного или нескольких *пользователей*s или удалить один или несколько s *пользователя*из *группы*:

Удаление пользователя *пользователя*\[, *пользователь*... \] \[Из *группы*\]

Удаление одного или нескольких s: *группы*

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


## <a name="remarks"></a>Замечания

При использовании этого ключевого слова в инструкции DROP USER каждого из s *пользователей*, перечисленных в инструкции будет удален из *группы* указанной после этого ключевого слова. Тем не менее *Пользователи*сами не будут удалены.

Инструкция DROP GROUP удаляет указанный *группы*(s). S *пользователей*, которые входят в *группу*(s) не удаляются, но они больше не входят удаленные *группы*(s).

