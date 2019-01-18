---
title: Оператор ALTER пользователя или базы данных (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702287"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>Оператор ALTER пользователя или базы данных (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Изменение пароля для существующего пользователя или для базы данных.

## <a name="syntax"></a>Синтаксис

Изменение ПАРОЛЯ базы данных *старый_пароль новый_пароль*

ПАРОЛЬ *пользователя* ALTER пользователя *старый_пароль новый_пароль*

Оператор ALTER пользователя или базы данных состоит из следующих частей:

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
<td><p><em>новый_пароль</em></p></td>
<td><p>Новый пароль, который необходимо связать с указанным именем <em>пользователя</em> или <em>базы данных</em> .</p></td>
</tr>
<tr class="odd">
<td><p><em>старый_пароль</em></p></td>
<td><p>Существующий пароль следует связать с указанным именем <em>пользователя</em> или <em>группы</em> .</p></td>
</tr>
</tbody>
</table>

