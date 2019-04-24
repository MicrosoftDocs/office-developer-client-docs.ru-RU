---
title: Рекордтипинум (Справочник по базам данных Access на компьютере)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c95e4b78a3e2259c3dc5961e87b98ca65ea55692
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309285"
---
# <a name="recordtypeenum"></a>RecordTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает тип объекта [Record](record-object-ado.md) .

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
<td><p><strong>Адсимплерекорд</strong></p></td>
<td><p>нуль</p></td>
<td><p>Показывает <em>простую</em> запись (не содержит дочерние узлы).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адколлектионрекорд</strong></p></td>
<td><p>1,1</p></td>
<td><p>Указывает запись <em>коллекции</em> (содержит дочерние узлы).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрекордункновн</strong></p></td>
<td><p>–1</p></td>
<td><p>Указывает, что тип этой <strong>записи</strong> неизвестен.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адструктдок</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает запись <em>коллекции</em> особого типа, которая представляет структурированные документы com.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

