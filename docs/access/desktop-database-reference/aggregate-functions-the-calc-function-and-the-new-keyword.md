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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718051"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="599d6-102">Агрегатные функции, функция CALC и ключевое слово NEW</span><span class="sxs-lookup"><span data-stu-id="599d6-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="599d6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="599d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="599d6-104">Формирование данных поддерживает следующие функции.</span><span class="sxs-lookup"><span data-stu-id="599d6-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="599d6-105">Имя, присвоенное главы, содержащую столбец, чтобы работать — это *псевдоним главы*.</span><span class="sxs-lookup"><span data-stu-id="599d6-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="599d6-106">Псевдонима главы может быть полным, состоящий из каждой главы имя столбца, приводя к главе, содержащая *имя столбца,* все разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="599d6-106">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods.</span></span> <span data-ttu-id="599d6-107">Например если главе родительского chap1, содержит дочерних главы, chap2, которая содержит столбец Сумма, сумма, а затем полным именем будет chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="599d6-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="599d6-108">Агрегатные функции</span><span class="sxs-lookup"><span data-stu-id="599d6-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="599d6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="599d6-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="599d6-110">Сумма (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="599d6-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="599d6-111">Вычисление суммы всех значений в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="599d6-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-112">AVG (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="599d6-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="599d6-113">Вычисляет среднее значение указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="599d6-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-114">Максимальное число (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="599d6-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="599d6-115">Вычисляет максимальное значение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="599d6-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-116">MIN (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="599d6-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="599d6-117">Вычисляет минимальное значение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="599d6-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-118">COUNT (<em>псевдоним главы</em>[.<em> Имя столбца</em>])</span><span class="sxs-lookup"><span data-stu-id="599d6-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="599d6-119">Подсчитывает количество строк в указанном псевдоним.</span><span class="sxs-lookup"><span data-stu-id="599d6-119">Counts the number of rows in the specified alias.</span></span> <span data-ttu-id="599d6-120">Если столбец указан, только строки, для которых этот столбец не равно Null включаются в подсчет.</span><span class="sxs-lookup"><span data-stu-id="599d6-120">If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-121">STDEV (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="599d6-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="599d6-122">Вычисляет стандартное отклонение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="599d6-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-123">ЛЮБОЙ (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="599d6-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="599d6-124">Значение указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="599d6-124">A value of the specified column.</span></span> <span data-ttu-id="599d6-125">Какие-либо имеет значение прогнозируемый только в том случае, если значение столбца является общим для всех строк в главе.</span><span class="sxs-lookup"><span data-stu-id="599d6-125">ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="599d6-126"><strong>Примечание</strong>: Если столбец не содержит такое же значение для всех строк в главе, команда ФИГУРЫ произвольно возвращает одно из значений в качестве значения любой функции.</span><span class="sxs-lookup"><span data-stu-id="599d6-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
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
<th><p><span data-ttu-id="599d6-127">Расчетного выражения</span><span class="sxs-lookup"><span data-stu-id="599d6-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="599d6-128">Описание</span><span class="sxs-lookup"><span data-stu-id="599d6-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="599d6-129">Вычисление (<em>выражение</em>)</span><span class="sxs-lookup"><span data-stu-id="599d6-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="599d6-130">Вычисляет произвольного выражения, но только в той строке <strong>набора записей</strong> , содержащий функция CALC.</span><span class="sxs-lookup"><span data-stu-id="599d6-130">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function.</span></span> <span data-ttu-id="599d6-131">Любое выражение, с помощью этих <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений (VBA) функции</a> разрешены.</span><span class="sxs-lookup"><span data-stu-id="599d6-131">Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
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
<th><p><span data-ttu-id="599d6-132">НОВОЕ ключевое слово</span><span class="sxs-lookup"><span data-stu-id="599d6-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="599d6-133">Описание</span><span class="sxs-lookup"><span data-stu-id="599d6-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="599d6-134">НОВЫЙ <em>Тип поля</em> [(<em>Ширина</em> | <em>масштаба</em> | <em>точности</em> | <em>Ошибка</em> [, <em>масштаба</em> | <em>Ошибка</em>])]</span><span class="sxs-lookup"><span data-stu-id="599d6-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="599d6-135">Добавляет пустой столбец указанного типа <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="599d6-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="599d6-136">*Тип поля* , переданные с НОВЫМ ключевым словом может быть любой из следующих типов данных.</span><span class="sxs-lookup"><span data-stu-id="599d6-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="599d6-137">Типы данных OLE DB </span><span class="sxs-lookup"><span data-stu-id="599d6-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="599d6-138">Тип данных ADO equivalent(s)</span><span class="sxs-lookup"><span data-stu-id="599d6-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="599d6-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="599d6-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="599d6-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="599d6-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="599d6-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="599d6-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="599d6-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="599d6-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="599d6-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="599d6-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="599d6-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="599d6-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="599d6-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="599d6-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="599d6-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="599d6-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="599d6-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="599d6-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="599d6-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="599d6-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="599d6-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="599d6-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="599d6-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="599d6-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="599d6-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="599d6-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="599d6-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="599d6-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="599d6-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="599d6-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="599d6-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="599d6-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="599d6-160">adBinary, AdVarBinary, adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="599d6-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="599d6-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="599d6-162">adChar, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="599d6-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="599d6-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="599d6-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="599d6-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="599d6-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="599d6-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="599d6-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="599d6-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="599d6-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="599d6-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="599d6-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="599d6-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="599d6-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="599d6-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="599d6-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="599d6-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="599d6-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="599d6-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="599d6-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="599d6-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="599d6-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="599d6-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="599d6-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="599d6-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="599d6-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="599d6-178">adError</span><span class="sxs-lookup"><span data-stu-id="599d6-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="599d6-179">Если новое поле имеет тип decimal (в OLE DB DBTYPE\_DECIMAL, или в ADO, adDecimal), необходимо указать значения точности и масштаба.</span><span class="sxs-lookup"><span data-stu-id="599d6-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

