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
# <a name="adcpropupdatecriteriaenum"></a><span data-ttu-id="f0136-102">Перечисление АДКПРОП\_упдатекритериа\_</span><span class="sxs-lookup"><span data-stu-id="f0136-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="f0136-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0136-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0136-104">Указывает, какие поля можно использовать для обнаружения конфликтов во время оптимистического обновления строки источника данных с помощью объекта [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f0136-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="f0136-105">Используйте эти константы с динамическим свойством **Recordset** "**критерии обновления**", на который ссылается [индекс динамического свойства ADO](ado-dynamic-property-index.md) и задокументированы в документации [службы курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="f0136-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0136-106">Константа</span><span class="sxs-lookup"><span data-stu-id="f0136-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="f0136-107">Значение</span><span class="sxs-lookup"><span data-stu-id="f0136-107">Value</span></span></p></th>
<th><p><span data-ttu-id="f0136-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f0136-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0136-109"><strong>Адкритериааллколс</strong></span><span class="sxs-lookup"><span data-stu-id="f0136-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="f0136-110">1,1</span><span class="sxs-lookup"><span data-stu-id="f0136-110">1</span></span></p></td>
<td><p><span data-ttu-id="f0136-111">Обнаруживает конфликты при изменении любого столбца строки источника данных.</span><span class="sxs-lookup"><span data-stu-id="f0136-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0136-112"><strong>Адкритериакэй</strong></span><span class="sxs-lookup"><span data-stu-id="f0136-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f0136-113">нуль</span><span class="sxs-lookup"><span data-stu-id="f0136-113">0</span></span></p></td>
<td><p><span data-ttu-id="f0136-114">Обнаруживает конфликты, если ключевой столбец строки источника данных изменился, что означает, что строка была удалена.</span><span class="sxs-lookup"><span data-stu-id="f0136-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0136-115"><strong>Адкритериатиместамп</strong></span><span class="sxs-lookup"><span data-stu-id="f0136-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="f0136-116">4</span><span class="sxs-lookup"><span data-stu-id="f0136-116">3</span></span></p></td>
<td><p><span data-ttu-id="f0136-117">Обнаруживает конфликты, если отметка времени строки источника данных была изменена, то есть доступ к строке выполнялся после получения <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="f0136-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0136-118"><strong>Адкритериаупдколс</strong></span><span class="sxs-lookup"><span data-stu-id="f0136-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="f0136-119">2</span><span class="sxs-lookup"><span data-stu-id="f0136-119">2</span></span></p></td>
<td><p><span data-ttu-id="f0136-120">Обнаруживает конфликты при изменении одного из столбцов строки источника данных, соответствующих обновленным полям <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="f0136-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f0136-121">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f0136-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="f0136-122">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="f0136-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0136-123">Константа</span><span class="sxs-lookup"><span data-stu-id="f0136-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0136-124">Адоенумс. Адкпропупдатекритериа. АЛЛКОЛС</span><span class="sxs-lookup"><span data-stu-id="f0136-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0136-125">Адоенумс. Адкпропупдатекритериа. KEY</span><span class="sxs-lookup"><span data-stu-id="f0136-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0136-126">Адоенумс. Адкпропупдатекритериа. TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="f0136-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0136-127">Адоенумс. Адкпропупдатекритериа. УПДКОЛС</span><span class="sxs-lookup"><span data-stu-id="f0136-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

