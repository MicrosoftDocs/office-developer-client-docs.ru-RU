---
title: Инструкция ADD USER (Microsoft Access SQL)
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
# <a name="add-user-statement-microsoft-access-sql"></a>Инструкция ADD USER (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Добавляет одного или нескольких существующих *пользователей*s в существующую *группу*.

## <a name="syntax"></a>Синтаксис

Добавить пользователя *user*\[, *пользователя*,... \] Для *группировки*

Оператор ADD USER состоит из следующих частей:

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
</tbody>
</table>


## <a name="remarks"></a>Примечания

После добавления *пользователя* в *группу* *пользователь* получает все разрешения, предоставленные *группе*.

