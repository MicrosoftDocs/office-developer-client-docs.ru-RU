---
title: Создание пользователя или группы оператора (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 52d376b05c195ed0ea4707e849c5ae395c2b5590
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936828"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>Создание пользователя или группы оператора (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Создает один или несколько новых пользователей или групп.

## <a name="syntax"></a>Синтаксис

### <a name="create-a-user"></a>Создание пользователя

Создание пользователя *пользователя* *пароль pid* \[, *пользователь* *пароль pid*,...\]

### <a name="create-a-group"></a>Создание группы

Создание группы *группы* *pid*\[, *Группа* *pid*...\]

Создание пользователя или группы оператора состоит из следующих частей:

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
<td><p>Имя пользователя для добавления файла рабочей группы.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Имя группы для добавления файла рабочей группы.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Пароль, будет связан с именем указанного <em>пользователя</em> .</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>Личный идентификатор.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

*Пользователей* и *группы* не может содержать таким же именем.

*Пароль* необходим для каждого *пользователя* или *группы* , которая создается.

