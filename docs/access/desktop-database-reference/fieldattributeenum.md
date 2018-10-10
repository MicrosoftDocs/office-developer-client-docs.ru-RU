---
title: FieldAttributeEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75644308b1af0dd4c6e3b40b2bd6b1c7461f928f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482614"
---
# <a name="fieldattributeenum"></a><span data-ttu-id="ebdc2-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="ebdc2-102">FieldAttributeEnum</span></span>


<span data-ttu-id="ebdc2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebdc2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ebdc2-104">Задает один или несколько атрибутов объекта [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ebdc2-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ebdc2-105">Константа</span><span class="sxs-lookup"><span data-stu-id="ebdc2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ebdc2-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ebdc2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ebdc2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ebdc2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-108"><strong>adFldCacheDeferred</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="ebdc2-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-110">Указывает, что поставщик кэширует значения полей и что последующих операций чтения выполняются из кэша.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-111"><strong>adFldFixed</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-112">0x10</span><span class="sxs-lookup"><span data-stu-id="ebdc2-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-113">Указывает, что поле содержит данные фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-114"><strong>adFldIsChapter</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="ebdc2-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-116">Указывает, что поле содержит значение главы, которое указывает набор дочерних записей, связанного с данным полем родительского.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-116">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field.</span></span> <span data-ttu-id="ebdc2-117">Обычно поля главы используются с формирования данных или фильтры.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-117">Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-118"><strong>adFldIsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-119">0x40000</span><span class="sxs-lookup"><span data-stu-id="ebdc2-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-120">Означает, что это поле указывает, что представленный запись ресурса представляет собой коллекцию другие ресурсы, например, в папке, а не простой ресурсов, таких как текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-121"><strong>adFldIsDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-122">0x20000</span><span class="sxs-lookup"><span data-stu-id="ebdc2-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-123">Указывает, что поле содержит поток по умолчанию для ресурса, представленное эту запись.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="ebdc2-124">Например поток по умолчанию может быть HTML-содержимое в корневой папке на веб-сайт, который автоматически выдается, когда он указан корневой URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-125"><strong>adFldIsNullable</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-126">0x20</span><span class="sxs-lookup"><span data-stu-id="ebdc2-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-127">Указывает, что поле может принимать значения null.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-128"><strong>adFldIsRowURL</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-129">0x10000</span><span class="sxs-lookup"><span data-stu-id="ebdc2-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-130">Указывает, что поле содержит URL-адрес, имена ресурсов из хранилища данных, представленного эту запись.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-132">0x80</span><span class="sxs-lookup"><span data-stu-id="ebdc2-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-133">Указывает, что поле двоичные поля.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-133">Indicates that the field is a long binary field.</span></span> <span data-ttu-id="ebdc2-134">Также указывается, что можно использовать методы <a href="appendchunk-method-ado.md">AppendChunk</a> и <a href="getchunk-method-ado.md">GetChunk</a> .</span><span class="sxs-lookup"><span data-stu-id="ebdc2-134">Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-136">0x40</span><span class="sxs-lookup"><span data-stu-id="ebdc2-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-137">Указывает, что значения null могут читать из поля.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-138"><strong>adFldMayDefer</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-139">0x2</span><span class="sxs-lookup"><span data-stu-id="ebdc2-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-140">Указывает, что поле откладывается, то есть, значения полей не извлекаются из источника данных с помощью всей записи, но только в том случае, если вы явно к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="ebdc2-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-143">Указывает, что поле представляет числовое значение из столбца, поддерживающего масштаба отрицательные значения.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-143">Indicates that the field represents a numeric value from a column that supports negative scale values.</span></span> <span data-ttu-id="ebdc2-144">Масштаб, задаваемое свойству <a href="numericscale-property-ado.md">NumericScale</a> .</span><span class="sxs-lookup"><span data-stu-id="ebdc2-144">The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-145"><strong>adFldRowID</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-146">0x100</span><span class="sxs-lookup"><span data-stu-id="ebdc2-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-147">Указывает, что поле содержит постоянный идентификатор строки, который невозможно записать и не имеет смысл значения кроме идентификации строки (например, запишите номер, уникальный идентификатор и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ebdc2-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-149">0x200</span><span class="sxs-lookup"><span data-stu-id="ebdc2-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-150">Указывает, что поле содержит каких-либо штамп даты и времени для отслеживания обновлений.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-152">0x8</span><span class="sxs-lookup"><span data-stu-id="ebdc2-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-153">Указывает, что поставщик не может определить, если можно создать в поле.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-154"><strong>adFldUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-155">-1</span><span class="sxs-lookup"><span data-stu-id="ebdc2-155">-1</span></span><br />
<span data-ttu-id="ebdc2-156">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="ebdc2-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-157">Указывает, что поставщик не определяет атрибуты поля.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc2-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="ebdc2-159">0x4</span><span class="sxs-lookup"><span data-stu-id="ebdc2-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="ebdc2-160">Указывает, что можно написать в поле.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ebdc2-161">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="ebdc2-161">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="ebdc2-162">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ebdc2-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ebdc2-163">Constant</span><span class="sxs-lookup"><span data-stu-id="ebdc2-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="ebdc2-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-165">AdoEnums.FieldAttribute.FIXED</span><span class="sxs-lookup"><span data-stu-id="ebdc2-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-166">AdoEnums.FieldAttribute.ISNULLABLE</span><span class="sxs-lookup"><span data-stu-id="ebdc2-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-167">AdoEnums.FieldAttribute.LONG</span><span class="sxs-lookup"><span data-stu-id="ebdc2-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-168">AdoEnums.FieldAttribute.MAYBENULL</span><span class="sxs-lookup"><span data-stu-id="ebdc2-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-169">AdoEnums.FieldAttribute.MAYDEFER</span><span class="sxs-lookup"><span data-stu-id="ebdc2-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span><span class="sxs-lookup"><span data-stu-id="ebdc2-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-171">AdoEnums.FieldAttribute.ROWID</span><span class="sxs-lookup"><span data-stu-id="ebdc2-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-172">AdoEnums.FieldAttribute.ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="ebdc2-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span><span class="sxs-lookup"><span data-stu-id="ebdc2-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebdc2-174">AdoEnums.FieldAttribute.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="ebdc2-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebdc2-175">AdoEnums.FieldAttribute.UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="ebdc2-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

