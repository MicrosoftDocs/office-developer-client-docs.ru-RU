---
title: Заявление REVOKE (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306533"
---
# <a name="revoke-statement-microsoft-access-sql"></a>Заявление REVOKE (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Отменяет определенные привилегии от существующего пользователя или группы.

## <a name="syntax"></a>Синтаксис

REVOKE {*привилегии* \[ , *привилегии*, ... \] } ON {TABLE *table* | *ОБЪЕКТ-объект*|

КОНТЕЙНЕР *CONTAINTER*} FROM *{authorizationname,* \[ *authorizationname*, ... \] }

В заявлении REVOKE есть такие части:

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
<td><p>Привилегии или привилегии, которые необходимо отозвали. Привилегии заданы с помощью следующих ключевых слов: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA и UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>таблица</em></p></td>
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

