---
title: Типы данных SQL эквивалентный ANSI
TOCTitle: Equivalent ANSI SQL Data Types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ed13aab8d1f6851dd05ea2d79877e34c14665a3f
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937164"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="b08f1-102">Типы данных SQL эквивалентный ANSI</span><span class="sxs-lookup"><span data-stu-id="b08f1-102">Equivalent ANSI SQL Data Types</span></span>


<span data-ttu-id="b08f1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b08f1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b08f1-104">В следующей таблице перечислены типы данных ANSI SQL, эквивалентные им типы данных ядра базы данных Microsoft Access SQL и допустимые синонимы.</span><span class="sxs-lookup"><span data-stu-id="b08f1-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="b08f1-105">Он также приведены эквивалентные типы данных Microsoft SQL Server™.</span><span class="sxs-lookup"><span data-stu-id="b08f1-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b08f1-106">Тип данных ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="b08f1-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="b08f1-107">Тип данных Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="b08f1-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="b08f1-108">Синоним</span><span class="sxs-lookup"><span data-stu-id="b08f1-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="b08f1-109">Тип данных Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="b08f1-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b08f1-110">BIT, ИЗМЕНЕНИЕ БИТА</span><span class="sxs-lookup"><span data-stu-id="b08f1-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="b08f1-111">ДВОИЧНЫЙ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-112">VARBINARY ДВОИЧНЫЕ МЕНЯЮЩЕГОСЯ ИЗМЕНЕНИЕ БИТА</span><span class="sxs-lookup"><span data-stu-id="b08f1-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="b08f1-113">ДВОИЧНЫЙ VARBINARY</span><span class="sxs-lookup"><span data-stu-id="b08f1-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b08f1-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b08f1-115">БИТ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-116">ЛОГИЧЕСКОЕ ЗНАЧЕНИЕ, ЛОГИЧЕСКИХ, ЛОГИЧЕСКОЕ_ЗНАЧЕНИЕ1, YESNO</span><span class="sxs-lookup"><span data-stu-id="b08f1-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="b08f1-117">БИТ</span><span class="sxs-lookup"><span data-stu-id="b08f1-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b08f1-118">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b08f1-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="b08f1-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="b08f1-120">INTEGER1 БАЙТ</span><span class="sxs-lookup"><span data-stu-id="b08f1-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="b08f1-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="b08f1-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b08f1-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b08f1-123">СЧЕТЧИК (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-124">АВТОУВЕЛИЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b08f1-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="b08f1-125">(См. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b08f1-126">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b08f1-127">ДЕНЬГИ</span><span class="sxs-lookup"><span data-stu-id="b08f1-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="b08f1-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="b08f1-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="b08f1-129">ДЕНЬГИ</span><span class="sxs-lookup"><span data-stu-id="b08f1-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b08f1-130">ДАТА, ВРЕМЯ, МЕТКИ ВРЕМЕНИ</span><span class="sxs-lookup"><span data-stu-id="b08f1-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="b08f1-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="b08f1-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="b08f1-132">Дата и время СОЗДАНИЯ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="b08f1-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b08f1-134">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b08f1-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="b08f1-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="b08f1-136">GUID</span><span class="sxs-lookup"><span data-stu-id="b08f1-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="b08f1-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="b08f1-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b08f1-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b08f1-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="b08f1-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b08f1-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="b08f1-140">ЧИСЛОВЫЕ, ДЕК</span><span class="sxs-lookup"><span data-stu-id="b08f1-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="b08f1-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b08f1-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b08f1-142">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="b08f1-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="b08f1-143">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="b08f1-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="b08f1-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="b08f1-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="b08f1-145">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="b08f1-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b08f1-146">ДВОЙНОЙ ТОЧНОСТИ С ПЛАВАЮЩЕЙ ЗАПЯТОЙ</span><span class="sxs-lookup"><span data-stu-id="b08f1-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="b08f1-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b08f1-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="b08f1-148">Данные типа DOUBLE, FLOAT8, IEEEDOUBLE, номер (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b08f1-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b08f1-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="b08f1-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="b08f1-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="b08f1-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="b08f1-152">SHORT INTEGER2</span><span class="sxs-lookup"><span data-stu-id="b08f1-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="b08f1-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="b08f1-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b08f1-154">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="b08f1-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="b08f1-155">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="b08f1-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="b08f1-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="b08f1-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="b08f1-157">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="b08f1-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b08f1-158">ИНТЕРВАЛ</span><span class="sxs-lookup"><span data-stu-id="b08f1-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="b08f1-159">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b08f1-160">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b08f1-161">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b08f1-162">ИЗОБРАЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b08f1-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="b08f1-163">OLEOBJECT LONGBINARY, ОБЩЕЕ,</span><span class="sxs-lookup"><span data-stu-id="b08f1-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="b08f1-164">ИЗОБРАЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b08f1-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b08f1-165">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b08f1-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="b08f1-166">ТЕКСТ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-167">LONGTEXT, LONGCHAR, ЗАМЕТКА, примечание, NTEXT (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-168">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="b08f1-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b08f1-169">СИМВОЛ, РАЗЛИЧНАЯ СИМВОЛ, НАЦИОНАЛЬНЫЙ СИМВОЛ МЕНЯЮЩЕГОСЯ НАЦИОНАЛЬНЫЙ СИМВОЛОВ</span><span class="sxs-lookup"><span data-stu-id="b08f1-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="b08f1-170">ЗНАКОВ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-171">Text(n) буквы, символов, строка, VARCHAR, VARYING символ, NCHAR, НАЦИОНАЛЬНЫЙ символ, НАЦИОНАЛЬНЫЙ символ, VARYING НАЦИОНАЛЬНЫЙ символ, НАЦИОНАЛЬНЫЙ ЗНАКОВ VARYING (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="b08f1-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b08f1-172">СИМВОЛ, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="b08f1-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="b08f1-173">Тип данных ANSI SQL BIT не соответствует типа данных Microsoft Access SQL BIT.</span><span class="sxs-lookup"><span data-stu-id="b08f1-173">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type.</span></span> <span data-ttu-id="b08f1-174">Он соответствует типу ДВОИЧНЫХ данных вместо этого.</span><span class="sxs-lookup"><span data-stu-id="b08f1-174">It corresponds to the BINARY data type instead.</span></span> <span data-ttu-id="b08f1-175">Для типа данных Microsoft Access SQL РАЗРЯДНАЯ эквивалентно не ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="b08f1-175">There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="b08f1-176">Метка времени больше не поддерживается как синоним для даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b08f1-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="b08f1-177">ЧИСЛОВОЙ больше не поддерживается как синоним с плавающей запятой или DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="b08f1-177">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE.</span></span> <span data-ttu-id="b08f1-178">ЧИСЛОВОЙ теперь используется как синоним для знаков после запятой.</span><span class="sxs-lookup"><span data-stu-id="b08f1-178">NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="b08f1-179">Поле LONGTEXT всегда хранятся в формате Юникод представления.</span><span class="sxs-lookup"><span data-stu-id="b08f1-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="b08f1-180">Если тип данных, имя, которое TEXT используется без указания длины, например TEXT(25), создается поле LONGTEXT.</span><span class="sxs-lookup"><span data-stu-id="b08f1-180">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created.</span></span> <span data-ttu-id="b08f1-181">Это позволяет написать, приведет к типов данных, схожих с Microsoft SQL Server [инструкции CREATE TABLE](create-table-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="b08f1-181">This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="b08f1-182">Поле символов всегда хранится в формате представления Unicode эквивалентен параметру типа данных НАЦИОНАЛЬНЫЙ ЗНАКОВ ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="b08f1-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="b08f1-183">Если имя типа данных TEXT используется с указанием длины, например TEXT(25), тип данных поля эквивалентно тип данных (знак).</span><span class="sxs-lookup"><span data-stu-id="b08f1-183">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type.</span></span> <span data-ttu-id="b08f1-184">Это позволяет сохранить обратной совместимости для большинства приложений Microsoft Jet, обеспечивая тип данных TEXT (без указания длины) для совместимости с Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b08f1-184">This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


