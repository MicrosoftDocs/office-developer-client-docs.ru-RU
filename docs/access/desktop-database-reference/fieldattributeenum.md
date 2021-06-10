---
title: FieldAttributeEnum (Ссылка на настольные базы данных)
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
# <a name="fieldattributeenum"></a><span data-ttu-id="b8c87-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="b8c87-102">FieldAttributeEnum</span></span>

<span data-ttu-id="b8c87-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8c87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8c87-104">Указывает один или несколько атрибутов объекта [Field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b8c87-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8c87-105">Константа</span><span class="sxs-lookup"><span data-stu-id="b8c87-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b8c87-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b8c87-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b8c87-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b8c87-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-108"><strong>adFldCacheDeferred</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="b8c87-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="b8c87-110">Указывает, что поставщик кэша значений поля и последующих считывалось из кэша.</span><span class="sxs-lookup"><span data-stu-id="b8c87-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-111"><strong>adFldFixed</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-112">0x10</span><span class="sxs-lookup"><span data-stu-id="b8c87-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="b8c87-113">Указывает, что поле содержит данные фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="b8c87-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-114"><strong>adFldIsChapter</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="b8c87-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="b8c87-116">Указывает, что поле содержит значение главы, которое указывает определенный набор записей ребенка, связанный с этим родительским полем.</span><span class="sxs-lookup"><span data-stu-id="b8c87-116">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field.</span></span> <span data-ttu-id="b8c87-117">Обычно поля глав используются при формировании данных или фильтрах.</span><span class="sxs-lookup"><span data-stu-id="b8c87-117">Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-118"><strong>adFldIsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-119">0x40000</span><span class="sxs-lookup"><span data-stu-id="b8c87-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="b8c87-120">Указывает, что поле указывает, что ресурс, представленный записью, представляет собой коллекцию других ресурсов, таких как папка, а не простой ресурс, например текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="b8c87-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-121"><strong>adFldIsDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-122">0x20000</span><span class="sxs-lookup"><span data-stu-id="b8c87-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="b8c87-123">Указывает, что поле содержит поток по умолчанию для ресурса, представленного записью.</span><span class="sxs-lookup"><span data-stu-id="b8c87-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="b8c87-124">Например, поток по умолчанию может быть HTML-контентом корневой папки на веб-сайте, который автоматически подается при указании корневого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b8c87-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-125"><strong>adFldIsNullable</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-126">0x20</span><span class="sxs-lookup"><span data-stu-id="b8c87-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="b8c87-127">Указывает, что поле принимает значения null.</span><span class="sxs-lookup"><span data-stu-id="b8c87-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-128"><strong>adFldIsRowURL</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-129">0x10000</span><span class="sxs-lookup"><span data-stu-id="b8c87-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="b8c87-130">Указывает, что поле содержит URL-адрес, который называет ресурс из магазина данных, представленного записью.</span><span class="sxs-lookup"><span data-stu-id="b8c87-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-132">0x80</span><span class="sxs-lookup"><span data-stu-id="b8c87-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="b8c87-133">Указывает, что поле — это длинное двоичное поле.</span><span class="sxs-lookup"><span data-stu-id="b8c87-133">Indicates that the field is a long binary field.</span></span> <span data-ttu-id="b8c87-134">Также указывает, что можно использовать методы <a href="appendchunk-method-ado.md">AppendChunk</a> и <a href="getchunk-method-ado.md">GetChunk.</a></span><span class="sxs-lookup"><span data-stu-id="b8c87-134">Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-136">0x40</span><span class="sxs-lookup"><span data-stu-id="b8c87-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="b8c87-137">Указывает, что вы можете читать значения null из поля.</span><span class="sxs-lookup"><span data-stu-id="b8c87-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-138"><strong>adFldMayDefer</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-139">0x2</span><span class="sxs-lookup"><span data-stu-id="b8c87-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="b8c87-140">Указывает, что поле отложено, то есть значения поля извлекаются не из источника данных со всей записью, а только при явном доступе к ним.</span><span class="sxs-lookup"><span data-stu-id="b8c87-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="b8c87-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="b8c87-143">Указывает, что поле представляет числовую величину столбца, поддерживают отрицательные значения масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b8c87-143">Indicates that the field represents a numeric value from a column that supports negative scale values.</span></span> <span data-ttu-id="b8c87-144">Масштаб указывается <a href="numericscale-property-ado.md">свойством NumericScale.</a></span><span class="sxs-lookup"><span data-stu-id="b8c87-144">The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-145"><strong>adFldRowID</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-146">0x100</span><span class="sxs-lookup"><span data-stu-id="b8c87-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="b8c87-147">Указывает, что поле содержит постоянный идентификатор строки, который не может быть написан и не имеет значимого значения, кроме как определить строку (например, номер записи, уникальный идентификатор и так далее).</span><span class="sxs-lookup"><span data-stu-id="b8c87-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-149">0x200</span><span class="sxs-lookup"><span data-stu-id="b8c87-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="b8c87-150">Указывает, что поле содержит какой-то штамп времени или даты, используемый для отслеживания обновлений.</span><span class="sxs-lookup"><span data-stu-id="b8c87-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-152">0x8</span><span class="sxs-lookup"><span data-stu-id="b8c87-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="b8c87-153">Указывает, что поставщик не может определить, можно ли написать в поле.</span><span class="sxs-lookup"><span data-stu-id="b8c87-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-154"><strong>adFldUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-155">–1</span><span class="sxs-lookup"><span data-stu-id="b8c87-155">-1</span></span><br />
<span data-ttu-id="b8c87-156">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="b8c87-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="b8c87-157">Указывает, что поставщик не указывает атрибуты поля.</span><span class="sxs-lookup"><span data-stu-id="b8c87-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="b8c87-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="b8c87-159">0x4</span><span class="sxs-lookup"><span data-stu-id="b8c87-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="b8c87-160">Указывает, что вы можете написать в поле.</span><span class="sxs-lookup"><span data-stu-id="b8c87-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b8c87-161">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="b8c87-161">ADO/WFC equivalent</span></span>

<span data-ttu-id="b8c87-162">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b8c87-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8c87-163">Константа</span><span class="sxs-lookup"><span data-stu-id="b8c87-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="b8c87-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-165">AdoEnums.FieldAttribute.FIXED</span><span class="sxs-lookup"><span data-stu-id="b8c87-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-166">AdoEnums.FieldAttribute.ISNULLABLE</span><span class="sxs-lookup"><span data-stu-id="b8c87-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-167">AdoEnums.FieldAttribute.LONG</span><span class="sxs-lookup"><span data-stu-id="b8c87-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-168">AdoEnums.FieldAttribute.MAYBENULL</span><span class="sxs-lookup"><span data-stu-id="b8c87-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-169">AdoEnums.FieldAttribute.MAYDEFER</span><span class="sxs-lookup"><span data-stu-id="b8c87-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span><span class="sxs-lookup"><span data-stu-id="b8c87-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-171">AdoEnums.FieldAttribute.ROWID</span><span class="sxs-lookup"><span data-stu-id="b8c87-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-172">AdoEnums.FieldAttribute.ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="b8c87-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span><span class="sxs-lookup"><span data-stu-id="b8c87-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8c87-174">AdoEnums.FieldAttribute.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="b8c87-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8c87-175">AdoEnums.FieldAttribute.UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="b8c87-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

