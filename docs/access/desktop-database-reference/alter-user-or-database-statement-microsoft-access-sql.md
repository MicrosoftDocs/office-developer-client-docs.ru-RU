---
title: Инструкция ALTER USER или DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297181"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>Инструкция ALTER USER или DATABASE (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Изменяет пароль для существующего пользователя или для базы данных.

## <a name="syntax"></a>Синтаксис

ALTER DATABASE PASSWORD *newPassword олдпассворд*

ИЗМЕНЕНИЕ пароля *пользователя* *newPassword олдпассворд*

Инструкция ALTER USER или DATABASE состоит из следующих частей:

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
<td><p><em>newPassword</em></p></td>
<td><p>Новый пароль, который необходимо связать с указанным именем <em>пользователя</em> или <em>базы данных</em> .</p></td>
</tr>
<tr class="odd">
<td><p><em>олдпассворд</em></p></td>
<td><p>Существующий пароль, который необходимо связать с указанным именем <em>пользователя</em> или <em>группы</em> .</p></td>
</tr>
</tbody>
</table>

