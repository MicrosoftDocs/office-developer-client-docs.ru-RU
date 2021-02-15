---
title: REVOKE statement (Microsoft Access SQL)
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
# <a name="revoke-statement-microsoft-access-sql"></a>REVOKE statement (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Отзывает определенные привилегии у существующего пользователя или группы.

## <a name="syntax"></a>Синтаксис

REVOKE {*privilege,* \[ *privilege*, ... \] } ON {TABLE *table* | Объект  OBJECT|

КОНТЕЙНЕР *CONTAINTER*} FROM {*authorizationname,* \[ *authorizationname*, ... \] }

В заявлении REVOKE есть такие части:

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
<td><p><em>privilege</em></p></td>
<td><p>Привилегии и привилегии, которые необходимо отоиметь. Привилегии заданы с помощью следующих ключевых слов: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA и UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>таблица</em></p></td>
<td><p>Любое допустимые имя таблицы.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Это может охватывать любой объект, не относя какой-либо из таблиц. В качестве примера можно привести сохраненный запрос (представление или процедуру).</p></td>
</tr>
<tr class="even">
<td><p><em>container</em></p></td>
<td><p>Имя допустимого контейнера.</p></td>
</tr>
<tr class="odd">
<td><p><em>authorizationname</em></p></td>
<td><p>Имя пользователя или группы.</p></td>
</tr>
</tbody>
</table>

