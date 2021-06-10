---
title: СОЗДАНИЕ пользовательского или ГРУППОВОГО заявления (Microsoft Access SQL)
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
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>СОЗДАНИЕ пользовательского или ГРУППОВОГО заявления (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает одного или несколько новых пользователей или групп.

## <a name="syntax"></a>Синтаксис

### <a name="create-a-user"></a>Создание пользователя

CREATE USER *user* *password pid* \[ , *user* *password pid*, ...\]

### <a name="create-a-group"></a>Создание группы

CREATE GROUP *group* *pid,* \[ *group* *pid*, ...\]

В заявлении CREATE USER или GROUP есть такие части:

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
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Пароль, связанный с указанным <em>именем</em> пользователя.</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>Личный id.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Пользователь *и* группа *не* могут иметь одно и то же имя.

Для *каждого* созданного  пользователя  или группы требуется пароль.

