---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8be93b0b7e4b32e3c040e871ff7d97a95f1e247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282854"
---
# <a name="adcprop_updatecriteria_enum"></a>Перечисление АДКПРОП\_упдатекритериа\_

**Область применения**: Access 2013, Office 2013

Указывает, какие поля можно использовать для обнаружения конфликтов во время оптимистического обновления строки источника данных с помощью объекта [Recordset](recordset-object-ado.md) .

Используйте эти константы с динамическим свойством **Recordset** "**критерии обновления**", на который ссылается [индекс динамического свойства ADO](ado-dynamic-property-index.md) и задокументированы в документации [службы курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) .

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
<td><p><strong>адкритериааллколс</strong></p></td>
<td><p>1,1</p></td>
<td><p>Обнаруживает конфликты при изменении любого столбца строки источника данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>адкритериакэй</strong></p></td>
<td><p>нуль</p></td>
<td><p>Обнаруживает конфликты, если ключевой столбец строки источника данных изменился, что означает, что строка была удалена.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адкритериатиместамп</strong></p></td>
<td><p>4</p></td>
<td><p>Обнаруживает конфликты, если отметка времени строки источника данных была изменена, то есть доступ к строке выполнялся после получения <strong>набора записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>адкритериаупдколс</strong></p></td>
<td><p>2</p></td>
<td><p>Обнаруживает конфликты при изменении одного из столбцов строки источника данных, соответствующих обновленным полям <strong>набора записей</strong> .</p></td>
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
<td><p>Адоенумс. Адкпропупдатекритериа. АЛЛКОЛС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Адкпропупдатекритериа. KEY</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Адкпропупдатекритериа. TIMESTAMP</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Адкпропупдатекритериа. УПДКОЛС</p></td>
</tr>
</tbody>
</table>

