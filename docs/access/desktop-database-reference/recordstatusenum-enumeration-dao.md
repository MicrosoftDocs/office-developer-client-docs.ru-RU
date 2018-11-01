---
title: RecordStatusEnum Enumeration (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c2d96c359a913660c146f4850a1846554e3b6856
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875121"
---
# <a name="recordstatusenum-enumeration-dao"></a>RecordStatusEnum Enumeration (DAO)


**Применимо к**: Access 2013, Office 2013

Используется совместно со свойством **RecordStatus** для указания состояния обновление текущей записи, если он входит в состав пакета обновления.

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
<td><p>dbRecordDBDeleted</p></td>
<td><p>4</p></td>
<td><p>Запись была удалена, локально и в базе данных.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordDeleted</p></td>
<td><p>3</p></td>
<td><p>Удален, но еще не удалены в базе данных записи.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordModified</p></td>
<td><p>1</p></td>
<td><p>Запись изменения и не обновляются в базе данных.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordNew</p></td>
<td><p>2</p></td>
<td><p>Вставить с помощью метода <strong>AddNew</strong> , но еще не вставлен в базе данных записи.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordUnmodified</p></td>
<td><p>0</p></td>
<td><p>(По умолчанию) Записи не были изменены или успешно обновлены.</p></td>
</tr>
</tbody>
</table>

