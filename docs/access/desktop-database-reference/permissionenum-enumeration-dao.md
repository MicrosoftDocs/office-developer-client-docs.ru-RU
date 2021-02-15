---
title: Enumeration PermissionEnum (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d4f6741bd6203dbdeffb364650b5e3550ea8b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287712"
---
# <a name="permissionenum-enumeration-dao"></a>Enumeration PermissionEnum (DAO)


**Область применения**: Access 2013, Office 2013

Используется со **свойством Permissions** для указания типа разрешений.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbSecCreate</p></td>
<td><p>1 </p></td>
<td><p>Пользователь может создавать новые документы (не допустимые для объектов Document).</p></td>
</tr>
<tr class="even">
<td><p>dbSecDBAdmin</p></td>
<td><p>8 </p></td>
<td><p>Пользователь может реплицировать базу данных и изменить пароль базы данных (не является допустимым для объектов Document).</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBCreate</p></td>
<td><p>1 </p></td>
<td><p>Пользователь может создавать новые базы данных. Этот параметр действителен только для контейнера Databases в файле сведений о группе (Systen.mdw). Эта константа не является допустимой для объектов Document.</p></td>
</tr>
<tr class="even">
<td><p>dbSecDBExclusive</p></td>
<td><p>4 </p></td>
<td><p>Пользователь имеет монопольный доступ к базе данных.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBOpen</p></td>
<td><p>2 </p></td>
<td><p>Пользователь может открыть базу данных.</p></td>
</tr>
<tr class="even">
<td><p>dbSecDelete</p></td>
<td><p>65536</p></td>
<td><p>Пользователь может удалить объект.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDeleteData</p></td>
<td><p>128</p></td>
<td><p>Пользователь может удалить записи.</p></td>
</tr>
<tr class="even">
<td><p>dbSecFullAccess</p></td>
<td><p>1048575</p></td>
<td><p>Пользователь имеет полный доступ к объекту.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecInsertData</p></td>
<td><p>32</p></td>
<td><p>Пользователь может добавлять записи.</p></td>
</tr>
<tr class="even">
<td><p>dbSecNoAccess</p></td>
<td><p>0</p></td>
<td><p>Пользователь не имеет доступа к объекту (не является допустимым для объектов Document).</p></td>
</tr>
<tr class="odd">
<td><p>dbSecReadDef</p></td>
<td><p>4 </p></td>
<td><p>Пользователь может прочитать определение таблицы, включая сведения о столбцах и индексах.</p></td>
</tr>
<tr class="even">
<td><p>dbSecReadSec</p></td>
<td><p>131072</p></td>
<td><p>Пользователь может прочитать сведения, связанные с безопасностью объекта.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecReplaceData</p></td>
<td><p>64</p></td>
<td><p>Пользователь может изменять записи.</p></td>
</tr>
<tr class="even">
<td><p>dbSecRetrieveData</p></td>
<td><p>20</p></td>
<td><p>Пользователь может получить данные из объекта Document.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecWriteDef</p></td>
<td><p>65548</p></td>
<td><p>Пользователь может изменять или удалять определение таблицы, включая сведения о столбцах и индексах.</p></td>
</tr>
<tr class="even">
<td><p>dbSecWriteOwner</p></td>
<td><p>524288</p></td>
<td><p>Пользователь может изменить параметр свойства Owner.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecWriteSec</p></td>
<td><p>262144</p></td>
<td><p>Пользователь может изменять разрешения на доступ.</p></td>
</tr>
</tbody>
</table>

