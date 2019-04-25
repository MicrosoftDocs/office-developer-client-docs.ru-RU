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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293513"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="09433-102">Эквивалентные типы данных ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="09433-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="09433-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09433-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09433-104">В следующей таблице перечислены типы данных ANSI SQL, эквивалентные типы данных SQL ядра СУБД Microsoft Access и допустимые синонимы.</span><span class="sxs-lookup"><span data-stu-id="09433-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="09433-105">В ней также перечислены эквивалентные типы данных Microsoft SQL Server™.</span><span class="sxs-lookup"><span data-stu-id="09433-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09433-106">Тип данных ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="09433-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="09433-107">Тип данных Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="09433-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="09433-108">Синоним</span><span class="sxs-lookup"><span data-stu-id="09433-108">Synonym lookup</span></span></p></th>
<th><p><span data-ttu-id="09433-109">Тип данных Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="09433-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09433-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="09433-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="09433-111">BINARY (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-112">VARBINARY, BINARY VARYING BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="09433-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="09433-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="09433-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09433-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="09433-115">BIT (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="09433-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="09433-117">BIT</span><span class="sxs-lookup"><span data-stu-id="09433-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09433-118">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="09433-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="09433-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="09433-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="09433-120">INTEGER1 — See BYTE</span></span></p></td>
<td><p><span data-ttu-id="09433-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="09433-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09433-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="09433-123">COUNTER (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="09433-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="09433-125">(См. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09433-126">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="09433-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="09433-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="09433-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="09433-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="09433-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="09433-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09433-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="09433-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="09433-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="09433-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="09433-132">DATE, TIME (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="09433-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09433-134">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="09433-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="09433-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="09433-136">GUID</span><span class="sxs-lookup"><span data-stu-id="09433-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="09433-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="09433-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09433-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="09433-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="09433-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="09433-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="09433-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="09433-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="09433-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="09433-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09433-142">REAL</span><span class="sxs-lookup"><span data-stu-id="09433-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="09433-143">REAL</span><span class="sxs-lookup"><span data-stu-id="09433-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="09433-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="09433-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="09433-145">REAL</span><span class="sxs-lookup"><span data-stu-id="09433-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09433-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="09433-146">Double precision float</span></span></p></td>
<td><p><span data-ttu-id="09433-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="09433-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="09433-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="09433-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09433-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="09433-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="09433-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="09433-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="09433-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="09433-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="09433-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="09433-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09433-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="09433-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="09433-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="09433-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="09433-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="09433-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="09433-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="09433-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09433-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="09433-158">Interval</span></span></p></td>
<td><p><span data-ttu-id="09433-159">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="09433-160">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09433-161">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="09433-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="09433-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="09433-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="09433-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="09433-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="09433-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09433-165">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09433-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="09433-166">TEXT (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="09433-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09433-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="09433-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="09433-170">CHAR (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="09433-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="09433-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="09433-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="09433-173">Тип данных BIT ANSI SQL не соответствует типу данных BIT Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="09433-173">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type.</span></span> <span data-ttu-id="09433-174">Он соответствует типу данных BINARY.</span><span class="sxs-lookup"><span data-stu-id="09433-174">It corresponds to the BINARY data type instead.</span></span> <span data-ttu-id="09433-175">Для типа данных BIT Microsoft Access SQL отсутствует эквивалент ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="09433-175">There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="09433-176">TIMESTAMP больше не поддерживается в качестве синонима для DATETIME.</span><span class="sxs-lookup"><span data-stu-id="09433-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="09433-177">NUMERIC больше не поддерживается в качестве синонима для FLOAT или DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="09433-177">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE.</span></span> <span data-ttu-id="09433-178">NUMERIC теперь используется в качестве синонима для DECIMAL.</span><span class="sxs-lookup"><span data-stu-id="09433-178">NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="09433-179">Поле LONGTEXT всегда хранится в формате представления Юникода.</span><span class="sxs-lookup"><span data-stu-id="09433-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="09433-180">Если тип данных TEXT используется без указания необязательной длины, например TEXT(25), создается поле LONGTEXT.</span><span class="sxs-lookup"><span data-stu-id="09433-180">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created.</span></span> <span data-ttu-id="09433-181">Это позволяет записывать [операторы CREATE TABLE](create-table-statement-microsoft-access-sql.md), возвращающие типы данных, которые соответствуют Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="09433-181">This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="09433-182">Поле CHAR всегда хранится в формате представления Юникода, что соответствует типу данных NATIONAL CHAR ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="09433-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="09433-183">Если тип данных TEXT используется с указанием необязательной длины, например TEXT(25), тип данных поля эквивалентен типу данных CHAR.</span><span class="sxs-lookup"><span data-stu-id="09433-183">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type.</span></span> <span data-ttu-id="09433-184">Это сохраняет обратную совместимость для большинства приложений Microsoft Jet, позволяя сопоставлять тип данных TEXT (без указания длины) с Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="09433-184">This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


