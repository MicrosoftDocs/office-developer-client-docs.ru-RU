---
title: RightsEnum (Ссылка на настольные базы данных)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306491"
---
# <a name="rightsenum"></a>RightsEnum

**Область применения**: Access 2013, Office 2013

Указывает права или разрешения для группы или пользователя объекта.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adRightCreate</strong></p></td>
<td><p>16384<br />
( &amp; H4000)</p></td>
<td><p>Пользователь или группа имеет разрешение на создание новых объектов этого типа.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightDelete</strong></p></td>
<td><p>65536<br />
( &amp; H10000)</p></td>
<td><p>Пользователь или группа имеет разрешение на удаление данных с объекта. Для таких объектов, как <strong>Таблицы,</strong>у пользователя есть разрешение на удаление значений данных из записей.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightDrop</strong></p></td>
<td><p>256<br />
( &amp; H100)</p></td>
<td><p>Пользователь или группа имеет разрешение на удаление объектов из каталога. Например, <strong>таблицы</strong> могут быть удалены командой DROP TABLE SQL.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightExclusive</strong></p></td>
<td><p>512<br />
( &amp; H200)</p></td>
<td><p>Пользователь или группа имеют разрешение на доступ к объекту исключительно.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightExecute</strong></p></td>
<td><p>536870912<br />
( &amp; H20000000)</p></td>
<td><p>Пользователь или группа имеет разрешение на выполнение объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightFull</strong></p></td>
<td><p>268435456<br />
( &amp; H10000000)</p></td>
<td><p>У пользователя или группы есть все разрешения на объекте.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightInsert</strong></p></td>
<td><p>32768<br />
( &amp; H8000)</p></td>
<td><p>Пользователь или группа имеет разрешение на вставку объекта. Для таких объектов, как <strong>Таблицы,</strong>у пользователя есть разрешение на вставку данных в таблицу.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightMaximumAllowed</strong></p></td>
<td><p>33554432 &amp; (H2000000)</p></td>
<td><p>У пользователя или группы максимальное количество разрешений, разрешенных поставщиком. Определенные разрешения зависят от поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightNone</strong></p></td>
<td><p>0</p></td>
<td><p>У пользователя или группы нет разрешений для объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightRead</strong></p></td>
<td><p>-2147483648<br />
( &amp; H80000000)</p></td>
<td><p>Пользователь или группа имеет разрешение на чтение объекта. Для таких объектов, как <a href="table-object-adox.md">Таблицы,</a>пользователь имеет разрешение на чтение данных в таблице.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReadDesign</strong></p></td>
<td><p>1024<br />
( &amp; H400)</p></td>
<td><p>Пользователь или группа имеет разрешение на чтение дизайна объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightReadPermissions</strong></p></td>
<td><p>131072<br />
( &amp; H20000)</p></td>
<td><p>Пользователь или группа могут просматривать, но не изменять конкретные разрешения для объекта в каталоге.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReference</strong></p></td>
<td><p>8192<br />
( &amp; H2000)</p></td>
<td><p>Пользователь или группа могут ссылаться на объект.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightUpdate</strong></p></td>
<td><p>1073741824<br />
( &amp; H40000000)</p></td>
<td><p>Пользователь или группа имеет разрешение на обновление объекта. Для таких объектов, как <strong>Таблицы,</strong>у пользователя есть разрешение на обновление данных в таблице.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWithGrant</strong></p></td>
<td><p>4096<br />
( &amp; H1000)</p></td>
<td><p>Пользователь или группа имеет разрешение на выдачу разрешений на объект.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWriteDesign</strong></p></td>
<td><p>2048<br />
( &amp; H800)</p></td>
<td><p>Пользователь или группа имеет разрешение на изменение дизайна объекта.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWriteOwner</strong></p></td>
<td><p>524288<br />
( &amp; H80000)</p></td>
<td><p>Пользователь или группа имеет разрешение на изменение владельца объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWritePermissions</strong></p></td>
<td><p>262144<br />
( &amp; H40000)</p></td>
<td><p>Пользователь или группа могут изменять определенные разрешения для объекта в каталоге.</p></td>
</tr>
</tbody>
</table>

