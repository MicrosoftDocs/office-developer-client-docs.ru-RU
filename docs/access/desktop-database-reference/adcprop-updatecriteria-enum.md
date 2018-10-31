---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 942639a4c87cfe325b9ec8326e2eb392458fa8b3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863692"
---
# <a name="adcpropupdatecriteriaenum"></a><span data-ttu-id="d9757-102">ADCPROP\_UPDATECRITERIA\_ENUM</span><span class="sxs-lookup"><span data-stu-id="d9757-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="d9757-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9757-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d9757-104">Задает поля, которые можно использовать для определения конфликтов при обновлении оптимистичный строки из источника данных с помощью объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d9757-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="d9757-105">Используйте эти константы со свойством динамических «**Условию обновления**» **набора записей** , который по ссылке в [ADO динамических свойство индекса](ado-dynamic-property-index.md) и описаны в документации по [Microsoft служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="d9757-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9757-106">Константа</span><span class="sxs-lookup"><span data-stu-id="d9757-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="d9757-107">Значение</span><span class="sxs-lookup"><span data-stu-id="d9757-107">Value</span></span></p></th>
<th><p><span data-ttu-id="d9757-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d9757-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9757-109"><strong>adCriteriaAllCols</strong></span><span class="sxs-lookup"><span data-stu-id="d9757-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="d9757-110">1</span><span class="sxs-lookup"><span data-stu-id="d9757-110">1</span></span></p></td>
<td><p><span data-ttu-id="d9757-111">Обнаруживает конфликтов при изменении любого столбца строки источника данных.</span><span class="sxs-lookup"><span data-stu-id="d9757-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9757-112"><strong>adCriteriaKey</strong></span><span class="sxs-lookup"><span data-stu-id="d9757-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="d9757-113">0</span><span class="sxs-lookup"><span data-stu-id="d9757-113">0</span></span></p></td>
<td><p><span data-ttu-id="d9757-114">Обнаружение конфликтов Если ключевого столбца данных источника строки был изменен, что означает, что строка была удалена.</span><span class="sxs-lookup"><span data-stu-id="d9757-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9757-115"><strong>adCriteriaTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="d9757-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="d9757-116">3</span><span class="sxs-lookup"><span data-stu-id="d9757-116">3</span></span></p></td>
<td><p><span data-ttu-id="d9757-117">Обнаружение конфликтов, если метка времени данных источника строки был изменен, что означает, что строка осуществлялся после получения <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="d9757-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9757-118"><strong>adCriteriaUpdCols</strong></span><span class="sxs-lookup"><span data-stu-id="d9757-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="d9757-119">2</span><span class="sxs-lookup"><span data-stu-id="d9757-119">2</span></span></p></td>
<td><p><span data-ttu-id="d9757-120">Обнаруживает конфликты, если столбцы строки источника данных, которые соответствуют обновляться полям <strong>набора записей</strong> были изменены.</span><span class="sxs-lookup"><span data-stu-id="d9757-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d9757-121">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d9757-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="d9757-122">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d9757-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9757-123">Constant</span><span class="sxs-lookup"><span data-stu-id="d9757-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9757-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span><span class="sxs-lookup"><span data-stu-id="d9757-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9757-125">AdoEnums.AdcPropUpdateCriteria.KEY</span><span class="sxs-lookup"><span data-stu-id="d9757-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9757-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="d9757-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9757-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span><span class="sxs-lookup"><span data-stu-id="d9757-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

