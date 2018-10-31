---
title: Создание пользователя или группы оператора (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 391c31240acf33a458895b00335d1600b975e834
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862648"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>Создание пользователя или группы оператора (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Создает один или несколько новых пользователей или групп.

## <a name="syntax"></a>Синтаксис

**Создание пользователя**:

Создание пользователя *пользователя* *пароль pid* \[, *пользователь* *пароль pid*,...\]

**Создание группы**:

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


## <a name="remarks"></a>Замечания

*Пользователей* и *группы* не может содержать таким же именем.

*Пароль* необходим для каждого *пользователя* или *группы* , которая создается.

