---
title: CompareEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd120f726a51c884d063bb03f6d6864ea2d48344
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296068"
---
# <a name="compareenum"></a>CompareEnum

**Область применения**: Access 2013, Office 2013

Указывает относительное положение двух записей, представленных закладки.

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
<td><p><strong>adCompareEqual</strong></p></td>
<td><p>1 </p></td>
<td><p>Указывает, что закладки равны.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCompareGreaterThan</strong></p></td>
<td><p>2 </p></td>
<td><p>Указывает, что первая закладка находится после второй.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCompareLessThan</strong></p></td>
<td><p>0</p></td>
<td><p>Указывает, что первая закладка находится перед второй.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCompareNotComparable</strong></p></td>
<td><p>4 </p></td>
<td><p>Указывает, что закладки невозможно сравнить.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCompareNotEqual</strong></p></td>
<td><p>3 </p></td>
<td><p>Указывает, что закладки не равны и не упорядочены.</p></td>
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
<td><p>AdoEnums.Compare.EQUAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Compare.GREATERTHAN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Compare.LESSTHAN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Compare.NOTCOMPARABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Compare.NOTEQUAL</p></td>
</tr>
</tbody>
</table>

