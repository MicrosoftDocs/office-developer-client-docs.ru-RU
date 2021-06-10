---
title: SchemaEnum (Ссылка на настольные базы данных)
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
# <a name="schemaenum"></a><span data-ttu-id="26792-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="26792-102">SchemaEnum</span></span>

<span data-ttu-id="26792-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26792-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26792-104">Указывает тип схемы **Recordset,** который извлекает метод [OpenSchema.](openschema-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="26792-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="26792-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="26792-105">Remarks</span></span>

<span data-ttu-id="26792-106">Дополнительные сведения о функции и столбцах, возвращенных для каждой константы ADO, можно найти в статьях Приложения B справочника *программистов OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="26792-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="26792-107">Имя каждой темы перечислены в скобки в разделе Описание следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="26792-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="26792-108">Дополнительные сведения о функции и столбцах, возвращаемой для каждой константы ADO MD, можно найти в разделах главы 23 *OLE DB* для документации OLAP.</span><span class="sxs-lookup"><span data-stu-id="26792-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="26792-109">Имя каждой темы перечислены в скобки и отмечены звездочкой () в столбце \* Описание следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="26792-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="26792-110">Перевод типов столбцов данных в документации OLE DB на типы данных ADO, ссылаясь на столбец Описание темы ADO [DataTypeEnum.](datatypeenum.md)</span><span class="sxs-lookup"><span data-stu-id="26792-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="26792-111">Например, тип данных OLE DB **\_ WSTR** эквивалентен типу данных **ADO adWChar.**</span><span class="sxs-lookup"><span data-stu-id="26792-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="26792-112">ADO создает схемы, как результаты для констант, **adSchemaDBInfoKeywords** и **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="26792-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="26792-113">ADO создает набор записей, а затем заполняет каждую строку значениями, возвращенными соответственно методами **IDBInfo::GetKeywords** и **IDBInfo::GetLiteralInfo.**</span><span class="sxs-lookup"><span data-stu-id="26792-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="26792-114">Дополнительные сведения об этих методах можно найти в разделе IDBInfo справочника *программиста OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="26792-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="26792-115">Константа</span><span class="sxs-lookup"><span data-stu-id="26792-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="26792-116">Значение</span><span class="sxs-lookup"><span data-stu-id="26792-116">Value</span></span></p></th>
<th><p><span data-ttu-id="26792-117">Описание</span><span class="sxs-lookup"><span data-stu-id="26792-117">Description</span></span></p></th>
<th><p><span data-ttu-id="26792-118">Столбцы ограничения</span><span class="sxs-lookup"><span data-stu-id="26792-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26792-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="26792-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-120">0</span><span class="sxs-lookup"><span data-stu-id="26792-120">0</span></span></p></td>
<td><p><span data-ttu-id="26792-121">Возвращает утверждения, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="26792-122">(ASSERTIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="26792-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="26792-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="26792-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-127">1</span><span class="sxs-lookup"><span data-stu-id="26792-127">1</span></span></p></td>
<td><p><span data-ttu-id="26792-128">Возвращает физические атрибуты, связанные с каталогами, доступными из DBMS.</span><span class="sxs-lookup"><span data-stu-id="26792-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="26792-129">(КАТАЛОГИ Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="26792-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-132">2</span><span class="sxs-lookup"><span data-stu-id="26792-132">2</span></span></p></td>
<td><p><span data-ttu-id="26792-133">Возвращает наборы символов, определенные в каталоге, доступные для данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="26792-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="26792-134">(CHARACTER_SETS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="26792-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="26792-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="26792-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-139">5 </span><span class="sxs-lookup"><span data-stu-id="26792-139">5</span></span></p></td>
<td><p><span data-ttu-id="26792-140">Возвращает ограничения проверки, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="26792-141">(CHECK_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="26792-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="26792-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="26792-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-146">3</span><span class="sxs-lookup"><span data-stu-id="26792-146">3</span></span></p></td>
<td><p><span data-ttu-id="26792-147">Возвращается коллаций символов, определенных в каталоге, доступных для данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="26792-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="26792-148">(COLLATIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="26792-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="26792-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="26792-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-153">13</span><span class="sxs-lookup"><span data-stu-id="26792-153">13</span></span></p></td>
<td><p><span data-ttu-id="26792-154">Возвращает привилегии для столбцов таблиц, определенных в каталоге, доступных или предоставленных определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="26792-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="26792-155">(COLUMN_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-158">TABLE_NAME</span></span><br />
<span data-ttu-id="26792-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="26792-160">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="26792-160">GRANTOR</span></span><br />
<span data-ttu-id="26792-161">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="26792-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="26792-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-163">4 </span><span class="sxs-lookup"><span data-stu-id="26792-163">4</span></span></p></td>
<td><p><span data-ttu-id="26792-164">Возвращает столбцы таблиц (включая представления), определенные в каталоге, доступные для данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="26792-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="26792-165">(СТОЛБЦЫ Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-168">TABLE_NAME</span></span><br />
<span data-ttu-id="26792-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="26792-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-171">11</span><span class="sxs-lookup"><span data-stu-id="26792-171">11</span></span></p></td>
<td><p><span data-ttu-id="26792-172">Возвращает столбцы, определенные в каталоге, которые зависят от домена, определенного в каталоге и владеющих определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="26792-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="26792-173">(COLUMN_DOMAIN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="26792-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="26792-176">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="26792-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="26792-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-179">6 </span><span class="sxs-lookup"><span data-stu-id="26792-179">6</span></span></p></td>
<td><p><span data-ttu-id="26792-180">Возвращает столбцы, используемые ссылками, уникальными ограничениями, ограничениями проверки и утверждениями, определенными в каталоге и принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="26792-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-184">TABLE_NAME</span></span><br />
<span data-ttu-id="26792-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="26792-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-187">7 </span><span class="sxs-lookup"><span data-stu-id="26792-187">7</span></span></p></td>
<td><p><span data-ttu-id="26792-188">Возвращает таблицы, используемые ссылками, уникальными ограничениями, ограничениями проверки и утверждениями, определенными в каталоге и принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="26792-189">(CONSTRAINT_TABLE_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="26792-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-194">32</span><span class="sxs-lookup"><span data-stu-id="26792-194">32</span></span></p></td>
<td><p><span data-ttu-id="26792-195">Возвращает сведения о доступных кубах в схеме (или каталоге, если поставщик не поддерживает схемы).</span><span class="sxs-lookup"><span data-stu-id="26792-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="26792-196">(CUBES Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="26792-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="26792-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="26792-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="26792-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="26792-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-201">30</span><span class="sxs-lookup"><span data-stu-id="26792-201">30</span></span></p></td>
<td><p><span data-ttu-id="26792-202">Возвращает список ключевых слов, определенных для поставщика.</span><span class="sxs-lookup"><span data-stu-id="26792-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="26792-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="26792-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="26792-204">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="26792-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="26792-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-206">31</span><span class="sxs-lookup"><span data-stu-id="26792-206">31</span></span></p></td>
<td><p><span data-ttu-id="26792-207">Возвращает список литералов, определенных для поставщика, используемых в текстовых командах.</span><span class="sxs-lookup"><span data-stu-id="26792-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="26792-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="26792-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="26792-209">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="26792-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="26792-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-211">33</span><span class="sxs-lookup"><span data-stu-id="26792-211">33</span></span></p></td>
<td><p><span data-ttu-id="26792-212">Возвращает сведения о измерениях в заданном кубе.</span><span class="sxs-lookup"><span data-stu-id="26792-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="26792-213">Она имеет одну строку для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="26792-213">It has one row for each dimension.</span></span> <span data-ttu-id="26792-214">(DIMENSIONS Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="26792-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="26792-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="26792-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="26792-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-217">CUBE_NAME</span></span><br />
<span data-ttu-id="26792-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="26792-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="26792-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-221">27</span><span class="sxs-lookup"><span data-stu-id="26792-221">27</span></span></p></td>
<td><p><span data-ttu-id="26792-222">Возвращает внешние столбцы ключей, определенные в каталоге определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="26792-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="26792-223">(FOREIGN_KEYS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="26792-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="26792-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-231">34</span><span class="sxs-lookup"><span data-stu-id="26792-231">34</span></span></p></td>
<td><p><span data-ttu-id="26792-232">Возвращает сведения об иерархиях, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="26792-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="26792-233">(ИЕРАРХИИ Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="26792-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="26792-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="26792-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="26792-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-236">CUBE_NAME</span></span><br />
<span data-ttu-id="26792-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="26792-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="26792-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-241">12 </span><span class="sxs-lookup"><span data-stu-id="26792-241">12</span></span></p></td>
<td><p><span data-ttu-id="26792-242">Возвращает индексы, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="26792-243">(INDEXES Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-246">INDEX_NAME</span></span><br />
<span data-ttu-id="26792-247">TYPE</span><span class="sxs-lookup"><span data-stu-id="26792-247">TYPE</span></span><br />
<span data-ttu-id="26792-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="26792-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-250">8 </span><span class="sxs-lookup"><span data-stu-id="26792-250">8</span></span></p></td>
<td><p><span data-ttu-id="26792-251">Возвращает столбцы, определенные в каталоге, которые ограничены в качестве ключей определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="26792-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="26792-252">(KEY_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="26792-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="26792-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="26792-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-258">TABLE_NAME</span></span><br />
<span data-ttu-id="26792-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="26792-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-261">35</span><span class="sxs-lookup"><span data-stu-id="26792-261">35</span></span></p></td>
<td><p><span data-ttu-id="26792-262">Возвращает сведения об уровнях, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="26792-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="26792-263">(LEVELS Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="26792-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="26792-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="26792-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="26792-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-266">CUBE_NAME</span></span><br />
<span data-ttu-id="26792-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="26792-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="26792-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-272">36</span><span class="sxs-lookup"><span data-stu-id="26792-272">36</span></span></p></td>
<td><p><span data-ttu-id="26792-273">Возвращает сведения о доступных мерах.</span><span class="sxs-lookup"><span data-stu-id="26792-273">Returns information about the available measures.</span></span> <span data-ttu-id="26792-274">(MEASURES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="26792-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="26792-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="26792-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="26792-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-277">CUBE_NAME</span></span><br />
<span data-ttu-id="26792-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="26792-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="26792-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-281">38</span><span class="sxs-lookup"><span data-stu-id="26792-281">38</span></span></p></td>
<td><p><span data-ttu-id="26792-282">Возвращает сведения о доступных членах.</span><span class="sxs-lookup"><span data-stu-id="26792-282">Returns information about the available members.</span></span> <span data-ttu-id="26792-283">(НАБОР УЧАСТНИКОВ \*)</span><span class="sxs-lookup"><span data-stu-id="26792-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="26792-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="26792-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="26792-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-286">CUBE_NAME</span></span><br />
<span data-ttu-id="26792-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="26792-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="26792-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="26792-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="26792-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="26792-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="26792-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="26792-295">Оператор дерева (Дополнительные сведения см. в документации OLE DB для OLAP.)</span><span class="sxs-lookup"><span data-stu-id="26792-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="26792-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-297">28</span><span class="sxs-lookup"><span data-stu-id="26792-297">28</span></span></p></td>
<td><p><span data-ttu-id="26792-298">Возвращает основные столбцы ключей, определенные в каталоге определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="26792-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="26792-299">(PRIMARY_KEYS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="26792-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-304">29</span><span class="sxs-lookup"><span data-stu-id="26792-304">29</span></span></p></td>
<td><p><span data-ttu-id="26792-305">Возвращает сведения о столбцах строк, возвращаемой процедурами.</span><span class="sxs-lookup"><span data-stu-id="26792-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="26792-306">(PROCEDURE_COLUMNS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="26792-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="26792-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="26792-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="26792-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-312">26</span><span class="sxs-lookup"><span data-stu-id="26792-312">26</span></span></p></td>
<td><p><span data-ttu-id="26792-313">Возвращает сведения о параметрах и кодах процедур.</span><span class="sxs-lookup"><span data-stu-id="26792-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="26792-314">(PROCEDURE_PARAMETERS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="26792-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="26792-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="26792-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="26792-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-320">16 </span><span class="sxs-lookup"><span data-stu-id="26792-320">16</span></span></p></td>
<td><p><span data-ttu-id="26792-321">Возвращает процедуры, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="26792-322">(PROCEDURES Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="26792-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="26792-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="26792-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="26792-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="26792-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-328">37</span><span class="sxs-lookup"><span data-stu-id="26792-328">37</span></span></p></td>
<td><p><span data-ttu-id="26792-329">Возвращает сведения о доступных свойствах для каждого уровня измерения.</span><span class="sxs-lookup"><span data-stu-id="26792-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="26792-330">(PROPERTIES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="26792-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="26792-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="26792-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="26792-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-333">CUBE_NAME</span></span><br />
<span data-ttu-id="26792-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="26792-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="26792-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="26792-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="26792-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-341">–1</span><span class="sxs-lookup"><span data-stu-id="26792-341">-1</span></span></p></td>
<td><p><span data-ttu-id="26792-342">Используется, если поставщик определяет собственные нестандартные запросы схемы.</span><span class="sxs-lookup"><span data-stu-id="26792-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="26792-343">&lt;Конкретный поставщик&gt;</span><span class="sxs-lookup"><span data-stu-id="26792-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="26792-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-345">22</span><span class="sxs-lookup"><span data-stu-id="26792-345">22</span></span></p></td>
<td><p><span data-ttu-id="26792-346">Возвращает типы (базовые) данные, поддерживаемые поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="26792-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="26792-347">(PROVIDER_TYPES Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="26792-348">DATA_TYPE</span></span><br />
<span data-ttu-id="26792-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="26792-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="26792-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-351">9 </span><span class="sxs-lookup"><span data-stu-id="26792-351">9</span></span></p></td>
<td><p><span data-ttu-id="26792-352">Возвращает ссылки, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="26792-353">(REFERENTIAL_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="26792-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="26792-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="26792-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-358">17 </span><span class="sxs-lookup"><span data-stu-id="26792-358">17</span></span></p></td>
<td><p><span data-ttu-id="26792-359">Возвращает схемы (объекты базы данных), которые принадлежат этому пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="26792-360">(SCHEMATA Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="26792-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="26792-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="26792-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="26792-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-365">18 </span><span class="sxs-lookup"><span data-stu-id="26792-365">18</span></span></p></td>
<td><p><span data-ttu-id="26792-366">Возвращает уровни соответствия, параметры и диалекты, поддерживаемые данными SQL-реализации, определенными в каталоге.</span><span class="sxs-lookup"><span data-stu-id="26792-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="26792-367">(SQL_LANGUAGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-368">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="26792-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="26792-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-370">19</span><span class="sxs-lookup"><span data-stu-id="26792-370">19</span></span></p></td>
<td><p><span data-ttu-id="26792-371">Возвращает статистические данные, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="26792-372">(STATISTICS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="26792-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-377">10 </span><span class="sxs-lookup"><span data-stu-id="26792-377">10</span></span></p></td>
<td><p><span data-ttu-id="26792-378">Возвращает ограничения таблицы, определенные в каталоге, которые принадлежат определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="26792-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="26792-379">(TABLE_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="26792-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="26792-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="26792-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-385">TABLE_NAME</span></span><br />
<span data-ttu-id="26792-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="26792-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="26792-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-388">14 </span><span class="sxs-lookup"><span data-stu-id="26792-388">14</span></span></p></td>
<td><p><span data-ttu-id="26792-389">Возвращает привилегии в таблицах, определенных в каталоге, доступных или предоставленных определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="26792-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="26792-390">(TABLE_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-393">TABLE_NAME</span></span><br />
<span data-ttu-id="26792-394">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="26792-394">GRANTOR</span></span><br />
<span data-ttu-id="26792-395">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="26792-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="26792-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-397">20</span><span class="sxs-lookup"><span data-stu-id="26792-397">20</span></span></p></td>
<td><p><span data-ttu-id="26792-398">Возвращает таблицы (включая представления), определенные в каталоге, доступные для данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="26792-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="26792-399">(TABLES Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-402">TABLE_NAME</span></span><br />
<span data-ttu-id="26792-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="26792-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="26792-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-405">21</span><span class="sxs-lookup"><span data-stu-id="26792-405">21</span></span></p></td>
<td><p><span data-ttu-id="26792-406">Возвращает переводы символов, определенные в каталоге, доступные для данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="26792-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="26792-407">(TRANSLATIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="26792-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="26792-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="26792-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-412">39</span><span class="sxs-lookup"><span data-stu-id="26792-412">39</span></span></p></td>
<td><p><span data-ttu-id="26792-413">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="26792-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="26792-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-415">15</span><span class="sxs-lookup"><span data-stu-id="26792-415">15</span></span></p></td>
<td><p><span data-ttu-id="26792-416">Возвращает привилегии USE для объектов, определенных в каталоге, доступных или предоставленных определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="26792-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="26792-417">(USAGE_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="26792-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="26792-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="26792-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="26792-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="26792-422">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="26792-422">GRANTOR</span></span><br />
<span data-ttu-id="26792-423">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="26792-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="26792-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-425">24</span><span class="sxs-lookup"><span data-stu-id="26792-425">24</span></span></p></td>
<td><p><span data-ttu-id="26792-426">Возвращает столбцы, на которых просматриваются таблицы, определенные в каталоге и принадлежат определенному пользователю, зависят.</span><span class="sxs-lookup"><span data-stu-id="26792-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="26792-427">(VIEW_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="26792-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="26792-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="26792-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-432">23</span><span class="sxs-lookup"><span data-stu-id="26792-432">23</span></span></p></td>
<td><p><span data-ttu-id="26792-433">Возвращает представления, определенные в каталоге, доступные для данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="26792-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="26792-434">(VIEWS Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="26792-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="26792-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="26792-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="26792-439">25</span><span class="sxs-lookup"><span data-stu-id="26792-439">25</span></span></p></td>
<td><p><span data-ttu-id="26792-440">Возвращает таблицы, на которых просматриваются таблицы, определенные в каталоге и принадлежат определенному пользователю, зависят.</span><span class="sxs-lookup"><span data-stu-id="26792-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="26792-441">(VIEW_TABLE_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="26792-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="26792-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="26792-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="26792-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="26792-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="26792-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="26792-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="26792-445">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="26792-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="26792-446">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="26792-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26792-447">Константа</span><span class="sxs-lookup"><span data-stu-id="26792-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26792-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="26792-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="26792-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="26792-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="26792-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="26792-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="26792-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="26792-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="26792-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="26792-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="26792-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="26792-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="26792-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="26792-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="26792-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="26792-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="26792-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="26792-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="26792-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="26792-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="26792-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="26792-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="26792-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="26792-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26792-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="26792-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="26792-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="26792-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="26792-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="26792-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="26792-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="26792-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="26792-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="26792-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="26792-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="26792-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="26792-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="26792-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-485">AdoEnums.Schema.USEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="26792-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="26792-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26792-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="26792-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26792-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="26792-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

