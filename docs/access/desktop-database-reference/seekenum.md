---
title: Сикенум (Справочник по базам данных Access на компьютере)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314660"
---
# <a name="seekenum"></a>SeekEnum

**Область применения**: Access 2013, Office 2013

Указывает тип выполняемого [поиска](seek-method-ado.md) .

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
<td><p>адсикфирстек</p></td>
<td><p>1,1</p></td>
<td><p>Ищет первый ключ, равный <em>кэйвалуес</em>.</p></td>
</tr>
<tr class="even">
<td><p>адсикластек</p></td>
<td><p>2</p></td>
<td><p>Ищет последний ключ, равный <em>кэйвалуес</em>.</p></td>
</tr>
<tr class="odd">
<td><p>адсикафтерек</p></td>
<td><p>4 </p></td>
<td><p>Ищет ключ, равный <em>кэйвалуес</em> , или сразу после того, как будет выполнено совпадение.</p></td>
</tr>
<tr class="even">
<td><p>адсикафтер</p></td>
<td><p>8 </p></td>
<td><p>Ищет ключ сразу после того места, где произошло сравнение с <em>кэйвалуес</em> .</p></td>
</tr>
<tr class="odd">
<td><p>адсикбефорик</p></td>
<td><p>16 </p></td>
<td><p>Ищет ключ, равный <em>кэйвалуес</em> , или только до того места, где будет выполнено это совпадение.</p></td>
</tr>
<tr class="even">
<td><p>адсикбефоре</p></td>
<td><p>32</p></td>
<td><p>Ищет ключ до того места, где было бы обнаружено сравнение с <em>кэйвалуес</em> .</p></td>
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
<td><p>Адоенумс. Seek. ФИРСТЕК</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Seek. ЛАСТЕК</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Seek. АФТЕРЕК</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Seek. AFTER</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Seek. БЕФОРИК</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Seek. BEFORE</p></td>
</tr>
</tbody>
</table>

