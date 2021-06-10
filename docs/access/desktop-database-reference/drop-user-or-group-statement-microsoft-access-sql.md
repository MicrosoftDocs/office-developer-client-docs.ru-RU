---
title: DROP USER или GROUP statement (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293646"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER или GROUP statement (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Удаляет одного или несколько существующих пользователей *или* *групп* или удаляет одного или несколько существующих пользователей *из* существующей *группы.*

## <a name="syntax"></a>Синтаксис

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Удаление одного или более пользователей или удаление одного или более пользователей из группы

DROP *USER user,* \[ *user*, ... \] \[ FROM *group*\]

### <a name="delete-one-or-more-groups"></a>Удаление одной или более групп

ГРУППА  \[ DROP, *группа*, ...\]

В заявлении DROP USER или GROUP есть такие части:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>user</em></p></td>
<td><p>Имя пользователя, удаляемого из информационного файла группы.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Имя группы, удаляемой из информационного файла рабочей группы.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если ключевое слово FROM используется в заявлении  DROP USER, каждый из  пользователей, перечисленных в заявлении, будет удален из группы, указанной по ключевому слову FROM. Однако сами *пользователи* не будут удалены.

В заявлении DROP GROUP будет удалена *указанная группа*(s). Пользователи, которые являются членами группы *(s),* не будут затронуты, но они больше не будут членами *удаленных* групп (s). 

