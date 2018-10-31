---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b9c1aff21b62eff061a3f68ef3ad56e07e46388d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860086"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="8e665-102">ADCPROP\_AUTORECALC\_ENUM</span><span class="sxs-lookup"><span data-stu-id="8e665-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="8e665-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e665-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8e665-104">Указывает, когда поставщик [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) повторно вычисляет статистические и вычисляемых столбцов в иерархической записей.</span><span class="sxs-lookup"><span data-stu-id="8e665-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="8e665-105">Эти константы используются только с поставщик **MSDataShape** и **записей** «**Автоматическое обновление ссылок**» динамические свойства, которое по ссылке в [ADO динамических свойство индекса](ado-dynamic-property-index.md) и описаны в [службы Microsoft курсора для OLE База данных](microsoft-cursor-service-for-ole-db-ado-service-component.md) или документации [Служба формирования Microsoft данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="8e665-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e665-106">Константа</span><span class="sxs-lookup"><span data-stu-id="8e665-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="8e665-107">Значение</span><span class="sxs-lookup"><span data-stu-id="8e665-107">Value</span></span></p></th>
<th><p><span data-ttu-id="8e665-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8e665-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e665-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="8e665-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="8e665-110">1</span><span class="sxs-lookup"><span data-stu-id="8e665-110">1</span></span></p></td>
<td><p><span data-ttu-id="8e665-111">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e665-111">Default.</span></span> <span data-ttu-id="8e665-112">Пересчет каждый раз, когда поставщик <strong>MSDataShape</strong> определяет значения, которые зависят от вычисляемых столбцов были изменены.</span><span class="sxs-lookup"><span data-stu-id="8e665-112">Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e665-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="8e665-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="8e665-114">0</span><span class="sxs-lookup"><span data-stu-id="8e665-114">0</span></span></p></td>
<td><p><span data-ttu-id="8e665-115">Вычисляет только в том случае, если изначально построение иерархических <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e665-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8e665-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8e665-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="8e665-117">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="8e665-117">These constants do not have ADO/WFC equivalents.</span></span>

