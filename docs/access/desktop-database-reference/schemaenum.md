---
title: SchemaEnum (Справочник по для настольных баз данных Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718828"
---
# <a name="schemaenum"></a><span data-ttu-id="5ed36-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="5ed36-102">SchemaEnum</span></span>

<span data-ttu-id="5ed36-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ed36-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ed36-104">Указывает тип схемы [OpenSchema](openschema-method-ado.md) метод извлекает **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5ed36-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ed36-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ed36-105">Remarks</span></span>

<span data-ttu-id="5ed36-106">Дополнительные сведения о функции и столбцов, возвращаемых для каждого константа ADO можно найти в разделах приложение Б *Справочнике программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="5ed36-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="5ed36-107">Имя каждого раздела отображается в скобки в разделе Описание в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5ed36-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="5ed36-108">Дополнительные сведения о функции и столбцов, возвращаемых для каждого ADO MD константу можно найти в разделах Глава 23 документации *OLE DB для OLAP* .</span><span class="sxs-lookup"><span data-stu-id="5ed36-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="5ed36-109">Имя каждого раздела приведены в скобках и помеченные звездочкой (\*) в столбце Описание в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5ed36-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="5ed36-110">Преобразования типов данных столбцов в документации по OLE DB для типов данных ADO с помощью ссылки на столбец описание раздела ADO [DataTypeEnum](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed36-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="5ed36-111">Например, тип данных OLE DB из **DBTYPE\_WSTR** соответствует типу данных ADO из **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="5ed36-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="5ed36-112">ADO создает аналогичную схемы результаты для константы, **adSchemaDBInfoKeywords** и **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="5ed36-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="5ed36-113">ADO создает **набор записей**, а затем заполняет каждой строки с помощью значения, возвращаемые методы **IDBInfo::GetKeywords** и **IDBInfo::GetLiteralInfo** соответственно.</span><span class="sxs-lookup"><span data-stu-id="5ed36-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="5ed36-114">Дополнительные сведения об этих методов можно найти в разделе IDBInfo *Справочник программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="5ed36-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="5ed36-115">Константа</span><span class="sxs-lookup"><span data-stu-id="5ed36-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="5ed36-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5ed36-116">Value</span></span></p></th>
<th><p><span data-ttu-id="5ed36-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5ed36-117">Description</span></span></p></th>
<th><p><span data-ttu-id="5ed36-118">Ограничение столбцов</span><span class="sxs-lookup"><span data-stu-id="5ed36-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-120">0</span><span class="sxs-lookup"><span data-stu-id="5ed36-120">0</span></span></p></td>
<td><p><span data-ttu-id="5ed36-121">Возвращает утверждения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="5ed36-122">(УТВЕРЖДЕНИЯ строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="5ed36-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-127">1</span><span class="sxs-lookup"><span data-stu-id="5ed36-127">1</span></span></p></td>
<td><p><span data-ttu-id="5ed36-128">Возвращает физические атрибуты, связанные с каталогами, доступными из СУБД.</span><span class="sxs-lookup"><span data-stu-id="5ed36-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="5ed36-129">(КАТАЛОГИ строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-132">2</span><span class="sxs-lookup"><span data-stu-id="5ed36-132">2</span></span></p></td>
<td><p><span data-ttu-id="5ed36-133">Возвращает наборы символов, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ed36-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="5ed36-134">(CHARACTER_SETS строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="5ed36-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-139">5</span><span class="sxs-lookup"><span data-stu-id="5ed36-139">5</span></span></p></td>
<td><p><span data-ttu-id="5ed36-140">Возвращает ограничения проверки, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="5ed36-141">(CHECK_CONSTRAINTS строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="5ed36-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-146">3</span><span class="sxs-lookup"><span data-stu-id="5ed36-146">3</span></span></p></td>
<td><p><span data-ttu-id="5ed36-147">Возвращает параметры сортировки символов, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ed36-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="5ed36-148">(Параметры СОРТИРОВКИ строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="5ed36-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-151">АРГУМЕНТ COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-153">13</span><span class="sxs-lookup"><span data-stu-id="5ed36-153">13</span></span></p></td>
<td><p><span data-ttu-id="5ed36-154">Возвращает привилегии для столбцов таблиц, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="5ed36-155">(COLUMN_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-158">TABLE_NAME</span></span><br />
<span data-ttu-id="5ed36-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="5ed36-160">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ed36-160">GRANTOR</span></span><br />
<span data-ttu-id="5ed36-161">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="5ed36-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-163">4</span><span class="sxs-lookup"><span data-stu-id="5ed36-163">4</span></span></p></td>
<td><p><span data-ttu-id="5ed36-164">Возвращает столбцы таблиц (включая представления) определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ed36-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="5ed36-165">(СТОЛБЦЫ строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-168">TABLE_NAME</span></span><br />
<span data-ttu-id="5ed36-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-171">11</span><span class="sxs-lookup"><span data-stu-id="5ed36-171">11</span></span></p></td>
<td><p><span data-ttu-id="5ed36-172">Возвращает столбцы, определенные в каталоге, зависящие от домена, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="5ed36-173">(COLUMN_DOMAIN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="5ed36-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-176">ИМЯ_ДОМЕНА</span><span class="sxs-lookup"><span data-stu-id="5ed36-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="5ed36-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-179">6</span><span class="sxs-lookup"><span data-stu-id="5ed36-179">6</span></span></p></td>
<td><p><span data-ttu-id="5ed36-180">Возвращает число столбцов, используемых ссылочные ограничения, ограничения уникальности, ограничения и утверждения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="5ed36-181">(CONSTRAINT_COLUMN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-184">TABLE_NAME</span></span><br />
<span data-ttu-id="5ed36-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-187">7</span><span class="sxs-lookup"><span data-stu-id="5ed36-187">7</span></span></p></td>
<td><p><span data-ttu-id="5ed36-188">Возвращает таблицы, используемые ссылочные ограничения, ограничения уникальности, ограничения и утверждения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="5ed36-189">(CONSTRAINT_TABLE_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-194">32</span><span class="sxs-lookup"><span data-stu-id="5ed36-194">32</span></span></p></td>
<td><p><span data-ttu-id="5ed36-195">Возвращает сведения о доступных кубов в схемы (или каталога, если поставщик не поддерживает схемы).</span><span class="sxs-lookup"><span data-stu-id="5ed36-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="5ed36-196">(КУБЫ строк \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="5ed36-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="5ed36-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-201">30</span><span class="sxs-lookup"><span data-stu-id="5ed36-201">30</span></span></p></td>
<td><p><span data-ttu-id="5ed36-202">Возвращает список ключевых слов, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ed36-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="5ed36-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-204">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="5ed36-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-206">31</span><span class="sxs-lookup"><span data-stu-id="5ed36-206">31</span></span></p></td>
<td><p><span data-ttu-id="5ed36-207">Возвращает список литералов от поставщика, используемых в текст команды.</span><span class="sxs-lookup"><span data-stu-id="5ed36-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="5ed36-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-209">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="5ed36-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-211">33</span><span class="sxs-lookup"><span data-stu-id="5ed36-211">33</span></span></p></td>
<td><p><span data-ttu-id="5ed36-212">Возвращает сведения о размеры данного куба.</span><span class="sxs-lookup"><span data-stu-id="5ed36-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="5ed36-213">Она содержится одна строка для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="5ed36-213">It has one row for each dimension.</span></span> <span data-ttu-id="5ed36-214">(РАЗМЕРЫ строк \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="5ed36-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="5ed36-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-217">CUBE_NAME</span></span><br />
<span data-ttu-id="5ed36-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="5ed36-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-221">27</span><span class="sxs-lookup"><span data-stu-id="5ed36-221">27</span></span></p></td>
<td><p><span data-ttu-id="5ed36-222">Возвращает столбцы внешнего ключа, определенные в каталоге данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ed36-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="5ed36-223">(FOREIGN_KEYS строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="5ed36-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-231">34</span><span class="sxs-lookup"><span data-stu-id="5ed36-231">34</span></span></p></td>
<td><p><span data-ttu-id="5ed36-232">Возвращает сведения о иерархий, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="5ed36-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="5ed36-233">(ИЕРАРХИИ строк \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="5ed36-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="5ed36-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-236">CUBE_NAME</span></span><br />
<span data-ttu-id="5ed36-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="5ed36-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-241">12</span><span class="sxs-lookup"><span data-stu-id="5ed36-241">12</span></span></p></td>
<td><p><span data-ttu-id="5ed36-242">Возвращает индексы, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="5ed36-243">(ИНДЕКСЫ строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-246">INDEX_NAME</span></span><br />
<span data-ttu-id="5ed36-247">ТИП</span><span class="sxs-lookup"><span data-stu-id="5ed36-247">TYPE</span></span><br />
<span data-ttu-id="5ed36-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-250">8</span><span class="sxs-lookup"><span data-stu-id="5ed36-250">8</span></span></p></td>
<td><p><span data-ttu-id="5ed36-251">Возвращает столбцы, определенные в каталоге, ограниченные как ключи данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ed36-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="5ed36-252">(Набор строк KEY_COLUMN_USAGE служит для указания)</span><span class="sxs-lookup"><span data-stu-id="5ed36-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="5ed36-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="5ed36-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-258">TABLE_NAME</span></span><br />
<span data-ttu-id="5ed36-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-261">35</span><span class="sxs-lookup"><span data-stu-id="5ed36-261">35</span></span></p></td>
<td><p><span data-ttu-id="5ed36-262">Возвращает сведения о доступных в измерении уровней.</span><span class="sxs-lookup"><span data-stu-id="5ed36-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="5ed36-263">(Уровни строк \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="5ed36-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="5ed36-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-266">CUBE_NAME</span></span><br />
<span data-ttu-id="5ed36-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="5ed36-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-272">36</span><span class="sxs-lookup"><span data-stu-id="5ed36-272">36</span></span></p></td>
<td><p><span data-ttu-id="5ed36-273">Возвращает сведения о доступных мер.</span><span class="sxs-lookup"><span data-stu-id="5ed36-273">Returns information about the available measures.</span></span> <span data-ttu-id="5ed36-274">(Набор строк меры \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="5ed36-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="5ed36-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-277">CUBE_NAME</span></span><br />
<span data-ttu-id="5ed36-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="5ed36-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-281">38</span><span class="sxs-lookup"><span data-stu-id="5ed36-281">38</span></span></p></td>
<td><p><span data-ttu-id="5ed36-282">Возвращает сведения о доступных членов.</span><span class="sxs-lookup"><span data-stu-id="5ed36-282">Returns information about the available members.</span></span> <span data-ttu-id="5ed36-283">(Строк MEMBERS \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="5ed36-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="5ed36-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-286">CUBE_NAME</span></span><br />
<span data-ttu-id="5ed36-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="5ed36-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="5ed36-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="5ed36-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="5ed36-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="5ed36-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ed36-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="5ed36-295">Оператор дерева (Дополнительные сведения см. в OLE DB для OLAP документации.)</span><span class="sxs-lookup"><span data-stu-id="5ed36-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-297">28</span><span class="sxs-lookup"><span data-stu-id="5ed36-297">28</span></span></p></td>
<td><p><span data-ttu-id="5ed36-298">Возвращает столбцы первичных ключей, определенные в каталоге данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ed36-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="5ed36-299">(PRIMARY_KEYS строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-304">29</span><span class="sxs-lookup"><span data-stu-id="5ed36-304">29</span></span></p></td>
<td><p><span data-ttu-id="5ed36-305">Возвращает сведения о столбцах наборы строк, возвращаемых процедурами.</span><span class="sxs-lookup"><span data-stu-id="5ed36-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="5ed36-306">(PROCEDURE_COLUMNS строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="5ed36-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-312">26</span><span class="sxs-lookup"><span data-stu-id="5ed36-312">26</span></span></p></td>
<td><p><span data-ttu-id="5ed36-313">Возвращает сведения о параметрах и кодах возврата процедур.</span><span class="sxs-lookup"><span data-stu-id="5ed36-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="5ed36-314">(PROCEDURE_PARAMETERS строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="5ed36-318">ИМЯ_ПАРАМЕТРА</span><span class="sxs-lookup"><span data-stu-id="5ed36-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-320">16</span><span class="sxs-lookup"><span data-stu-id="5ed36-320">16</span></span></p></td>
<td><p><span data-ttu-id="5ed36-321">Возвращает процедуры, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="5ed36-322">(ПРОЦЕДУРЫ строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="5ed36-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ed36-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-328">37</span><span class="sxs-lookup"><span data-stu-id="5ed36-328">37</span></span></p></td>
<td><p><span data-ttu-id="5ed36-329">Возвращает сведения о свойствах, доступных для каждого уровня измерения.</span><span class="sxs-lookup"><span data-stu-id="5ed36-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="5ed36-330">(Набор строк свойства \*)</span><span class="sxs-lookup"><span data-stu-id="5ed36-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="5ed36-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="5ed36-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-333">CUBE_NAME</span></span><br />
<span data-ttu-id="5ed36-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="5ed36-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ed36-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="5ed36-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-341">–1</span><span class="sxs-lookup"><span data-stu-id="5ed36-341">-1</span></span></p></td>
<td><p><span data-ttu-id="5ed36-342">Используется, если поставщик определяет нестандартного схемы запросов.</span><span class="sxs-lookup"><span data-stu-id="5ed36-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="5ed36-343">&lt;Поставщика&gt;</span><span class="sxs-lookup"><span data-stu-id="5ed36-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-345">22</span><span class="sxs-lookup"><span data-stu-id="5ed36-345">22</span></span></p></td>
<td><p><span data-ttu-id="5ed36-346">Возвращает типы данных (базовый), поддерживаемых поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="5ed36-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="5ed36-347">(Строк PROVIDER_TYPES)</span><span class="sxs-lookup"><span data-stu-id="5ed36-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ed36-348">DATA_TYPE</span></span><br />
<span data-ttu-id="5ed36-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="5ed36-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-351">9</span><span class="sxs-lookup"><span data-stu-id="5ed36-351">9</span></span></p></td>
<td><p><span data-ttu-id="5ed36-352">Возвращает ссылочные ограничения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="5ed36-353">(REFERENTIAL_CONSTRAINTS строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="5ed36-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-358">17</span><span class="sxs-lookup"><span data-stu-id="5ed36-358">17</span></span></p></td>
<td><p><span data-ttu-id="5ed36-359">Возвращает схемы (объекты базы данных), принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="5ed36-360">(СХЕМ строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="5ed36-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="5ed36-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="5ed36-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-365">18</span><span class="sxs-lookup"><span data-stu-id="5ed36-365">18</span></span></p></td>
<td><p><span data-ttu-id="5ed36-366">Возвращает уровни соответствия, параметры и языки меньшинств, поддерживаемые данными обработки реализации SQL, определенные в каталоге.</span><span class="sxs-lookup"><span data-stu-id="5ed36-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="5ed36-367">(SQL_LANGUAGES строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-368">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="5ed36-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-370">19</span><span class="sxs-lookup"><span data-stu-id="5ed36-370">19</span></span></p></td>
<td><p><span data-ttu-id="5ed36-371">Возвращает статистику, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="5ed36-372">(СТАТИСТИКА строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-377">10</span><span class="sxs-lookup"><span data-stu-id="5ed36-377">10</span></span></p></td>
<td><p><span data-ttu-id="5ed36-378">Возвращает табличные ограничения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="5ed36-379">(Набор строк TABLE_CONSTRAINTS служит для указания)</span><span class="sxs-lookup"><span data-stu-id="5ed36-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="5ed36-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="5ed36-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-385">TABLE_NAME</span></span><br />
<span data-ttu-id="5ed36-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ed36-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-388">14</span><span class="sxs-lookup"><span data-stu-id="5ed36-388">14</span></span></p></td>
<td><p><span data-ttu-id="5ed36-389">Возвращает привилегии для таблиц, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="5ed36-390">(TABLE_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-393">TABLE_NAME</span></span><br />
<span data-ttu-id="5ed36-394">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ed36-394">GRANTOR</span></span><br />
<span data-ttu-id="5ed36-395">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="5ed36-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-397">20</span><span class="sxs-lookup"><span data-stu-id="5ed36-397">20</span></span></p></td>
<td><p><span data-ttu-id="5ed36-398">Возвращает таблицы (включая представления) определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ed36-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="5ed36-399">(Набор строк таблицы)</span><span class="sxs-lookup"><span data-stu-id="5ed36-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-402">TABLE_NAME</span></span><br />
<span data-ttu-id="5ed36-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="5ed36-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-405">21</span><span class="sxs-lookup"><span data-stu-id="5ed36-405">21</span></span></p></td>
<td><p><span data-ttu-id="5ed36-406">Возвращает преобразования знаков, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ed36-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="5ed36-407">(Переводы строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="5ed36-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-412">39</span><span class="sxs-lookup"><span data-stu-id="5ed36-412">39</span></span></p></td>
<td><p><span data-ttu-id="5ed36-413">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="5ed36-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-415">15</span><span class="sxs-lookup"><span data-stu-id="5ed36-415">15</span></span></p></td>
<td><p><span data-ttu-id="5ed36-416">Возвращает привилегии USAGE для объектов, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ed36-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="5ed36-417">(USAGE_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="5ed36-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="5ed36-421">ТИП_ОБЪЕКТА</span><span class="sxs-lookup"><span data-stu-id="5ed36-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="5ed36-422">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ed36-422">GRANTOR</span></span><br />
<span data-ttu-id="5ed36-423">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="5ed36-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-425">24</span><span class="sxs-lookup"><span data-stu-id="5ed36-425">24</span></span></p></td>
<td><p><span data-ttu-id="5ed36-426">Возвращает столбцы, в которых просматриваемые таблицы, определенные в каталоге и принадлежащие указанному пользователю зависят.</span><span class="sxs-lookup"><span data-stu-id="5ed36-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="5ed36-427">(VIEW_COLUMN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="5ed36-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-432">23</span><span class="sxs-lookup"><span data-stu-id="5ed36-432">23</span></span></p></td>
<td><p><span data-ttu-id="5ed36-433">Возвращает представления, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ed36-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="5ed36-434">(Набор строк ПРЕДСТАВЛЕНИЯ)</span><span class="sxs-lookup"><span data-stu-id="5ed36-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="5ed36-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="5ed36-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed36-439">25</span><span class="sxs-lookup"><span data-stu-id="5ed36-439">25</span></span></p></td>
<td><p><span data-ttu-id="5ed36-440">Возвращает таблиц, в котором просматриваемые таблицы, определенные в каталоге и принадлежащие указанному пользователю зависят.</span><span class="sxs-lookup"><span data-stu-id="5ed36-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="5ed36-441">(VIEW_TABLE_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="5ed36-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="5ed36-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5ed36-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="5ed36-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="5ed36-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="5ed36-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="5ed36-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="5ed36-445">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="5ed36-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="5ed36-446">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="5ed36-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ed36-447">Константа</span><span class="sxs-lookup"><span data-stu-id="5ed36-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="5ed36-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="5ed36-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="5ed36-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="5ed36-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="5ed36-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="5ed36-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="5ed36-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="5ed36-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="5ed36-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="5ed36-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="5ed36-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="5ed36-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="5ed36-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="5ed36-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="5ed36-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="5ed36-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="5ed36-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="5ed36-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="5ed36-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="5ed36-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="5ed36-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="5ed36-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="5ed36-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ed36-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="5ed36-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5ed36-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="5ed36-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="5ed36-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="5ed36-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="5ed36-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="5ed36-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="5ed36-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="5ed36-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="5ed36-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="5ed36-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="5ed36-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="5ed36-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="5ed36-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="5ed36-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed36-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="5ed36-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ed36-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="5ed36-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

