---
title: Алловнуллсенум (Справочник по базам данных Access на компьютере)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c184253551fa3f974de1840d47654af597881cb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297168"
---
# <a name="allownullsenum"></a>AllowNullsEnum

**Область применения**: Access 2013, Office 2013

Указывает, индексируются ли записи со значениями NULL.

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
<td><p><strong>адиндекснуллсаллов</strong></p></td>
<td><p>нуль</p></td>
<td><p>В индексе разрешены записи с ключевыми столбцами null. Если в ключевом столбце введено значение null, запись вставляется в индекс.</p></td>
</tr>
<tr class="even">
<td><p><strong>адиндекснуллсдисаллов</strong></p></td>
<td><p>1,1</p></td>
<td><p>Значение, используемое по умолчанию. В индексе не допускаются записи с ключевыми столбцами null. Если в ключевом столбце введено значение null, возникнет ошибка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адиндекснуллсигноре</strong></p></td>
<td><p>2</p></td>
<td><p>Индекс не вставляет записи, содержащие ключи null. Если в ключевом столбце введено значение null, то запись игнорируется и ошибка не возникает.</p></td>
</tr>
<tr class="even">
<td><p><strong>адиндекснуллсигнореани</strong></p></td>
<td><p>4 </p></td>
<td><p>Индекс не вставляет записи, в которых некоторый ключевой столбец имеет значение null. Если в индексе используется ключ с несколькими столбцами, то при вводе значения NULL в некоторый столбец Эта запись игнорируется, а ошибка не возникает.</p></td>
</tr>
</tbody>
</table>

