---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f9fdf9dd5908b65ae3b6f6ce5a44eba07e4d9bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308808"
---
# <a name="searchdirectionenum"></a>SearchDirectionEnum


**Область применения**: Access 2013, Office 2013

Задает направление поиска записи в [наборе записей](recordset-object-ado.md).

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
<td><p><strong>адсеарчбакквард</strong></p></td>
<td><p>–1</p></td>
<td><p>Выполняет поиск в обратном направлении, останавливается в начале <strong>набора записей</strong>. Если соответствующее значение не найдено, указатель записи располагается по адресу <a href="bof-eof-properties-ado.md">BOF</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>адсеарчфорвард</strong></p></td>
<td><p>1,1</p></td>
<td><p>Выполняет поиск вперед, завершается в конце <strong>набора записей</strong>. Если соответствующее значение не найдено, указатель записи размещается на <a href="bof-eof-properties-ado.md">EOF</a>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Адоенумс. Сеарчдиректион. назад</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Сеарчдиректион. FORWARD</p></td>
</tr>
</tbody>
</table>

