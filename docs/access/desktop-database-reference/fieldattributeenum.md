---
title: Фиелдаттрибутинум (Справочник по базам данных Access на компьютере)
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
# <a name="fieldattributeenum"></a><span data-ttu-id="77cd4-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="77cd4-102">FieldAttributeEnum</span></span>

<span data-ttu-id="77cd4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77cd4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77cd4-104">Задает один или несколько атрибутов объекта [field](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="77cd4-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77cd4-105">Константа</span><span class="sxs-lookup"><span data-stu-id="77cd4-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="77cd4-106">Значение</span><span class="sxs-lookup"><span data-stu-id="77cd4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="77cd4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="77cd4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-108"><strong>Адфлдкачедеферред</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="77cd4-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="77cd4-110">Указывает, что поставщик кэширует значения полей, а последующие операции чтения выполняются из кэша.</span><span class="sxs-lookup"><span data-stu-id="77cd4-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-111"><strong>Адфлдфиксед</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-112">0x10</span><span class="sxs-lookup"><span data-stu-id="77cd4-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="77cd4-113">Указывает, что поле содержит данные фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="77cd4-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-114"><strong>Адфлдисчаптер</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="77cd4-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="77cd4-116">Указывает, что поле содержит значение главы, которое указывает конкретный дочерний набор записей, связанный с этим родительским полем.</span><span class="sxs-lookup"><span data-stu-id="77cd4-116">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field.</span></span> <span data-ttu-id="77cd4-117">Обычно поля главы используются с формированием данных или фильтрами.</span><span class="sxs-lookup"><span data-stu-id="77cd4-117">Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-118"><strong>Адфлдисколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-119">0x40000</span><span class="sxs-lookup"><span data-stu-id="77cd4-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="77cd4-120">Указывает, что поле указывает, что ресурс, представленный записью, является коллекцией других ресурсов, например папки, а не простым ресурсом, например текстовым файлом.</span><span class="sxs-lookup"><span data-stu-id="77cd4-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-121"><strong>Адфлдисдефаултстреам</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-122">0x20000</span><span class="sxs-lookup"><span data-stu-id="77cd4-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="77cd4-123">Указывает, что поле содержит поток по умолчанию для ресурса, представленного записью.</span><span class="sxs-lookup"><span data-stu-id="77cd4-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="77cd4-124">Например, поток по умолчанию может быть HTML-контентом корневой папки на веб-сайте, который автоматически обрабатывается, когда указан корневой URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="77cd4-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-125"><strong>Адфлдиснуллабле</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-126">0x20</span><span class="sxs-lookup"><span data-stu-id="77cd4-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="77cd4-127">Указывает, что поле принимает значения NULL.</span><span class="sxs-lookup"><span data-stu-id="77cd4-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-128"><strong>Адфлдисровурл</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-129">0x10000</span><span class="sxs-lookup"><span data-stu-id="77cd4-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="77cd4-130">Указывает, что поле содержит URL-адрес, указывающий ресурс из хранилища данных, представленного записью.</span><span class="sxs-lookup"><span data-stu-id="77cd4-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-131"><strong>Адфлдлонг</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-132">0x80</span><span class="sxs-lookup"><span data-stu-id="77cd4-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="77cd4-133">Указывает, что поле является длинным бинарным полем.</span><span class="sxs-lookup"><span data-stu-id="77cd4-133">Indicates that the field is a long binary field.</span></span> <span data-ttu-id="77cd4-134">Также указывает, что вы можете использовать методы AppendChunk <a href="getchunk-method-ado.md"></a> и <a href="appendchunk-method-ado.md"></a> .</span><span class="sxs-lookup"><span data-stu-id="77cd4-134">Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-135"><strong>Адфлдмайбенулл</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-136">0x40</span><span class="sxs-lookup"><span data-stu-id="77cd4-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="77cd4-137">Указывает, что в поле можно считывать значения NULL.</span><span class="sxs-lookup"><span data-stu-id="77cd4-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-138"><strong>Адфлдмайдефер</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-139">0x2</span><span class="sxs-lookup"><span data-stu-id="77cd4-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="77cd4-140">Указывает, что поле является отложенным — то есть значения полей не извлекаются из источника данных с использованием всей записи, но только при явном доступе к ним.</span><span class="sxs-lookup"><span data-stu-id="77cd4-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-141"><strong>Адфлднегативескале</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="77cd4-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="77cd4-143">Указывает, что поле представляет числовое значение из столбца, поддерживающего отрицательные значения шкалы.</span><span class="sxs-lookup"><span data-stu-id="77cd4-143">Indicates that the field represents a numeric value from a column that supports negative scale values.</span></span> <span data-ttu-id="77cd4-144">Масштаб задается свойством <a href="numericscale-property-ado.md">NumericScale</a> .</span><span class="sxs-lookup"><span data-stu-id="77cd4-144">The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-145"><strong>Адфлдровид</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-146">0x100</span><span class="sxs-lookup"><span data-stu-id="77cd4-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="77cd4-147">Указывает, что поле содержит постоянный идентификатор строки, который не может быть записан в и имеет неосмысленное значение, за исключением идентификации строки (например, номера записи, уникального идентификатора и т. д.).</span><span class="sxs-lookup"><span data-stu-id="77cd4-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-148"><strong>Адфлдровверсион</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-149">0x200</span><span class="sxs-lookup"><span data-stu-id="77cd4-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="77cd4-150">Указывает, что поле содержит дату и время, которые используются для отслеживания обновлений.</span><span class="sxs-lookup"><span data-stu-id="77cd4-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-151"><strong>Адфлдункновнупдатабле</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-152">0x8</span><span class="sxs-lookup"><span data-stu-id="77cd4-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="77cd4-153">Указывает, что поставщик не может определить, можно ли выполнять запись в поле.</span><span class="sxs-lookup"><span data-stu-id="77cd4-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-154"><strong>АдфлдунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-155">–1</span><span class="sxs-lookup"><span data-stu-id="77cd4-155">-1</span></span><br />
<span data-ttu-id="77cd4-156">Равен</span><span class="sxs-lookup"><span data-stu-id="77cd4-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="77cd4-157">Указывает, что поставщик не задает атрибуты поля.</span><span class="sxs-lookup"><span data-stu-id="77cd4-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-158"><strong>Адфлдупдатабле</strong></span><span class="sxs-lookup"><span data-stu-id="77cd4-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="77cd4-159">0x4</span><span class="sxs-lookup"><span data-stu-id="77cd4-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="77cd4-160">Указывает, что вы можете выполнять запись в поле.</span><span class="sxs-lookup"><span data-stu-id="77cd4-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="77cd4-161">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="77cd4-161">ADO/WFC equivalent</span></span>

<span data-ttu-id="77cd4-162">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="77cd4-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77cd4-163">Константа</span><span class="sxs-lookup"><span data-stu-id="77cd4-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-164">Адоенумс. Фиелдаттрибуте. КАЧЕДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="77cd4-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-165">Адоенумс. Фиелдаттрибуте. FIXED</span><span class="sxs-lookup"><span data-stu-id="77cd4-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-166">Адоенумс. Фиелдаттрибуте. NULL</span><span class="sxs-lookup"><span data-stu-id="77cd4-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-167">Адоенумс. Фиелдаттрибуте. LONG</span><span class="sxs-lookup"><span data-stu-id="77cd4-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-168">Адоенумс. Фиелдаттрибуте. МАЙБЕНУЛЛ</span><span class="sxs-lookup"><span data-stu-id="77cd4-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-169">Адоенумс. Фиелдаттрибуте. МАЙДЕФЕР</span><span class="sxs-lookup"><span data-stu-id="77cd4-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-170">Адоенумс. Фиелдаттрибуте. НЕГАТИВЕСКАЛЕ</span><span class="sxs-lookup"><span data-stu-id="77cd4-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-171">Адоенумс. Фиелдаттрибуте. ROWID</span><span class="sxs-lookup"><span data-stu-id="77cd4-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-172">Адоенумс. Фиелдаттрибуте. ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="77cd4-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-173">Адоенумс. Фиелдаттрибуте. УНКНОВНУПДАТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="77cd4-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77cd4-174">Адоенумс. Фиелдаттрибуте. unspecifieded</span><span class="sxs-lookup"><span data-stu-id="77cd4-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77cd4-175">Адоенумс. Фиелдаттрибуте. ОБНОВЛЯЕМый</span><span class="sxs-lookup"><span data-stu-id="77cd4-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

