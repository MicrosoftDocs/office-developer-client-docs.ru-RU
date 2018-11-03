---
title: Эквивалентные типы данных ANSI SQL
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d1a07e3a7565e15fc5689bf73fe066a3529d3234
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946281"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="25b56-102">Эквивалентные типы данных ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="25b56-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="25b56-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="25b56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25b56-104">В следующей таблице перечислены типы данных ANSI SQL, эквивалентные им типы данных ядра базы данных Microsoft Access SQL и допустимые синонимы.</span><span class="sxs-lookup"><span data-stu-id="25b56-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="25b56-105">Он также приведены эквивалентные типы данных Microsoft SQL Server™.</span><span class="sxs-lookup"><span data-stu-id="25b56-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25b56-106">Тип данных ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="25b56-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="25b56-107">Тип данных Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="25b56-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="25b56-108">Синоним</span><span class="sxs-lookup"><span data-stu-id="25b56-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="25b56-109">Тип данных Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="25b56-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25b56-110">BIT, ИЗМЕНЕНИЕ БИТА</span><span class="sxs-lookup"><span data-stu-id="25b56-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="25b56-111">ДВОИЧНЫЙ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-112">VARBINARY ДВОИЧНЫЕ МЕНЯЮЩЕГОСЯ ИЗМЕНЕНИЕ БИТА</span><span class="sxs-lookup"><span data-stu-id="25b56-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="25b56-113">ДВОИЧНЫЙ VARBINARY</span><span class="sxs-lookup"><span data-stu-id="25b56-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25b56-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="25b56-115">БИТ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-116">ЛОГИЧЕСКОЕ ЗНАЧЕНИЕ, ЛОГИЧЕСКИХ, ЛОГИЧЕСКОЕ_ЗНАЧЕНИЕ1, YESNO</span><span class="sxs-lookup"><span data-stu-id="25b56-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="25b56-117">БИТ</span><span class="sxs-lookup"><span data-stu-id="25b56-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25b56-118">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="25b56-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="25b56-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="25b56-120">INTEGER1 БАЙТ</span><span class="sxs-lookup"><span data-stu-id="25b56-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="25b56-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="25b56-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25b56-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="25b56-123">СЧЕТЧИК (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-124">АВТОУВЕЛИЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25b56-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="25b56-125">(См. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25b56-126">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="25b56-127">ДЕНЬГИ</span><span class="sxs-lookup"><span data-stu-id="25b56-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="25b56-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="25b56-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="25b56-129">ДЕНЬГИ</span><span class="sxs-lookup"><span data-stu-id="25b56-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25b56-130">ДАТА, ВРЕМЯ, МЕТКИ ВРЕМЕНИ</span><span class="sxs-lookup"><span data-stu-id="25b56-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="25b56-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="25b56-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="25b56-132">Дата и время СОЗДАНИЯ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="25b56-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25b56-134">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="25b56-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="25b56-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="25b56-136">GUID</span><span class="sxs-lookup"><span data-stu-id="25b56-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="25b56-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="25b56-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25b56-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="25b56-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="25b56-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="25b56-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="25b56-140">ЧИСЛОВЫЕ, ДЕК</span><span class="sxs-lookup"><span data-stu-id="25b56-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="25b56-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="25b56-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25b56-142">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="25b56-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="25b56-143">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="25b56-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="25b56-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="25b56-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="25b56-145">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="25b56-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25b56-146">ДВОЙНОЙ ТОЧНОСТИ С ПЛАВАЮЩЕЙ ЗАПЯТОЙ</span><span class="sxs-lookup"><span data-stu-id="25b56-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="25b56-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="25b56-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="25b56-148">Данные типа DOUBLE, FLOAT8, IEEEDOUBLE, номер (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="25b56-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25b56-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="25b56-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="25b56-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="25b56-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="25b56-152">SHORT INTEGER2</span><span class="sxs-lookup"><span data-stu-id="25b56-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="25b56-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="25b56-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25b56-154">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="25b56-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="25b56-155">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="25b56-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="25b56-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="25b56-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="25b56-157">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="25b56-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25b56-158">ИНТЕРВАЛ</span><span class="sxs-lookup"><span data-stu-id="25b56-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="25b56-159">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="25b56-160">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25b56-161">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="25b56-162">ИЗОБРАЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25b56-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="25b56-163">OLEOBJECT LONGBINARY, ОБЩЕЕ,</span><span class="sxs-lookup"><span data-stu-id="25b56-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="25b56-164">ИЗОБРАЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25b56-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25b56-165">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25b56-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="25b56-166">ТЕКСТ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-167">LONGTEXT, LONGCHAR, ЗАМЕТКА, примечание, NTEXT (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-168">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="25b56-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25b56-169">СИМВОЛ, РАЗЛИЧНАЯ СИМВОЛ, НАЦИОНАЛЬНЫЙ СИМВОЛ МЕНЯЮЩЕГОСЯ НАЦИОНАЛЬНЫЙ СИМВОЛОВ</span><span class="sxs-lookup"><span data-stu-id="25b56-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="25b56-170">ЗНАКОВ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-171">Text(n) буквы, символов, строка, VARCHAR, VARYING символ, NCHAR, НАЦИОНАЛЬНЫЙ символ, НАЦИОНАЛЬНЫЙ символ, VARYING НАЦИОНАЛЬНЫЙ символ, НАЦИОНАЛЬНЫЙ ЗНАКОВ VARYING (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="25b56-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="25b56-172">СИМВОЛ, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="25b56-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="25b56-173">Тип данных ANSI SQL BIT не соответствует типа данных Microsoft Access SQL BIT.</span><span class="sxs-lookup"><span data-stu-id="25b56-173">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type.</span></span> <span data-ttu-id="25b56-174">Он соответствует типу ДВОИЧНЫХ данных вместо этого.</span><span class="sxs-lookup"><span data-stu-id="25b56-174">It corresponds to the BINARY data type instead.</span></span> <span data-ttu-id="25b56-175">Для типа данных Microsoft Access SQL РАЗРЯДНАЯ эквивалентно не ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="25b56-175">There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="25b56-176">Метка времени больше не поддерживается как синоним для даты и времени.</span><span class="sxs-lookup"><span data-stu-id="25b56-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="25b56-177">ЧИСЛОВОЙ больше не поддерживается как синоним с плавающей запятой или DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="25b56-177">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE.</span></span> <span data-ttu-id="25b56-178">ЧИСЛОВОЙ теперь используется как синоним для знаков после запятой.</span><span class="sxs-lookup"><span data-stu-id="25b56-178">NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="25b56-179">Поле LONGTEXT всегда хранятся в формате Юникод представления.</span><span class="sxs-lookup"><span data-stu-id="25b56-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="25b56-180">Если тип данных, имя, которое TEXT используется без указания длины, например TEXT(25), создается поле LONGTEXT.</span><span class="sxs-lookup"><span data-stu-id="25b56-180">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created.</span></span> <span data-ttu-id="25b56-181">Это позволяет написать, приведет к типов данных, схожих с Microsoft SQL Server [инструкции CREATE TABLE](create-table-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="25b56-181">This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="25b56-182">Поле символов всегда хранится в формате представления Unicode эквивалентен параметру типа данных НАЦИОНАЛЬНЫЙ ЗНАКОВ ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="25b56-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="25b56-183">Если имя типа данных TEXT используется с указанием длины, например TEXT(25), тип данных поля эквивалентно тип данных (знак).</span><span class="sxs-lookup"><span data-stu-id="25b56-183">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type.</span></span> <span data-ttu-id="25b56-184">Это позволяет сохранить обратной совместимости для большинства приложений Microsoft Jet, обеспечивая тип данных TEXT (без указания длины) для совместимости с Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="25b56-184">This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


