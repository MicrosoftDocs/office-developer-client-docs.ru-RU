---
title: AffectEnum (Справочник по для настольных баз данных Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720585"
---
# <a name="affectenum"></a>AffectEnum

**Применимо к**: Access 2013, Office 2013

Указывает, какие записи, влияют операции.

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
<td><p><strong>adAffectAll</strong></p></td>
<td><p>3</p></td>
<td><p>Если не применен <a href="filter-property-ado.md">Фильтр</a> для <strong>записей</strong>, влияет на все записи. Если свойство <strong>фильтра</strong> имеет значение условий строки (например, &quot;автор = «Smith»&quot;), операцию влияет на видимых записей в текущем. Если свойство <strong>фильтра</strong> должна быть членом <a href="filtergroupenum.md">FilterGroupEnum</a> или массив закладки, операция повлияет на все строки из <strong>набора записей</strong>.</p><p><strong>Примечание</strong>: adAffectAll скрыто в обозревателе объектов Visual Basic.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4</p></td>
<td><p>Влияет на все записи в все родственные главы набора <strong>записей</strong>, включая те, которые не видны с помощью любого <strong>фильтра</strong> , применяемого в настоящее время.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1</p></td>
<td><p>Влияет только текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>Влияет только записи, которые удовлетворяют текущего значения свойства <a href="filter-property-ado.md">фильтра</a> . Значение <strong>FilterGroupEnum</strong> или массив <strong>закладки</strong> , чтобы использовать этот параметр, необходимо установить свойство <strong>фильтра</strong> .</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

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
<td><p>AdoEnums.Affect.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.ALLCHAPTERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Affect.CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.GROUP</p></td>
</tr>
</tbody>
</table>

