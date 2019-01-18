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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705402"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="1f3b5-102">ADCPROP\_AUTORECALC\_ENUM</span><span class="sxs-lookup"><span data-stu-id="1f3b5-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="1f3b5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f3b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f3b5-104">Указывает, когда поставщик [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) повторно вычисляет статистические и вычисляемых столбцов в иерархической записей.</span><span class="sxs-lookup"><span data-stu-id="1f3b5-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="1f3b5-105">Эти константы используются только с поставщик **MSDataShape** и **записей** «**Автоматическое обновление ссылок**» динамические свойства, которое по ссылке в [ADO динамических свойство индекса](ado-dynamic-property-index.md) и описаны в [службы Microsoft курсора для OLE База данных](microsoft-cursor-service-for-ole-db-ado-service-component.md) или документации [Служба формирования Microsoft данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="1f3b5-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f3b5-106">Константа</span><span class="sxs-lookup"><span data-stu-id="1f3b5-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="1f3b5-107">Значение</span><span class="sxs-lookup"><span data-stu-id="1f3b5-107">Value</span></span></p></th>
<th><p><span data-ttu-id="1f3b5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1f3b5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f3b5-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="1f3b5-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3b5-110">1</span><span class="sxs-lookup"><span data-stu-id="1f3b5-110">1</span></span></p></td>
<td><p><span data-ttu-id="1f3b5-111">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f3b5-111">Default.</span></span> <span data-ttu-id="1f3b5-112">Пересчет каждый раз, когда поставщик <strong>MSDataShape</strong> определяет значения, которые зависят от вычисляемых столбцов были изменены.</span><span class="sxs-lookup"><span data-stu-id="1f3b5-112">Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f3b5-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="1f3b5-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="1f3b5-114">0</span><span class="sxs-lookup"><span data-stu-id="1f3b5-114">0</span></span></p></td>
<td><p><span data-ttu-id="1f3b5-115">Вычисляет только в том случае, если изначально построение иерархических <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f3b5-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1f3b5-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1f3b5-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="1f3b5-117">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="1f3b5-117">These constants do not have ADO/WFC equivalents.</span></span>

