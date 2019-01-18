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
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699382"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="ae08a-102">Эквивалентные типы данных ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="ae08a-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="ae08a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae08a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae08a-104">В следующей таблице перечислены типы данных ANSI SQL, эквивалентные им типы данных ядра базы данных Microsoft Access SQL и допустимые синонимы.</span><span class="sxs-lookup"><span data-stu-id="ae08a-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="ae08a-105">Он также приведены эквивалентные типы данных Microsoft SQL Server™.</span><span class="sxs-lookup"><span data-stu-id="ae08a-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae08a-106">Тип данных ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="ae08a-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="ae08a-107">Тип данных Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="ae08a-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="ae08a-108">Синоним</span><span class="sxs-lookup"><span data-stu-id="ae08a-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="ae08a-109">Тип данных Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ae08a-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae08a-110">BIT, ИЗМЕНЕНИЕ БИТА</span><span class="sxs-lookup"><span data-stu-id="ae08a-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="ae08a-111">ДВОИЧНЫЙ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-112">VARBINARY ДВОИЧНЫЕ МЕНЯЮЩЕГОСЯ ИЗМЕНЕНИЕ БИТА</span><span class="sxs-lookup"><span data-stu-id="ae08a-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="ae08a-113">ДВОИЧНЫЙ VARBINARY</span><span class="sxs-lookup"><span data-stu-id="ae08a-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae08a-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ae08a-115">БИТ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-116">ЛОГИЧЕСКОЕ ЗНАЧЕНИЕ, ЛОГИЧЕСКИХ, ЛОГИЧЕСКОЕ_ЗНАЧЕНИЕ1, YESNO</span><span class="sxs-lookup"><span data-stu-id="ae08a-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="ae08a-117">БИТ</span><span class="sxs-lookup"><span data-stu-id="ae08a-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae08a-118">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ae08a-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="ae08a-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="ae08a-120">INTEGER1 БАЙТ</span><span class="sxs-lookup"><span data-stu-id="ae08a-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="ae08a-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="ae08a-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae08a-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ae08a-123">СЧЕТЧИК (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-124">АВТОУВЕЛИЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae08a-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="ae08a-125">(См. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae08a-126">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ae08a-127">ДЕНЬГИ</span><span class="sxs-lookup"><span data-stu-id="ae08a-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="ae08a-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="ae08a-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="ae08a-129">ДЕНЬГИ</span><span class="sxs-lookup"><span data-stu-id="ae08a-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae08a-130">ДАТА, ВРЕМЯ, МЕТКИ ВРЕМЕНИ</span><span class="sxs-lookup"><span data-stu-id="ae08a-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="ae08a-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="ae08a-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="ae08a-132">Дата и время СОЗДАНИЯ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="ae08a-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae08a-134">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ae08a-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="ae08a-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="ae08a-136">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="ae08a-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="ae08a-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="ae08a-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae08a-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="ae08a-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="ae08a-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="ae08a-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="ae08a-140">ЧИСЛОВЫЕ, ДЕК</span><span class="sxs-lookup"><span data-stu-id="ae08a-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="ae08a-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="ae08a-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae08a-142">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="ae08a-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="ae08a-143">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="ae08a-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="ae08a-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="ae08a-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="ae08a-145">РЕАЛЬНЫЕ</span><span class="sxs-lookup"><span data-stu-id="ae08a-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae08a-146">ДВОЙНОЙ ТОЧНОСТИ С ПЛАВАЮЩЕЙ ЗАПЯТОЙ</span><span class="sxs-lookup"><span data-stu-id="ae08a-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="ae08a-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ae08a-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="ae08a-148">Данные типа DOUBLE, FLOAT8, IEEEDOUBLE, номер (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ae08a-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae08a-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="ae08a-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="ae08a-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="ae08a-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="ae08a-152">SHORT INTEGER2</span><span class="sxs-lookup"><span data-stu-id="ae08a-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="ae08a-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="ae08a-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae08a-154">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="ae08a-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="ae08a-155">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="ae08a-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="ae08a-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="ae08a-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="ae08a-157">ЦЕЛОЕ ЧИСЛО</span><span class="sxs-lookup"><span data-stu-id="ae08a-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae08a-158">ИНТЕРВАЛ</span><span class="sxs-lookup"><span data-stu-id="ae08a-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="ae08a-159">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ae08a-160">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae08a-161">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ae08a-162">ИЗОБРАЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae08a-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="ae08a-163">OLEOBJECT LONGBINARY, ОБЩЕЕ,</span><span class="sxs-lookup"><span data-stu-id="ae08a-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="ae08a-164">ИЗОБРАЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae08a-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae08a-165">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae08a-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="ae08a-166">ТЕКСТ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-167">LONGTEXT, LONGCHAR, ЗАМЕТКА, примечание, NTEXT (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-168">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="ae08a-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae08a-169">СИМВОЛ, РАЗЛИЧНАЯ СИМВОЛ, НАЦИОНАЛЬНЫЙ СИМВОЛ МЕНЯЮЩЕГОСЯ НАЦИОНАЛЬНЫЙ СИМВОЛОВ</span><span class="sxs-lookup"><span data-stu-id="ae08a-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="ae08a-170">ЗНАКОВ (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-171">Text(n) буквы, символов, строка, VARCHAR, VARYING символ, NCHAR, НАЦИОНАЛЬНЫЙ символ, НАЦИОНАЛЬНЫЙ символ, VARYING НАЦИОНАЛЬНЫЙ символ, НАЦИОНАЛЬНЫЙ ЗНАКОВ VARYING (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="ae08a-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="ae08a-172">СИМВОЛ, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="ae08a-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="ae08a-173">Тип данных ANSI SQL BIT не соответствует типа данных Microsoft Access SQL BIT.</span><span class="sxs-lookup"><span data-stu-id="ae08a-173">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type.</span></span> <span data-ttu-id="ae08a-174">Он соответствует типу ДВОИЧНЫХ данных вместо этого.</span><span class="sxs-lookup"><span data-stu-id="ae08a-174">It corresponds to the BINARY data type instead.</span></span> <span data-ttu-id="ae08a-175">Для типа данных Microsoft Access SQL РАЗРЯДНАЯ эквивалентно не ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="ae08a-175">There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="ae08a-176">Метка времени больше не поддерживается как синоним для даты и времени.</span><span class="sxs-lookup"><span data-stu-id="ae08a-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="ae08a-177">ЧИСЛОВОЙ больше не поддерживается как синоним с плавающей запятой или DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="ae08a-177">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE.</span></span> <span data-ttu-id="ae08a-178">ЧИСЛОВОЙ теперь используется как синоним для знаков после запятой.</span><span class="sxs-lookup"><span data-stu-id="ae08a-178">NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="ae08a-179">Поле LONGTEXT всегда хранятся в формате Юникод представления.</span><span class="sxs-lookup"><span data-stu-id="ae08a-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="ae08a-180">Если тип данных, имя, которое TEXT используется без указания длины, например TEXT(25), создается поле LONGTEXT.</span><span class="sxs-lookup"><span data-stu-id="ae08a-180">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created.</span></span> <span data-ttu-id="ae08a-181">Это позволяет написать, приведет к типов данных, схожих с Microsoft SQL Server [инструкции CREATE TABLE](create-table-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="ae08a-181">This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="ae08a-182">Поле символов всегда хранится в формате представления Unicode эквивалентен параметру типа данных НАЦИОНАЛЬНЫЙ ЗНАКОВ ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="ae08a-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="ae08a-183">Если имя типа данных TEXT используется с указанием длины, например TEXT(25), тип данных поля эквивалентно тип данных (знак).</span><span class="sxs-lookup"><span data-stu-id="ae08a-183">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type.</span></span> <span data-ttu-id="ae08a-184">Это позволяет сохранить обратной совместимости для большинства приложений Microsoft Jet, обеспечивая тип данных TEXT (без указания длины) для совместимости с Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ae08a-184">This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


