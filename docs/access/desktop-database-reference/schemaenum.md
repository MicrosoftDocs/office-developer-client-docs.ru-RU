---
title: SchemaEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308865"
---
# <a name="schemaenum"></a><span data-ttu-id="9a409-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="9a409-102">SchemaEnum</span></span>

<span data-ttu-id="9a409-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a409-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a409-104">Указывает тип наборов **записей** схемы, извлекаемого [методом OpenSchema.](openschema-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="9a409-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a409-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="9a409-105">Remarks</span></span>

<span data-ttu-id="9a409-106">Дополнительные сведения о функции и столбцах, возвращаемой для каждой константы ADO, можно найти в статьях приложения Б справочника по *программистам OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="9a409-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="9a409-107">Имя каждого раздела перечислены в скобки в разделе "Описание" следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="9a409-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="9a409-108">Дополнительные сведения о функции и столбцах, возвращаемой для каждой константы ADO MD, можно найти в разделах главы 23 документации *OLE DB для OLAP.*</span><span class="sxs-lookup"><span data-stu-id="9a409-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="9a409-109">Имя каждого раздела перечислены в скобки и помечены звездочкой ( ) в столбце \* "Описание" следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="9a409-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="9a409-110">Перевод типов данных столбцов в документации OLE DB в типы данных ADO, ссылаясь на столбец "Описание" статьи ADO [DataTypeEnum.](datatypeenum.md)</span><span class="sxs-lookup"><span data-stu-id="9a409-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="9a409-111">Например, тип данных OLE DB **типа DBTYPE \_ WSTR** эквивалентен типу данных ADO **adWChar.**</span><span class="sxs-lookup"><span data-stu-id="9a409-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="9a409-112">ADO создает результаты, похожие на схему, для констант **adSchemaDBInfoKeywords** и **adSchemaDBInfoLiterals.**</span><span class="sxs-lookup"><span data-stu-id="9a409-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="9a409-113">ADO создает набор записей, а затем заполняет каждую строку значениями, возвращенными соответственно методами **IDBInfo::GetKeywords** и **IDBInfo::GetLiteralInfo.**</span><span class="sxs-lookup"><span data-stu-id="9a409-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="9a409-114">Дополнительные сведения об этих методах можно найти в разделе IDBInfo справочника *по OLE DB Programmer.*</span><span class="sxs-lookup"><span data-stu-id="9a409-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a409-115">Константа</span><span class="sxs-lookup"><span data-stu-id="9a409-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="9a409-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9a409-116">Value</span></span></p></th>
<th><p><span data-ttu-id="9a409-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9a409-117">Description</span></span></p></th>
<th><p><span data-ttu-id="9a409-118">Столбцы ограничения</span><span class="sxs-lookup"><span data-stu-id="9a409-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a409-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-120">0</span><span class="sxs-lookup"><span data-stu-id="9a409-120">0</span></span></p></td>
<td><p><span data-ttu-id="9a409-121">Возвращает утверждения, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9a409-122">(ASSERTIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9a409-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9a409-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-127">1 </span><span class="sxs-lookup"><span data-stu-id="9a409-127">1</span></span></p></td>
<td><p><span data-ttu-id="9a409-128">Возвращает физические атрибуты, связанные с каталогами, доступными из DBMS.</span><span class="sxs-lookup"><span data-stu-id="9a409-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="9a409-129">(Набор строк CATALOGS)</span><span class="sxs-lookup"><span data-stu-id="9a409-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-132">2 </span><span class="sxs-lookup"><span data-stu-id="9a409-132">2</span></span></p></td>
<td><p><span data-ttu-id="9a409-133">Возвращает наборы символов, определенные в каталоге, доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9a409-134">(CHARACTER_SETS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="9a409-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="9a409-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-139">5 </span><span class="sxs-lookup"><span data-stu-id="9a409-139">5</span></span></p></td>
<td><p><span data-ttu-id="9a409-140">Возвращает ограничения проверки, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9a409-141">(CHECK_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9a409-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9a409-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-146">3 </span><span class="sxs-lookup"><span data-stu-id="9a409-146">3</span></span></p></td>
<td><p><span data-ttu-id="9a409-147">Возвращает знаки, определенные в каталоге, доступные для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a409-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9a409-148">(COLLATIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="9a409-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="9a409-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-153">13 </span><span class="sxs-lookup"><span data-stu-id="9a409-153">13</span></span></p></td>
<td><p><span data-ttu-id="9a409-154">Возвращает привилегии для столбцов таблиц, определенных в каталоге, доступных или предоставленных определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="9a409-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="9a409-155">(COLUMN_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-158">TABLE_NAME</span></span><br />
<span data-ttu-id="9a409-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="9a409-160">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="9a409-160">GRANTOR</span></span><br />
<span data-ttu-id="9a409-161">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="9a409-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-163">4 </span><span class="sxs-lookup"><span data-stu-id="9a409-163">4</span></span></p></td>
<td><p><span data-ttu-id="9a409-164">Возвращает столбцы таблиц (включая представления), определенные в каталоге, доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9a409-165">(Набор строк COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="9a409-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-168">TABLE_NAME</span></span><br />
<span data-ttu-id="9a409-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-171">11</span><span class="sxs-lookup"><span data-stu-id="9a409-171">11</span></span></p></td>
<td><p><span data-ttu-id="9a409-172">Возвращает столбцы, определенные в каталоге, которые зависят от домена, определенного в каталоге и принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="9a409-173">(COLUMN_DOMAIN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="9a409-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="9a409-176">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="9a409-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-179">6 </span><span class="sxs-lookup"><span data-stu-id="9a409-179">6</span></span></p></td>
<td><p><span data-ttu-id="9a409-180">Возвращает столбцы, используемые ограничениями, уникальными ограничениями, ограничениями проверки и утверждениями, определенными в каталоге и принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="9a409-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-184">TABLE_NAME</span></span><br />
<span data-ttu-id="9a409-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-187">7 </span><span class="sxs-lookup"><span data-stu-id="9a409-187">7</span></span></p></td>
<td><p><span data-ttu-id="9a409-188">Возвращает таблицы, используемые в ссылающихся ограничениях, уникальных ограничениях, ограничениях проверки и утверждениях, определенных в каталоге и владельцем определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a409-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="9a409-189">(CONSTRAINT_TABLE_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-194">32</span><span class="sxs-lookup"><span data-stu-id="9a409-194">32</span></span></p></td>
<td><p><span data-ttu-id="9a409-195">Возвращает сведения о доступных кубах в схеме (или каталоге, если поставщик не поддерживает схемы).</span><span class="sxs-lookup"><span data-stu-id="9a409-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="9a409-196">(КУБS Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="9a409-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="9a409-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9a409-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-201">30</span><span class="sxs-lookup"><span data-stu-id="9a409-201">30</span></span></p></td>
<td><p><span data-ttu-id="9a409-202">Возвращает список ключевых слов для конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="9a409-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="9a409-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="9a409-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-204">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="9a409-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-206">31</span><span class="sxs-lookup"><span data-stu-id="9a409-206">31</span></span></p></td>
<td><p><span data-ttu-id="9a409-207">Возвращает список специальных литералов, используемых в текстовых командах.</span><span class="sxs-lookup"><span data-stu-id="9a409-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="9a409-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="9a409-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-209">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="9a409-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-211">33</span><span class="sxs-lookup"><span data-stu-id="9a409-211">33</span></span></p></td>
<td><p><span data-ttu-id="9a409-212">Возвращает сведения о измерениях в заданном кубе.</span><span class="sxs-lookup"><span data-stu-id="9a409-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="9a409-213">У него есть одна строка для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="9a409-213">It has one row for each dimension.</span></span> <span data-ttu-id="9a409-214">(DIMENSIONS Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9a409-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="9a409-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9a409-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-217">CUBE_NAME</span></span><br />
<span data-ttu-id="9a409-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="9a409-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-221">27</span><span class="sxs-lookup"><span data-stu-id="9a409-221">27</span></span></p></td>
<td><p><span data-ttu-id="9a409-222">Возвращает столбцы внешнего ключа, определенные в каталоге определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="9a409-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="9a409-223">(FOREIGN_KEYS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="9a409-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-231">34</span><span class="sxs-lookup"><span data-stu-id="9a409-231">34</span></span></p></td>
<td><p><span data-ttu-id="9a409-232">Возвращает сведения об иерархиях, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="9a409-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="9a409-233">(HIERARCHIES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9a409-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="9a409-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9a409-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-236">CUBE_NAME</span></span><br />
<span data-ttu-id="9a409-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="9a409-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-241">12 </span><span class="sxs-lookup"><span data-stu-id="9a409-241">12</span></span></p></td>
<td><p><span data-ttu-id="9a409-242">Возвращает индексы, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9a409-243">(НАБОР строк INDEXES)</span><span class="sxs-lookup"><span data-stu-id="9a409-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-246">INDEX_NAME</span></span><br />
<span data-ttu-id="9a409-247">TYPE</span><span class="sxs-lookup"><span data-stu-id="9a409-247">TYPE</span></span><br />
<span data-ttu-id="9a409-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-250">8 </span><span class="sxs-lookup"><span data-stu-id="9a409-250">8</span></span></p></td>
<td><p><span data-ttu-id="9a409-251">Возвращает столбцы, определенные в каталоге и ограниченные в качестве ключей определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="9a409-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="9a409-252">(KEY_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9a409-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9a409-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="9a409-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-258">TABLE_NAME</span></span><br />
<span data-ttu-id="9a409-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-261">35</span><span class="sxs-lookup"><span data-stu-id="9a409-261">35</span></span></p></td>
<td><p><span data-ttu-id="9a409-262">Возвращает сведения об уровнях, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="9a409-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="9a409-263">(LEVELS Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="9a409-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="9a409-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9a409-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-266">CUBE_NAME</span></span><br />
<span data-ttu-id="9a409-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="9a409-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-272">36</span><span class="sxs-lookup"><span data-stu-id="9a409-272">36</span></span></p></td>
<td><p><span data-ttu-id="9a409-273">Возвращает сведения о доступных мерах.</span><span class="sxs-lookup"><span data-stu-id="9a409-273">Returns information about the available measures.</span></span> <span data-ttu-id="9a409-274">(MEASURES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9a409-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="9a409-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9a409-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-277">CUBE_NAME</span></span><br />
<span data-ttu-id="9a409-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="9a409-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-281">38</span><span class="sxs-lookup"><span data-stu-id="9a409-281">38</span></span></p></td>
<td><p><span data-ttu-id="9a409-282">Возвращает сведения о доступных членах.</span><span class="sxs-lookup"><span data-stu-id="9a409-282">Returns information about the available members.</span></span> <span data-ttu-id="9a409-283">(MEMBERS Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9a409-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="9a409-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9a409-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-286">CUBE_NAME</span></span><br />
<span data-ttu-id="9a409-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="9a409-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="9a409-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="9a409-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="9a409-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="9a409-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="9a409-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="9a409-295">Оператор дерева (дополнительные сведения см. в документации OLE DB для OLAP.)</span><span class="sxs-lookup"><span data-stu-id="9a409-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-297">28</span><span class="sxs-lookup"><span data-stu-id="9a409-297">28</span></span></p></td>
<td><p><span data-ttu-id="9a409-298">Возвращает столбцы первичного ключа, определенные в каталоге определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="9a409-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="9a409-299">(PRIMARY_KEYS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-304">29</span><span class="sxs-lookup"><span data-stu-id="9a409-304">29</span></span></p></td>
<td><p><span data-ttu-id="9a409-305">Возвращает сведения о столбцах строк, возвращаемой процедурами.</span><span class="sxs-lookup"><span data-stu-id="9a409-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="9a409-306">(PROCEDURE_COLUMNS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="9a409-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="9a409-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-312">26</span><span class="sxs-lookup"><span data-stu-id="9a409-312">26</span></span></p></td>
<td><p><span data-ttu-id="9a409-313">Возвращает сведения о параметрах и кодах возврата процедур.</span><span class="sxs-lookup"><span data-stu-id="9a409-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="9a409-314">(PROCEDURE_PARAMETERS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="9a409-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="9a409-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-320">16 </span><span class="sxs-lookup"><span data-stu-id="9a409-320">16</span></span></p></td>
<td><p><span data-ttu-id="9a409-321">Возвращает процедуры, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9a409-322">(НАБОР строк PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="9a409-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="9a409-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="9a409-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="9a409-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-328">37</span><span class="sxs-lookup"><span data-stu-id="9a409-328">37</span></span></p></td>
<td><p><span data-ttu-id="9a409-329">Возвращает сведения о доступных свойствах для каждого уровня измерения.</span><span class="sxs-lookup"><span data-stu-id="9a409-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="9a409-330">(PROPERTIES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="9a409-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="9a409-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="9a409-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9a409-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-333">CUBE_NAME</span></span><br />
<span data-ttu-id="9a409-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="9a409-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="9a409-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="9a409-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-341">–1</span><span class="sxs-lookup"><span data-stu-id="9a409-341">-1</span></span></p></td>
<td><p><span data-ttu-id="9a409-342">Используется, если поставщик определяет собственные нестандартные запросы схемы.</span><span class="sxs-lookup"><span data-stu-id="9a409-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="9a409-343">&lt;Конкретный поставщик&gt;</span><span class="sxs-lookup"><span data-stu-id="9a409-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-345">22</span><span class="sxs-lookup"><span data-stu-id="9a409-345">22</span></span></p></td>
<td><p><span data-ttu-id="9a409-346">Возвращает (базовые) типы данных, поддерживаемые поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="9a409-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="9a409-347">(PROVIDER_TYPES Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="9a409-348">DATA_TYPE</span></span><br />
<span data-ttu-id="9a409-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="9a409-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-351">9 </span><span class="sxs-lookup"><span data-stu-id="9a409-351">9</span></span></p></td>
<td><p><span data-ttu-id="9a409-352">Возвращает ограничения, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9a409-353">(REFERENTIAL_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9a409-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9a409-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-358">17 </span><span class="sxs-lookup"><span data-stu-id="9a409-358">17</span></span></p></td>
<td><p><span data-ttu-id="9a409-359">Возвращает схемы (объекты базы данных), которые принадлежат заданным пользователем.</span><span class="sxs-lookup"><span data-stu-id="9a409-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="9a409-360">(Набор строк SCHEMATA)</span><span class="sxs-lookup"><span data-stu-id="9a409-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="9a409-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="9a409-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="9a409-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-365">18 </span><span class="sxs-lookup"><span data-stu-id="9a409-365">18</span></span></p></td>
<td><p><span data-ttu-id="9a409-366">Возвращает уровни соответствия, параметры и диалекты, поддерживаемые SQL данных обработки, определенных в каталоге.</span><span class="sxs-lookup"><span data-stu-id="9a409-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="9a409-367">(SQL_LANGUAGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-368">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="9a409-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-370">19</span><span class="sxs-lookup"><span data-stu-id="9a409-370">19</span></span></p></td>
<td><p><span data-ttu-id="9a409-371">Возвращает статистику, заданную в каталоге, которая принадлежит определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9a409-372">(НАБОР строк СТАТИСТИКИ)</span><span class="sxs-lookup"><span data-stu-id="9a409-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-377">10 </span><span class="sxs-lookup"><span data-stu-id="9a409-377">10</span></span></p></td>
<td><p><span data-ttu-id="9a409-378">Возвращает ограничения таблицы, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="9a409-379">(TABLE_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="9a409-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="9a409-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="9a409-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-385">TABLE_NAME</span></span><br />
<span data-ttu-id="9a409-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="9a409-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-388">14 </span><span class="sxs-lookup"><span data-stu-id="9a409-388">14</span></span></p></td>
<td><p><span data-ttu-id="9a409-389">Возвращает привилегии в таблицах, определенных в каталоге, доступных или предоставленных определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="9a409-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="9a409-390">(TABLE_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-393">TABLE_NAME</span></span><br />
<span data-ttu-id="9a409-394">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="9a409-394">GRANTOR</span></span><br />
<span data-ttu-id="9a409-395">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="9a409-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-397">20</span><span class="sxs-lookup"><span data-stu-id="9a409-397">20</span></span></p></td>
<td><p><span data-ttu-id="9a409-398">Возвращает таблицы (включая представления), определенные в каталоге, доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9a409-399">(TABLES Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-402">TABLE_NAME</span></span><br />
<span data-ttu-id="9a409-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="9a409-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-405">21</span><span class="sxs-lookup"><span data-stu-id="9a409-405">21</span></span></p></td>
<td><p><span data-ttu-id="9a409-406">Возвращает переводы символов, определенные в каталоге, доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9a409-407">(НАБОР строк TRANSLATIONS)</span><span class="sxs-lookup"><span data-stu-id="9a409-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="9a409-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="9a409-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-412">39</span><span class="sxs-lookup"><span data-stu-id="9a409-412">39</span></span></p></td>
<td><p><span data-ttu-id="9a409-413">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="9a409-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-415">15 </span><span class="sxs-lookup"><span data-stu-id="9a409-415">15</span></span></p></td>
<td><p><span data-ttu-id="9a409-416">Возвращает привилегии ИСПОЛЬЗОВАНИЯ для объектов, определенных в каталоге, доступных или предоставленных определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="9a409-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="9a409-417">(USAGE_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="9a409-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="9a409-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="9a409-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="9a409-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="9a409-422">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="9a409-422">GRANTOR</span></span><br />
<span data-ttu-id="9a409-423">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="9a409-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-425">24</span><span class="sxs-lookup"><span data-stu-id="9a409-425">24</span></span></p></td>
<td><p><span data-ttu-id="9a409-426">Возвращает столбцы, от которых зависят просматриваемые таблицы, определенные в каталоге и принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="9a409-427">(VIEW_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="9a409-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="9a409-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-432">23</span><span class="sxs-lookup"><span data-stu-id="9a409-432">23</span></span></p></td>
<td><p><span data-ttu-id="9a409-433">Возвращает представления, определенные в каталоге, доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="9a409-434">(VIEWS Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="9a409-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="9a409-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="9a409-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="9a409-439">25</span><span class="sxs-lookup"><span data-stu-id="9a409-439">25</span></span></p></td>
<td><p><span data-ttu-id="9a409-440">Возвращает таблицы, в которых просматриваются таблицы, определенные в каталоге и принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="9a409-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="9a409-441">(VIEW_TABLE_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="9a409-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="9a409-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9a409-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="9a409-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9a409-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="9a409-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="9a409-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9a409-445">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9a409-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="9a409-446">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9a409-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a409-447">Константа</span><span class="sxs-lookup"><span data-stu-id="9a409-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a409-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="9a409-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="9a409-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="9a409-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="9a409-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="9a409-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="9a409-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="9a409-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="9a409-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="9a409-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="9a409-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="9a409-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="9a409-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="9a409-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="9a409-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="9a409-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="9a409-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="9a409-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="9a409-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="9a409-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="9a409-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="9a409-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="9a409-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="9a409-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a409-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="9a409-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9a409-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="9a409-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="9a409-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="9a409-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="9a409-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="9a409-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="9a409-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="9a409-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="9a409-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="9a409-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="9a409-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="9a409-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="9a409-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="9a409-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a409-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="9a409-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a409-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="9a409-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

