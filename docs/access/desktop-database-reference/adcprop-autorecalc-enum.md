---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e385df5029238106b51aa62949d5e4e94f065657
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280524"
---
# <a name="adcpropautorecalcenum"></a>Перечисление АДКПРОП\_ауторекалк\_

**Область применения**: Access 2013, Office 2013

Указывает, когда поставщик [мсдаташапе](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) выполняет повторное вычисление статистических и вычисляемых столбцов в иерархическом наборе записей.

Эти константы используются только с поставщиком **мсдаташапе** и динамическим свойством **Recordset** "**Auto пересчет**", на который ссылается [индекс динамического свойства ADO](ado-dynamic-property-index.md) и задокументированы в [службе курсора Майкрософт для OLE ](microsoft-cursor-service-for-ole-db-ado-service-component.md)Документация по базе [данных или службе формирования данных Майкрософт для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .

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
<td><p><strong>Адрекалкалвайс</strong></p></td>
<td><p>1,1</p></td>
<td><p>Значение, используемое по умолчанию. Пересчитывается всякий раз, когда поставщик <strong>мсдаташапе</strong> определяет значения, от которых зависит изменение вычисляемых столбцов.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрекалкупфронт</strong></p></td>
<td><p>нуль</p></td>
<td><p>Вычисляется только при первоначальном построении иерархического <strong>набора записей</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

