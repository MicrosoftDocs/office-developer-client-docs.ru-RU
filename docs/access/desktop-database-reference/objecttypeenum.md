---
title: ObjectTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c5fb9dbf86823ab4d84327d97eceb037eb77dec0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863724"
---
# <a name="objecttypeenum"></a>ObjectTypeEnum

**Применимо к**: Access 2013 | Office 2013

Указывает тип объекта базы данных, для которого необходимо задать разрешения или владельца.

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
<td><p><strong>adPermObjColumn</strong></p></td>
<td><p>2</p></td>
<td><p>Объект является столбец.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjDatabase</strong></p></td>
<td><p>3</p></td>
<td><p>Объект представляет собой базу данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjProcedure</strong></p></td>
<td><p>4</p></td>
<td><p>Объект не является процедурой.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjProviderSpecific</strong></p></td>
<td><p>-1</p></td>
<td><p>Объект — это тип, определяемый поставщиком. Если параметр <em>ObjectType</em> <strong>adPermObjProviderSpecific</strong> и <em>ObjectTypeId</em> не указан, произойдет ошибка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjTable</strong></p></td>
<td><p>1</p></td>
<td><p>Объект — это таблица.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjView</strong></p></td>
<td><p>5</p></td>
<td><p>Объект — это представление.</p></td>
</tr>
</tbody>
</table>

