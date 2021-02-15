---
title: MarshalOptionsEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: MarshalOptionsEnum
ms:assetid: 5361884b-a0fe-c480-1b9f-18e53be77f86
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249272(v=office.15)
ms:contentKeyID: 48544867
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a128f9980bc8c827ddfcb72e738ce5f879be1051
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289730"
---
# <a name="marshaloptionsenum"></a>MarshalOptionsEnum

**Область применения**: Access 2013, Office 2013

Указывает, какие записи должны быть возвращены на сервер.

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
<td><p><strong>adMarshalAll</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Возвращает все строки на сервер.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMarshalModifiedOnly</strong></p></td>
<td><p>1 </p></td>
<td><p>Возвращает на сервер только измененные строки.</p></td>
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
<td><p>AdoEnums.MarshalOptions.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.MarshalOptions.MODIFIEDONLY</p></td>
</tr>
</tbody>
</table>

