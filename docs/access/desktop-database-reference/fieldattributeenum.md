---
title: FieldAttributeEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292603"
---
# <a name="fieldattributeenum"></a><span data-ttu-id="dcfbe-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="dcfbe-102">FieldAttributeEnum</span></span>

<span data-ttu-id="dcfbe-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcfbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dcfbe-104">Указывает один или несколько атрибутов объекта [Field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="dcfbe-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcfbe-105">Константа</span><span class="sxs-lookup"><span data-stu-id="dcfbe-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="dcfbe-106">Значение</span><span class="sxs-lookup"><span data-stu-id="dcfbe-106">Value</span></span></p></th>
<th><p><span data-ttu-id="dcfbe-107">Описание</span><span class="sxs-lookup"><span data-stu-id="dcfbe-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-108"><strong>adFldCacheDeferred</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="dcfbe-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-110">Указывает, что поставщик кэшет значений полей и что последующие считывались из кэша.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-111"><strong>adFldFixed</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-112">0x10</span><span class="sxs-lookup"><span data-stu-id="dcfbe-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-113">Указывает, что поле содержит данные фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-114"><strong>adFldIsChapter</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="dcfbe-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-116">Указывает, что поле содержит значение главы, которое указывает определенный набор записей, связанный с этим родительским полем.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-116">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field.</span></span> <span data-ttu-id="dcfbe-117">Обычно поля глав используются с формированием данных или фильтрами.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-117">Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-118"><strong>adFldIsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-119">0x40000</span><span class="sxs-lookup"><span data-stu-id="dcfbe-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-120">Указывает, что в поле указывается, что ресурс, представленный записью, представляет собой коллекцию других ресурсов, таких как папка, а не простой ресурс, например текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-121"><strong>adFldIsDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-122">0x20000</span><span class="sxs-lookup"><span data-stu-id="dcfbe-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-123">Указывает, что поле содержит поток по умолчанию для ресурса, представленного записью.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="dcfbe-124">Например, потоком по умолчанию может быть HTML-контент корневой папки на веб-сайте, который автоматически обслуживается при указании корневого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-125"><strong>adFldIsNullable</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-126">0x20</span><span class="sxs-lookup"><span data-stu-id="dcfbe-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-127">Указывает, что поле принимает значения null.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-128"><strong>adFldIsRowURL</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-129">0x10000</span><span class="sxs-lookup"><span data-stu-id="dcfbe-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-130">Указывает, что поле содержит URL-адрес, который указывает имя ресурса из данных, представляемого записью.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-132">0x80</span><span class="sxs-lookup"><span data-stu-id="dcfbe-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-133">Указывает, что поле является длинным двоичным полем.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-133">Indicates that the field is a long binary field.</span></span> <span data-ttu-id="dcfbe-134">Также указывает, что можно использовать методы <a href="appendchunk-method-ado.md">AppendChunk</a> и <a href="getchunk-method-ado.md">GetChunk.</a></span><span class="sxs-lookup"><span data-stu-id="dcfbe-134">Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-136">0x40</span><span class="sxs-lookup"><span data-stu-id="dcfbe-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-137">Указывает, что можно считыть значения null из поля.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-138"><strong>adFldMayDefer</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-139">0x2</span><span class="sxs-lookup"><span data-stu-id="dcfbe-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-140">Указывает, что поле отложено, то есть значения полей не извлекаются из источника данных со всей записью, а только при явном доступе к ним.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="dcfbe-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-143">Указывает, что поле представляет числовую величину из столбца, который поддерживает отрицательные значения масштаба.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-143">Indicates that the field represents a numeric value from a column that supports negative scale values.</span></span> <span data-ttu-id="dcfbe-144">Масштаб задан свойством <a href="numericscale-property-ado.md">NumericScale.</a></span><span class="sxs-lookup"><span data-stu-id="dcfbe-144">The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-145"><strong>adFldRowID</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-146">0x100</span><span class="sxs-lookup"><span data-stu-id="dcfbe-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-147">Указывает, что поле содержит постоянный идентификатор строки, в который нельзя записать значение, и не имеет осмысленное значение, кроме идентификации строки (например, номера записи, уникального идентификатора и так далее).</span><span class="sxs-lookup"><span data-stu-id="dcfbe-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-149">0x200</span><span class="sxs-lookup"><span data-stu-id="dcfbe-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-150">Указывает, что поле содержит отметку времени или даты, используемую для отслеживания обновлений.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-152">0x8</span><span class="sxs-lookup"><span data-stu-id="dcfbe-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-153">Указывает, что поставщик не может определить, можно ли записывать данные в поле.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-154"><strong>adFldUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-155">–1</span><span class="sxs-lookup"><span data-stu-id="dcfbe-155">-1</span></span><br />
<span data-ttu-id="dcfbe-156">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="dcfbe-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-157">Указывает, что поставщик не указывает атрибуты поля.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="dcfbe-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="dcfbe-159">0x4</span><span class="sxs-lookup"><span data-stu-id="dcfbe-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="dcfbe-160">Указывает, что в поле можно записывать данные.</span><span class="sxs-lookup"><span data-stu-id="dcfbe-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="dcfbe-161">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="dcfbe-161">ADO/WFC equivalent</span></span>

<span data-ttu-id="dcfbe-162">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="dcfbe-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcfbe-163">Константа</span><span class="sxs-lookup"><span data-stu-id="dcfbe-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="dcfbe-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-165">AdoEnums.FieldAttribute.FIXED</span><span class="sxs-lookup"><span data-stu-id="dcfbe-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-166">AdoEnums.FieldAttribute.ISNULLABLE</span><span class="sxs-lookup"><span data-stu-id="dcfbe-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-167">AdoEnums.FieldAttribute.LONG</span><span class="sxs-lookup"><span data-stu-id="dcfbe-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-168">AdoEnums.FieldAttribute.MAYBENULL</span><span class="sxs-lookup"><span data-stu-id="dcfbe-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-169">AdoEnums.FieldAttribute.MAYDEFER</span><span class="sxs-lookup"><span data-stu-id="dcfbe-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span><span class="sxs-lookup"><span data-stu-id="dcfbe-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-171">AdoEnums.FieldAttribute.ROWID</span><span class="sxs-lookup"><span data-stu-id="dcfbe-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-172">AdoEnums.FieldAttribute.ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="dcfbe-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span><span class="sxs-lookup"><span data-stu-id="dcfbe-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcfbe-174">AdoEnums.FieldAttribute.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="dcfbe-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcfbe-175">AdoEnums.FieldAttribute.UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="dcfbe-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

