---
title: Создание оператора "пользователь" или "Группа" (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295382"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>Создание оператора "пользователь" или "Группа" (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает одного или нескольких новых пользователей или групп.

## <a name="syntax"></a>Синтаксис

### <a name="create-a-user"></a>Создание пользователя

Создайте ** *пароль пользователя PID* \[, пароль *пользователя* *PID*,...\]

### <a name="create-a-group"></a>Создание группы

Создание группы ** *PID*\[, *группы* *PID*,...\]

Инструкция CREATE USER или GROUP состоит из следующих частей:

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
<td><p>Имя пользователя, добавляемого в информационный файл рабочей группы.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Имя группы, которую необходимо добавить в файл сведений о рабочей группе.</p></td>
</tr>
<tr class="odd">
<td><p><em>Ввод</em></p></td>
<td><p>Пароль, который необходимо связать с указанным именем <em>пользователя</em> .</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>Личный идентификатор.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Имя *пользователя* и *группы* не могут совпадать.

Для каждого создаваемого *пользователя* или *группы* необходим *пароль* .

