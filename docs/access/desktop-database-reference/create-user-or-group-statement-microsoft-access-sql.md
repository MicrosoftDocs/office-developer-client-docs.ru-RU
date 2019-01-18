---
title: Создание пользователя или группы оператора (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710925"
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
<td><p><em>пароль</em></p></td>
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

