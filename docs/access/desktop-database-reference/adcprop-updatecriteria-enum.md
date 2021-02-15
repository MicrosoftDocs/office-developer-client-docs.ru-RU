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
# <a name="adcprop_updatecriteria_enum"></a>ADCPROP \_ UPDATECRITERIA \_ ENUM

**Область применения**: Access 2013, Office 2013

Указывает, какие поля можно использовать для обнаружения конфликтов во время оптимистичного обновления строки источника данных с [объектом Recordset.](recordset-object-ado.md)

Используйте эти константы с динамическим свойством **Recordset** **"Update Criteria"**(Условия обновления), на которое ссылается динамический индекс [свойств ADO](ado-dynamic-property-index.md) и задокументировано в документации microsoft [Cursor Service для OLE DB.](microsoft-cursor-service-for-ole-db-ado-service-component.md)

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
<td><p>1 </p></td>
<td><p>Обнаруживает конфликты, если был изменен какой-либо столбец строки источника данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaKey</strong></p></td>
<td><p>0</p></td>
<td><p>Обнаруживает конфликты, если ключевой столбец строки источника данных был изменен, что означает, что строка была удалена.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCriteriaTimeStamp</strong></p></td>
<td><p>3 </p></td>
<td><p>Обнаруживает конфликты, если была изменена временная запись строки источника данных, то есть доступ к строке был получен после получения <strong>recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaUpdCols</strong></p></td>
<td><p>2 </p></td>
<td><p>Обнаруживает конфликты, если один из столбцов строки источника данных, соответствующий обновленным полям в <strong>наборе записей,</strong> был изменен.</p></td>
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

