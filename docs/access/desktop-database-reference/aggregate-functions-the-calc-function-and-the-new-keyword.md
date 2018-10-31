---
title: Агрегатные функции, функция CALC и ключевое слово NEW
TOCTitle: Aggregate Functions, the CALC Function, and the NEW Keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8250d2a21f0c4a4d5af64310fc14f96f56a46b54
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860016"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="748a0-102">Агрегатные функции, функция CALC и ключевое слово NEW</span><span class="sxs-lookup"><span data-stu-id="748a0-102">Aggregate Functions, the CALC Function, and the NEW Keyword</span></span>


<span data-ttu-id="748a0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="748a0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="748a0-104">Формирование данных поддерживает следующие функции.</span><span class="sxs-lookup"><span data-stu-id="748a0-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="748a0-105">Имя, присвоенное главы, содержащую столбец, чтобы работать — это *псевдоним главы*.</span><span class="sxs-lookup"><span data-stu-id="748a0-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="748a0-106">Псевдонима главы может быть полным, состоящий из каждой главы имя столбца, приводя к главе, содержащая *имя столбца,* все разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="748a0-106">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods.</span></span> <span data-ttu-id="748a0-107">Например если главе родительского chap1, содержит дочерних главы, chap2, которая содержит столбец Сумма, сумма, а затем полным именем будет chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="748a0-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="748a0-108">Статистические функции</span><span class="sxs-lookup"><span data-stu-id="748a0-108">Aggregate Functions</span></span></p></th>
<th><p><span data-ttu-id="748a0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="748a0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="748a0-110">Сумма (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="748a0-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="748a0-111">Вычисление суммы всех значений в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="748a0-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-112">AVG (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="748a0-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="748a0-113">Вычисляет среднее значение указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="748a0-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-114">Максимальное число (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="748a0-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="748a0-115">Вычисляет максимальное значение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="748a0-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-116">MIN (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="748a0-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="748a0-117">Вычисляет минимальное значение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="748a0-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-118">COUNT (<em>псевдоним главы</em>[.<em> Имя столбца</em>])</span><span class="sxs-lookup"><span data-stu-id="748a0-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="748a0-119">Подсчитывает количество строк в указанном псевдоним.</span><span class="sxs-lookup"><span data-stu-id="748a0-119">Counts the number of rows in the specified alias.</span></span> <span data-ttu-id="748a0-120">Если столбец указан, только строки, для которых этот столбец не равно Null включаются в подсчет.</span><span class="sxs-lookup"><span data-stu-id="748a0-120">If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-121">STDEV (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="748a0-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="748a0-122">Вычисляет стандартное отклонение в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="748a0-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-123">ЛЮБОЙ (<em>псевдоним главы</em>.<em> Имя столбца</em>)</span><span class="sxs-lookup"><span data-stu-id="748a0-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="748a0-124">Значение указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="748a0-124">A value of the specified column.</span></span> <span data-ttu-id="748a0-125">Какие-либо имеет значение прогнозируемый только в том случае, если значение столбца является общим для всех строк в главе.</span><span class="sxs-lookup"><span data-stu-id="748a0-125">ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p>

> [!NOTE]
> <span data-ttu-id="748a0-126">Если столбец не содержит такое же значение для всех строк в главе, команда ФИГУРЫ произвольно возвращает одно из значений в качестве значения любой функции.</span><span class="sxs-lookup"><span data-stu-id="748a0-126">If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span>


<p></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="748a0-127">Расчетного выражения</span><span class="sxs-lookup"><span data-stu-id="748a0-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="748a0-128">Описание</span><span class="sxs-lookup"><span data-stu-id="748a0-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="748a0-129">Вычисление (<em>выражение</em>)</span><span class="sxs-lookup"><span data-stu-id="748a0-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="748a0-130">Вычисляет произвольного выражения, но только в той строке <strong>набора записей</strong> , содержащий функция CALC.</span><span class="sxs-lookup"><span data-stu-id="748a0-130">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function.</span></span> <span data-ttu-id="748a0-131">Любое выражение, с помощью этих <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений (VBA) функции</a> разрешены.</span><span class="sxs-lookup"><span data-stu-id="748a0-131">Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="748a0-132">НОВОЕ ключевое слово</span><span class="sxs-lookup"><span data-stu-id="748a0-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="748a0-133">Описание</span><span class="sxs-lookup"><span data-stu-id="748a0-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="748a0-134">НОВЫЙ <em>Тип поля</em> [(<em>Ширина</em> | <em>масштаба</em> | <em>точности</em> | <em>Ошибка</em> [, <em>масштаба</em> | <em>Ошибка</em>])]</span><span class="sxs-lookup"><span data-stu-id="748a0-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="748a0-135">Добавляет пустой столбец указанного типа <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="748a0-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="748a0-136">*Тип поля* , переданные с НОВЫМ ключевым словом может быть любой из следующих типов данных.</span><span class="sxs-lookup"><span data-stu-id="748a0-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="748a0-137">Типы данных OLE DB </span><span class="sxs-lookup"><span data-stu-id="748a0-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="748a0-138">Тип данных ADO equivalent(s)</span><span class="sxs-lookup"><span data-stu-id="748a0-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="748a0-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="748a0-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="748a0-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="748a0-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="748a0-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="748a0-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="748a0-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="748a0-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="748a0-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="748a0-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="748a0-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="748a0-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="748a0-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="748a0-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="748a0-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="748a0-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="748a0-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="748a0-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="748a0-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="748a0-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="748a0-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="748a0-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="748a0-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="748a0-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="748a0-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="748a0-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="748a0-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="748a0-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="748a0-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="748a0-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="748a0-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="748a0-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="748a0-160">adBinary, AdVarBinary, adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="748a0-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="748a0-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="748a0-162">adChar, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="748a0-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="748a0-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="748a0-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="748a0-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="748a0-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="748a0-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="748a0-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="748a0-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="748a0-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="748a0-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="748a0-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="748a0-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="748a0-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="748a0-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="748a0-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="748a0-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="748a0-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="748a0-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="748a0-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748a0-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="748a0-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="748a0-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="748a0-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748a0-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="748a0-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="748a0-178">adError</span><span class="sxs-lookup"><span data-stu-id="748a0-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="748a0-179">Если новое поле имеет тип decimal (в OLE DB DBTYPE\_DECIMAL, или в ADO, adDecimal), необходимо указать значения точности и масштаба.</span><span class="sxs-lookup"><span data-stu-id="748a0-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

