---
title: CompareEnum (Справочник по для настольных баз данных Access)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd120f726a51c884d063bb03f6d6864ea2d48344
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718898"
---
# <a name="compareenum"></a>CompareEnum

**Применимо к**: Access 2013, Office 2013

Задает относительное положение двух записей, представленное закладок.

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
<td><p>1</p></td>
<td><p>Указывает, что закладки равны.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCompareGreaterThan</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что первая закладка после секунды.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCompareLessThan</strong></p></td>
<td><p>0</p></td>
<td><p>Указывает, что первая закладка перед второй.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCompareNotComparable</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает, что нельзя сравнивать закладки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCompareNotEqual</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает, что закладки не равно и не упорядоченные.</p></td>
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

