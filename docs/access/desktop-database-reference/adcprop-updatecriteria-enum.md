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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704310"
---
# <a name="adcpropupdatecriteriaenum"></a>ADCPROP\_UPDATECRITERIA\_ENUM

**Применимо к**: Access 2013, Office 2013

Задает поля, которые можно использовать для определения конфликтов при обновлении оптимистичный строки из источника данных с помощью объекта [набора записей](recordset-object-ado.md) .

Используйте эти константы со свойством динамических «**Условию обновления**» **набора записей** , который по ссылке в [ADO динамических свойство индекса](ado-dynamic-property-index.md) и описаны в документации по [Microsoft служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) .

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
<td><p><strong>adCriteriaAllCols</strong></p></td>
<td><p>1</p></td>
<td><p>Обнаруживает конфликтов при изменении любого столбца строки источника данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaKey</strong></p></td>
<td><p>0</p></td>
<td><p>Обнаружение конфликтов Если ключевого столбца данных источника строки был изменен, что означает, что строка была удалена.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCriteriaTimeStamp</strong></p></td>
<td><p>3</p></td>
<td><p>Обнаружение конфликтов, если метка времени данных источника строки был изменен, что означает, что строка осуществлялся после получения <strong>набора записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaUpdCols</strong></p></td>
<td><p>2</p></td>
<td><p>Обнаруживает конфликты, если столбцы строки источника данных, которые соответствуют обновляться полям <strong>набора записей</strong> были изменены.</p></td>
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
<td><p>AdoEnums.AdcPropUpdateCriteria.ALLCOLS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropUpdateCriteria.KEY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropUpdateCriteria.UPDCOLS</p></td>
</tr>
</tbody>
</table>

