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
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="3eafc-102">Агрегатные функции, функция CALC и ключевое слово NEW</span><span class="sxs-lookup"><span data-stu-id="3eafc-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="3eafc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3eafc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3eafc-104">Формирование данных поддерживает следующие функции.</span><span class="sxs-lookup"><span data-stu-id="3eafc-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="3eafc-105">Имя, назначенное главе, содержащей столбец, на котором будет работать столбец, является *псевдонимом главы*.</span><span class="sxs-lookup"><span data-stu-id="3eafc-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="3eafc-106">Псевдоним главы может быть полностью квалифицированным, состоящим из каждого имени столбца главы, ведущего к *главе,* содержащей имя столбца, разделенное по периодам.</span><span class="sxs-lookup"><span data-stu-id="3eafc-106">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods.</span></span> <span data-ttu-id="3eafc-107">Например, если в родительской главе chap1 содержится детская глава chap2, которая содержит столбец суммы, амт, то квалифицированным именем будет chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="3eafc-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3eafc-108">Агрегатные функции</span><span class="sxs-lookup"><span data-stu-id="3eafc-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="3eafc-109">Description</span><span class="sxs-lookup"><span data-stu-id="3eafc-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-110">SUM<em>(псевдоним главы.</em><em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="3eafc-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="3eafc-111">Вычисляет сумму всех значений в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="3eafc-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-112">AVG<em>(псевдоним главы.</em><em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="3eafc-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="3eafc-113">Вычисляет среднее значение всех значений указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="3eafc-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-114">MAX<em>(псевдоним главы.</em><em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="3eafc-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="3eafc-115">Вычисляет максимальное значение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="3eafc-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-116">MIN<em>(псевдоним главы.</em><em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="3eafc-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="3eafc-117">Вычисляет минимальное значение указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="3eafc-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-118">COUNT<em>(псевдоним главы</em>[.<em> столбец-имя</em>])</span><span class="sxs-lookup"><span data-stu-id="3eafc-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="3eafc-119">Подсчитывают количество строк в указанном псевдониме.</span><span class="sxs-lookup"><span data-stu-id="3eafc-119">Counts the number of rows in the specified alias.</span></span> <span data-ttu-id="3eafc-120">Если указан столбец, в графу включаются только строки, для которых этот столбец не является Null.</span><span class="sxs-lookup"><span data-stu-id="3eafc-120">If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-121">STDEV<em>(псевдоним главы.</em><em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="3eafc-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="3eafc-122">Вычисляет стандартное отклонение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="3eafc-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-123">ANY<em>(псевдоним главы.</em><em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="3eafc-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="3eafc-124">Значение указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="3eafc-124">A value of the specified column.</span></span> <span data-ttu-id="3eafc-125">ANY имеет предсказуемое значение только в том случае, если значение столбца одинаково для всех строк в главе.</span><span class="sxs-lookup"><span data-stu-id="3eafc-125">ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="3eafc-126"><strong>ПРИМЕЧАНИЕ.</strong>Если в столбце не содержится одинаковое значение для всех строк в главе, команда SHAPE произвольно возвращает одно из значений для значения функции ANY.</span><span class="sxs-lookup"><span data-stu-id="3eafc-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
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
<th><p><span data-ttu-id="3eafc-127">Вычислимая экспрессия</span><span class="sxs-lookup"><span data-stu-id="3eafc-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="3eafc-128">Description</span><span class="sxs-lookup"><span data-stu-id="3eafc-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-129">CALC<em>(выражение)</em></span><span class="sxs-lookup"><span data-stu-id="3eafc-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="3eafc-130">Вычисляет произвольное выражение, но только в строке <strong>Recordset,</strong> содержащей функцию CALC.</span><span class="sxs-lookup"><span data-stu-id="3eafc-130">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function.</span></span> <span data-ttu-id="3eafc-131">Любое выражение с <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений (VBA) Функции</a> разрешено.</span><span class="sxs-lookup"><span data-stu-id="3eafc-131">Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
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
<th><p><span data-ttu-id="3eafc-132">Ключевое слово NEW</span><span class="sxs-lookup"><span data-stu-id="3eafc-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="3eafc-133">Description</span><span class="sxs-lookup"><span data-stu-id="3eafc-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-134">NEW <em>field-type</em> [(<em>ошибка</em>точности масштабирования  |  <em></em>  |  <em></em>  |  <em></em> ширины [, <em>ошибка</em>  |  <em>масштабирования])]</em></span><span class="sxs-lookup"><span data-stu-id="3eafc-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="3eafc-135">Добавляет пустой столбец указанного типа в <strong>набор Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="3eafc-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="3eafc-136">Тип *поля, переданный* с помощью ключевого слова NEW, может быть любым из следующих типов данных.</span><span class="sxs-lookup"><span data-stu-id="3eafc-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3eafc-137">Типы данных OLE DB</span><span class="sxs-lookup"><span data-stu-id="3eafc-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="3eafc-138">Эквивалент типа данных ADO (s)</span><span class="sxs-lookup"><span data-stu-id="3eafc-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="3eafc-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="3eafc-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="3eafc-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="3eafc-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="3eafc-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="3eafc-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="3eafc-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="3eafc-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="3eafc-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="3eafc-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="3eafc-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="3eafc-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="3eafc-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="3eafc-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="3eafc-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="3eafc-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="3eafc-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="3eafc-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="3eafc-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="3eafc-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="3eafc-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="3eafc-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="3eafc-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="3eafc-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="3eafc-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="3eafc-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="3eafc-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="3eafc-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="3eafc-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="3eafc-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="3eafc-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="3eafc-160">adBinary, AdVarBinary, adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="3eafc-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="3eafc-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="3eafc-162">adChar, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="3eafc-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="3eafc-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="3eafc-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="3eafc-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="3eafc-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="3eafc-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="3eafc-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="3eafc-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="3eafc-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="3eafc-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="3eafc-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="3eafc-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="3eafc-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="3eafc-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="3eafc-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="3eafc-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="3eafc-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="3eafc-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="3eafc-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="3eafc-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="3eafc-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="3eafc-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="3eafc-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="3eafc-178">adError</span><span class="sxs-lookup"><span data-stu-id="3eafc-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3eafc-179">Когда новое поле имеет десятичной тип (в OLE DB, DBTYPE \_ DECIMAL или в ADO, adDecimal), необходимо указать точность и значения масштабирования.</span><span class="sxs-lookup"><span data-stu-id="3eafc-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

