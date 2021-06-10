---
title: Заявление GRANT (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292134"
---
# <a name="grant-statement-microsoft-access-sql"></a>Заявление GRANT (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Предоставляет определенные привилегии существующему пользователю или группе.

## <a name="syntax"></a>Синтаксис

GRANT *{privilege* \[ , *privilege*, ... \] } ТАБЛИЦА ON{TABLE *|* *ОБЪЕКТ-объект*|

КОНТЕЙНЕР *контейнера* } TO {*имя авторизации,* \[ имя *авторизации*, ... \] }

В заявлении GRANT есть такие части:

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
<td><p><em>привилегия</em></p></td>
<td><p>Привилегии или привилегии, которые должны быть предоставлены. Привилегии заданы с помощью следующих ключевых слов: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA и UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>имя таблицы</em></p></td>
<td><p>Любое допустимые имя таблицы.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Это может охватывать любой объект без таблицы. Одним из примеров является сохраненный запрос (представление или процедура).</p></td>
</tr>
<tr class="even">
<td><p><em>контейнер</em></p></td>
<td><p>Имя допустимого контейнера.</p></td>
</tr>
<tr class="odd">
<td><p><em>имя авторизации</em></p></td>
<td><p>Имя пользователя или группы.</p></td>
</tr>
</tbody>
</table>

