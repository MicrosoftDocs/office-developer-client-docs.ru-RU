---
title: Аффектенум (Справочник по базам данных Access на компьютере)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297202"
---
# <a name="affectenum"></a>AffectEnum

**Область применения**: Access 2013, Office 2013

Указывает, какие записи затрагиваются операцией.

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
<td><p><strong>Адаффекталл</strong></p></td>
<td><p>4</p></td>
<td><p>Если к <strong>набору записей</strong>не применен <a href="filter-property-ado.md">Фильтр</a> , затрагивают все записи. Если для свойства <strong>Filter</strong> задано строковое условие (например, &quot;Author = ' Smith '&quot;), операция влияет на видимые записи в текущей главе. Если свойству <strong>Filter</strong> присвоено значение Member объекта <a href="filtergroupenum.md">Филтерграупенум</a> или массива закладок, операция повлияет на все строки <strong>набора записей</strong>.</p><p><strong>Note</strong>: адаффекталл скрыт в обозревателе объектов Visual Basic.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>Адаффекталлчаптерс</strong></p></td>
<td><p>SP4</p></td>
<td><p>Влияет на все записи во всех соседних главах <strong>набора записей</strong>, включая те, которые не видны с помощью <strong>фильтра</strong> , который применяется в данный момент.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адаффекткуррент</strong></p></td>
<td><p>1,1</p></td>
<td><p>Влияет только на текущую запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адаффектграуп</strong></p></td>
<td><p>2</p></td>
<td><p>Влияет только на записи, которые соответствуют текущему значению свойства <a href="filter-property-ado.md">Filter</a> . Для использования этого параметра необходимо задать для свойства <strong>Filter</strong> значение <strong>Филтерграупенум</strong> или массив <strong>закладок</strong> .</p></td>
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
<td><p>Адоенумс. ALL</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. влиял. АЛЛЧАПТЕРС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. влиял. CURRENT</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. влияние. GROUP</p></td>
</tr>
</tbody>
</table>

