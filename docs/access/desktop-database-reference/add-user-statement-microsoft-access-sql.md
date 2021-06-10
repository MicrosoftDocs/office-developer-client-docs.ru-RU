---
title: ADD USER statement (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280427"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ADD USER statement (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Добавляет один или несколько *существующих* пользователей в существующую *группу.*

## <a name="syntax"></a>Синтаксис

ДОБАВИТЬ ПОЛЬЗОВАТЕЛЯ *пользователя,* \[ *пользователя*, ... \] Группа  TO

В заявлении ADD USER есть такие части:

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
<td><p><em>user</em></p></td>
<td><p>Имя пользователя, который будет добавлен в информационный файл группы.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Имя группы, которая будет добавлена в информационный файл рабочей группы.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

После *того как* пользователь был добавлен  в *группу,* у него есть все разрешения, которые были предоставлены *группе.*

