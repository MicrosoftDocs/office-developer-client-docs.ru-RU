---
title: CREATE USER or GROUP Statement (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dce5b9a6894eb1e09a0307b389207baefae6aa58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481996"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>CREATE USER or GROUP Statement (Microsoft Access SQL)


**Применимо к**: Access 2013 | Office 2013

Создает один или несколько новых пользователей или групп.

## <a name="syntax"></a>Синтаксис

Создание пользователя:

Создание пользователя *пользователя* *пароль pid* \[, *пользователь* *пароль pid*,...\]

Создание группы:

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

