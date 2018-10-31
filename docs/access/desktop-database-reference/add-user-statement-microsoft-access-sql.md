---
title: Добавление пользователя оператора (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 80e3a8fe62cf077accfc18a30e188898fb279d1d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862291"
---
# <a name="add-user-statement-microsoft-access-sql"></a>Добавление пользователя оператора (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Добавление одного или нескольких существующих *пользователей*s существующей *группы*.

## <a name="syntax"></a>Синтаксис

Добавление пользователя *пользователя*\[, *пользователь*... \] В *группу*

Оператор добавить пользователя состоит из следующих частей:

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
</tbody>
</table>


## <a name="remarks"></a>Замечания

После *пользователь* добавлен в *группу*, *пользователь* имеет все разрешения, предоставленные в *группу*.

