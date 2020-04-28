---
title: Агрегатные функции, функция CALC и ключевое слово NEW
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297195"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="d9f4b-102">Агрегатные функции, функция CALC и ключевое слово NEW</span><span class="sxs-lookup"><span data-stu-id="d9f4b-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="d9f4b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9f4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9f4b-104">Функция формирования данных поддерживает следующие функции.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="d9f4b-105">Имя, присвоенное разделу, содержащему столбец, с которым выполняется работа, — это *псевдоним главы*.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="d9f4b-106">Название главы — псевдоним может быть полностью полным, состоящим из каждого имени столбца главы, которое начинается с раздела *, содержащего имя столбца,* разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-106">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods.</span></span> <span data-ttu-id="d9f4b-107">Например, если родительская глава, Chap1, содержит дочернюю главу, Chap2, которая содержит столбец Amount (сумма), то полное имя будет Chap1. Chap2. AMT.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9f4b-108">Агрегатные функции</span><span class="sxs-lookup"><span data-stu-id="d9f4b-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="d9f4b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d9f4b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-110">SUM (<em>Chapter-Alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="d9f4b-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-111">Вычисляет сумму всех значений в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-112">AVG (<em>Chapter-Alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="d9f4b-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-113">Вычисляет среднее для всех значений в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-114">MAX (<em>Chapter-Alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="d9f4b-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-115">Вычисляет максимальное значение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-116">MIN (<em>Chapter-Alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="d9f4b-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-117">Вычисляет минимальное значение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-118">COUNT (<em>Chapter-Alias</em>[.<em> column-name</em>])</span><span class="sxs-lookup"><span data-stu-id="d9f4b-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-119">Подсчитывает количество строк в указанном псевдониме.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-119">Counts the number of rows in the specified alias.</span></span> <span data-ttu-id="d9f4b-120">Если указан столбец, в число включаются только те строки, для которых этот столбец имеет значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-120">If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-121">СТАНДОТКЛОН (<em>Chapter-Alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="d9f4b-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-122">Вычисляет стандартное отклонение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-123">ANY (<em>Chapter-Alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="d9f4b-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-124">Значение указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-124">A value of the specified column.</span></span> <span data-ttu-id="d9f4b-125">Значение ANY имеет прогнозируемое значение, только если значение столбца одинаково для всех строк в главе.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-125">ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="d9f4b-126"><strong>Note</strong>: если столбец содержит одно и то же значение для всех строк в главе, команда Shape произвольно возвращает одно из значений в качестве значения функции Any.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9f4b-127">Вычисляемое выражение</span><span class="sxs-lookup"><span data-stu-id="d9f4b-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="d9f4b-128">Описание</span><span class="sxs-lookup"><span data-stu-id="d9f4b-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-129">CALC (<em>выражение</em>)</span><span class="sxs-lookup"><span data-stu-id="d9f4b-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-130">Вычисляет произвольное выражение, но только для строки <strong>Recordset</strong> , СОДЕРЖАЩЕЙ функцию Calc.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-130">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function.</span></span> <span data-ttu-id="d9f4b-131">Любое выражение, использующее эти <a href="visual-basic-for-applications-functions.md">функции Visual Basic для приложений (VBA)</a> , разрешено.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-131">Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9f4b-132">Ключевое слово NEW</span><span class="sxs-lookup"><span data-stu-id="d9f4b-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="d9f4b-133">Описание</span><span class="sxs-lookup"><span data-stu-id="d9f4b-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-134">New <em>field-Type</em> [(<em>Ошибка</em> <em>точности</em> | <em>масштабирования</em> | <em>ширины</em> | , ошибка <em>масштабирования</em> | <em>error</em>])]</span><span class="sxs-lookup"><span data-stu-id="d9f4b-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-135">Добавляет в <strong>набор записей</strong>пустой столбец указанного типа.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="d9f4b-136">*Типом поля* , передаваемым с помощью ключевого слова New, может быть любой из следующих типов данных.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9f4b-137">Типы данных OLE DB</span><span class="sxs-lookup"><span data-stu-id="d9f4b-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="d9f4b-138">Эквиваленты типов данных ADO</span><span class="sxs-lookup"><span data-stu-id="d9f4b-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="d9f4b-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-140">адбстр</span><span class="sxs-lookup"><span data-stu-id="d9f4b-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="d9f4b-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-142">адбулеан</span><span class="sxs-lookup"><span data-stu-id="d9f4b-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="d9f4b-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-144">аддеЦимал</span><span class="sxs-lookup"><span data-stu-id="d9f4b-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="d9f4b-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-146">адунсигнедтининт</span><span class="sxs-lookup"><span data-stu-id="d9f4b-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="d9f4b-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-148">адтининт</span><span class="sxs-lookup"><span data-stu-id="d9f4b-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="d9f4b-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-150">адунсигнедсмаллинт</span><span class="sxs-lookup"><span data-stu-id="d9f4b-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="d9f4b-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-152">адунсигнединт</span><span class="sxs-lookup"><span data-stu-id="d9f4b-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="d9f4b-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-154">адбигинт</span><span class="sxs-lookup"><span data-stu-id="d9f4b-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="d9f4b-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-156">адунсигнедбигинт</span><span class="sxs-lookup"><span data-stu-id="d9f4b-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="d9f4b-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-158">адгуид</span><span class="sxs-lookup"><span data-stu-id="d9f4b-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="d9f4b-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-160">Адбинари, Адварбинари, Адлонгварбинари</span><span class="sxs-lookup"><span data-stu-id="d9f4b-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="d9f4b-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-162">Адчар, Адварчар, Адлонгварчар</span><span class="sxs-lookup"><span data-stu-id="d9f4b-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="d9f4b-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-164">Адвчар, Адварвчар, Адлонгварвчар</span><span class="sxs-lookup"><span data-stu-id="d9f4b-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="d9f4b-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-166">аднумерик</span><span class="sxs-lookup"><span data-stu-id="d9f4b-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="d9f4b-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-168">аддбдате</span><span class="sxs-lookup"><span data-stu-id="d9f4b-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="d9f4b-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-170">аддбтиме</span><span class="sxs-lookup"><span data-stu-id="d9f4b-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="d9f4b-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-172">аддбтиместамп</span><span class="sxs-lookup"><span data-stu-id="d9f4b-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="d9f4b-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-174">адварнумерик</span><span class="sxs-lookup"><span data-stu-id="d9f4b-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9f4b-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="d9f4b-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-176">адфилетиме</span><span class="sxs-lookup"><span data-stu-id="d9f4b-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f4b-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="d9f4b-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="d9f4b-178">адеррор</span><span class="sxs-lookup"><span data-stu-id="d9f4b-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d9f4b-179">Если новое поле имеет тип Decimal (в OLE DB, DBTYPE\_Decimal или в ADO, аддеЦимал), необходимо указать значения точности и масштаба.</span><span class="sxs-lookup"><span data-stu-id="d9f4b-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

