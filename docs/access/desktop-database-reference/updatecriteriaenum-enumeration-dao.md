---
title: Переопределение UpdateCriteriaEnum (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e27eb1bdfb9b393df76af8bdf54bc7f05fd82c2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306372"
---
# <a name="updatecriteriaenum-enumeration-dao"></a>Переопределение UpdateCriteriaEnum (DAO)


**Область применения**: Access 2013, Office 2013

Используется с **методом UpdateOptions,** чтобы указать, как строится пакетное обновление.

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
<td><p>dbCriteriaAllCols</p></td>
<td><p>4 </p></td>
<td><p>Использует столбец клавиши (s) и все столбцы в пункте where.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaDeleteInsert</p></td>
<td><p>16 </p></td>
<td><p>Использует пару заявлений DELETE и INSERT для каждой измененной строки.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaKey</p></td>
<td><p>1</p></td>
<td><p>Использует только столбец клавиши (ы) в пункте где.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaModValues</p></td>
<td><p>2</p></td>
<td><p>Использует столбец клавиши (s) и все обновленные столбцы в пункте где.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaTimestamp</p></td>
<td><p>8 </p></td>
<td><p>Использует только столбец timestamp, если это доступно (будет создавать ошибку времени запуска, если столбец timestamp не находится в наборе результатов).</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaUpdate</p></td>
<td><p>32</p></td>
<td><p>Использует заявление UPDATE для каждой измененной строки.</p></td>
</tr>
</tbody>
</table>

