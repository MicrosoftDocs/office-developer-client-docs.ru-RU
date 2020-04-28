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
# <a name="adcprop_autorecalc_enum"></a><span data-ttu-id="b5533-102">Перечисление АДКПРОП\_ауторекалк\_</span><span class="sxs-lookup"><span data-stu-id="b5533-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="b5533-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5533-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5533-104">Указывает, когда поставщик [мсдаташапе](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) выполняет повторное вычисление статистических и вычисляемых столбцов в иерархическом наборе записей.</span><span class="sxs-lookup"><span data-stu-id="b5533-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="b5533-105">Эти константы используются только с поставщиком **мсдаташапе** и динамическим свойством **Recordset** "**Auto recalc**", на который ссылается [индекс динамического свойства ADO](ado-dynamic-property-index.md) и задокументированы в [службе курсора Microsoft Cursor для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) или Microsoft Cursor [Data Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="b5533-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5533-106">Константа</span><span class="sxs-lookup"><span data-stu-id="b5533-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="b5533-107">Значение</span><span class="sxs-lookup"><span data-stu-id="b5533-107">Value</span></span></p></th>
<th><p><span data-ttu-id="b5533-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b5533-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5533-109"><strong>адрекалкалвайс</strong></span><span class="sxs-lookup"><span data-stu-id="b5533-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="b5533-110">1,1</span><span class="sxs-lookup"><span data-stu-id="b5533-110">1</span></span></p></td>
<td><p><span data-ttu-id="b5533-111">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5533-111">Default.</span></span> <span data-ttu-id="b5533-112">Пересчитывается всякий раз, когда поставщик <strong>мсдаташапе</strong> определяет значения, от которых зависит изменение вычисляемых столбцов.</span><span class="sxs-lookup"><span data-stu-id="b5533-112">Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5533-113"><strong>адрекалкупфронт</strong></span><span class="sxs-lookup"><span data-stu-id="b5533-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="b5533-114">нуль</span><span class="sxs-lookup"><span data-stu-id="b5533-114">0</span></span></p></td>
<td><p><span data-ttu-id="b5533-115">Вычисляется только при первоначальном построении иерархического <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5533-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b5533-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="b5533-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="b5533-117">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="b5533-117">These constants do not have ADO/WFC equivalents.</span></span>

