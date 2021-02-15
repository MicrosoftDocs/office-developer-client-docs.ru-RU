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
# <a name="adcprop_autorecalc_enum"></a>ADCPROP \_ AUTORECALC \_ ENUM

**Область применения**: Access 2013, Office 2013

Указывает, когда поставщик [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) повторно вычисляет сводные и вычисляемые столбцы в иерархическом наборе записей.

Эти константы используются только с поставщиком **MSDataShape** и динамическим свойством **Recordset** **"Auto Recalc",** на которое ссылается динамический индекс [свойств ADO](ado-dynamic-property-index.md) и документируется в службе курсоров Майкрософт для [OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) или службе формирования данных Майкрософт для [документации OLE DB.](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

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
<td><p><strong>adRecalcAlways</strong></p></td>
<td><p>1 </p></td>
<td><p>Значение, используемое по умолчанию. Пересчитывает каждый раз, когда поставщик <strong>MSDataShape</strong> определяет значения, от которых зависят вычисленные столбцы.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>0</p></td>
<td><p>Вычисляется только при первоначальном построении иерархического <strong>наборов записей.</strong></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

