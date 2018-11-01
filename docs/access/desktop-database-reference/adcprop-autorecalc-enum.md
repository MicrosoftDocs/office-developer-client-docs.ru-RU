---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: d8f8a8f3ea27ff40c059ceada6d7f6df65b79664
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867176"
---
# <a name="adcpropautorecalcenum"></a>ADCPROP\_AUTORECALC\_ENUM

**Применимо к**: Access 2013, Office 2013

Указывает, когда поставщик [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) повторно вычисляет статистические и вычисляемых столбцов в иерархической записей.

Эти константы используются только с поставщик **MSDataShape** и **записей** «**Автоматическое обновление ссылок**» динамические свойства, которое по ссылке в [ADO динамических свойство индекса](ado-dynamic-property-index.md) и описаны в [службы Microsoft курсора для OLE База данных](microsoft-cursor-service-for-ole-db-ado-service-component.md) или документации [Служба формирования Microsoft данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .

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
<td><p>1</p></td>
<td><p>Значение, используемое по умолчанию. Пересчет каждый раз, когда поставщик <strong>MSDataShape</strong> определяет значения, которые зависят от вычисляемых столбцов были изменены.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>0</p></td>
<td><p>Вычисляет только в том случае, если изначально построение иерархических <strong>набора записей</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы нет ADO/WFC эквивалентами.

