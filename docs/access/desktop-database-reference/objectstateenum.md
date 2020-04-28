---
title: Обжектстатинум (Справочник по базам данных Access на компьютере)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288527"
---
# <a name="objectstateenum"></a>ObjectStateEnum

**Область применения**: Access 2013, Office 2013

Указывает, является ли объект открытым или закрытым, подключается к источнику данных, выполняя команду или получая данные.

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
<td><p><strong>адстатеклосед</strong></p></td>
<td><p>нуль</p></td>
<td><p>Указывает, что объект закрыт.</p></td>
</tr>
<tr class="even">
<td><p><strong>адстатеопен</strong></p></td>
<td><p>1,1</p></td>
<td><p>Указывает, что объект открыт.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адстатеконнектинг</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что объект подключается.</p></td>
</tr>
<tr class="even">
<td><p><strong>адстатиксекутинг</strong></p></td>
<td><p>4 </p></td>
<td><p>Указывает, что объект выполняет команду.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адстатефетчинг</strong></p></td>
<td><p>8 </p></td>
<td><p>Указывает, что извлекаются строки объекта.</p></td>
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
<td><p>Адоенумс. Обжектстате. CLOSED</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Обжектстате. OPEN</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Обжектстате. подключение</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Обжектстате. выполнение</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Обжектстате. получение</p></td>
</tr>
</tbody>
</table>

