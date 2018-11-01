---
title: SchemaEnum (Справочник по для настольных баз данных Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c7f9f9e52f2220a384ba73a64d96dd93fec2cd91
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871285"
---
# <a name="schemaenum"></a><span data-ttu-id="f5104-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="f5104-102">SchemaEnum</span></span>

<span data-ttu-id="f5104-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5104-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5104-104">Указывает тип схемы [OpenSchema](openschema-method-ado.md) метод извлекает **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f5104-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5104-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="f5104-105">Remarks</span></span>

<span data-ttu-id="f5104-106">Дополнительные сведения о функции и столбцов, возвращаемых для каждого константа ADO можно найти в разделах приложение Б *Справочнике программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="f5104-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="f5104-107">Имя каждого раздела отображается в скобки в разделе Описание в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f5104-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="f5104-108">Дополнительные сведения о функции и столбцов, возвращаемых для каждого ADO MD константу можно найти в разделах Глава 23 документации *OLE DB для OLAP* .</span><span class="sxs-lookup"><span data-stu-id="f5104-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="f5104-109">Имя каждого раздела приведены в скобках и помеченные звездочкой (\*) в столбце Описание в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f5104-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="f5104-110">Преобразования типов данных столбцов в документации по OLE DB для типов данных ADO с помощью ссылки на столбец описание раздела ADO [DataTypeEnum](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="f5104-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="f5104-111">Например, тип данных OLE DB из **DBTYPE\_WSTR** соответствует типу данных ADO из **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="f5104-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="f5104-112">ADO создает аналогичную схемы результаты для константы, **adSchemaDBInfoKeywords** и **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="f5104-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="f5104-113">ADO создает **набор записей**, а затем заполняет каждой строки с помощью значения, возвращаемые методы **IDBInfo::GetKeywords** и **IDBInfo::GetLiteralInfo** соответственно.</span><span class="sxs-lookup"><span data-stu-id="f5104-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="f5104-114">Дополнительные сведения об этих методов можно найти в разделе IDBInfo *Справочник программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="f5104-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="f5104-115">Константа</span><span class="sxs-lookup"><span data-stu-id="f5104-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="f5104-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f5104-116">Value</span></span></p></th>
<th><p><span data-ttu-id="f5104-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f5104-117">Description</span></span></p></th>
<th><p><span data-ttu-id="f5104-118">Ограничение столбцов</span><span class="sxs-lookup"><span data-stu-id="f5104-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5104-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-120">0</span><span class="sxs-lookup"><span data-stu-id="f5104-120">0</span></span></p></td>
<td><p><span data-ttu-id="f5104-121">Возвращает утверждения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f5104-122">(УТВЕРЖДЕНИЯ строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f5104-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f5104-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-127">1</span><span class="sxs-lookup"><span data-stu-id="f5104-127">1</span></span></p></td>
<td><p><span data-ttu-id="f5104-128">Возвращает физические атрибуты, связанные с каталогами, доступными из СУБД.</span><span class="sxs-lookup"><span data-stu-id="f5104-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="f5104-129">(КАТАЛОГИ строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-132">2</span><span class="sxs-lookup"><span data-stu-id="f5104-132">2</span></span></p></td>
<td><p><span data-ttu-id="f5104-133">Возвращает наборы символов, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5104-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f5104-134">(CHARACTER_SETS строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="f5104-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="f5104-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-139">5</span><span class="sxs-lookup"><span data-stu-id="f5104-139">5</span></span></p></td>
<td><p><span data-ttu-id="f5104-140">Возвращает ограничения проверки, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f5104-141">(CHECK_CONSTRAINTS строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f5104-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f5104-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-146">3</span><span class="sxs-lookup"><span data-stu-id="f5104-146">3</span></span></p></td>
<td><p><span data-ttu-id="f5104-147">Возвращает параметры сортировки символов, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5104-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f5104-148">(Параметры СОРТИРОВКИ строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="f5104-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="f5104-151">АРГУМЕНТ COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-153">13</span><span class="sxs-lookup"><span data-stu-id="f5104-153">13</span></span></p></td>
<td><p><span data-ttu-id="f5104-154">Возвращает привилегии для столбцов таблиц, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="f5104-155">(COLUMN_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-158">TABLE_NAME</span></span><br />
<span data-ttu-id="f5104-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="f5104-160">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="f5104-160">GRANTOR</span></span><br />
<span data-ttu-id="f5104-161">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="f5104-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-163">4</span><span class="sxs-lookup"><span data-stu-id="f5104-163">4</span></span></p></td>
<td><p><span data-ttu-id="f5104-164">Возвращает столбцы таблиц (включая представления) определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5104-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f5104-165">(СТОЛБЦЫ строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-168">TABLE_NAME</span></span><br />
<span data-ttu-id="f5104-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-171">11</span><span class="sxs-lookup"><span data-stu-id="f5104-171">11</span></span></p></td>
<td><p><span data-ttu-id="f5104-172">Возвращает столбцы, определенные в каталоге, зависящие от домена, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="f5104-173">(COLUMN_DOMAIN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="f5104-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="f5104-176">ИМЯ_ДОМЕНА</span><span class="sxs-lookup"><span data-stu-id="f5104-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="f5104-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-179">6</span><span class="sxs-lookup"><span data-stu-id="f5104-179">6</span></span></p></td>
<td><p><span data-ttu-id="f5104-180">Возвращает число столбцов, используемых ссылочные ограничения, ограничения уникальности, ограничения и утверждения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="f5104-181">(CONSTRAINT_COLUMN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-184">TABLE_NAME</span></span><br />
<span data-ttu-id="f5104-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-187">7</span><span class="sxs-lookup"><span data-stu-id="f5104-187">7</span></span></p></td>
<td><p><span data-ttu-id="f5104-188">Возвращает таблицы, используемые ссылочные ограничения, ограничения уникальности, ограничения и утверждения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="f5104-189">(CONSTRAINT_TABLE_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-194">32</span><span class="sxs-lookup"><span data-stu-id="f5104-194">32</span></span></p></td>
<td><p><span data-ttu-id="f5104-195">Возвращает сведения о доступных кубов в схемы (или каталога, если поставщик не поддерживает схемы).</span><span class="sxs-lookup"><span data-stu-id="f5104-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="f5104-196">(КУБЫ строк \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="f5104-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f5104-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-201">30</span><span class="sxs-lookup"><span data-stu-id="f5104-201">30</span></span></p></td>
<td><p><span data-ttu-id="f5104-202">Возвращает список ключевых слов, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="f5104-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="f5104-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-204">&lt;Отсутствует&gt;</span><span class="sxs-lookup"><span data-stu-id="f5104-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-206">31</span><span class="sxs-lookup"><span data-stu-id="f5104-206">31</span></span></p></td>
<td><p><span data-ttu-id="f5104-207">Возвращает список литералов от поставщика, используемых в текст команды.</span><span class="sxs-lookup"><span data-stu-id="f5104-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="f5104-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-209">&lt;Отсутствует&gt;</span><span class="sxs-lookup"><span data-stu-id="f5104-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-211">33</span><span class="sxs-lookup"><span data-stu-id="f5104-211">33</span></span></p></td>
<td><p><span data-ttu-id="f5104-212">Возвращает сведения о размеры данного куба.</span><span class="sxs-lookup"><span data-stu-id="f5104-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="f5104-213">Она содержится одна строка для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="f5104-213">It has one row for each dimension.</span></span> <span data-ttu-id="f5104-214">(РАЗМЕРЫ строк \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="f5104-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f5104-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-217">CUBE_NAME</span></span><br />
<span data-ttu-id="f5104-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="f5104-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-221">27</span><span class="sxs-lookup"><span data-stu-id="f5104-221">27</span></span></p></td>
<td><p><span data-ttu-id="f5104-222">Возвращает столбцы внешнего ключа, определенные в каталоге данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="f5104-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="f5104-223">(FOREIGN_KEYS строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="f5104-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-231">34</span><span class="sxs-lookup"><span data-stu-id="f5104-231">34</span></span></p></td>
<td><p><span data-ttu-id="f5104-232">Возвращает сведения о иерархий, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="f5104-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="f5104-233">(ИЕРАРХИИ строк \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="f5104-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f5104-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-236">CUBE_NAME</span></span><br />
<span data-ttu-id="f5104-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="f5104-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-241">12</span><span class="sxs-lookup"><span data-stu-id="f5104-241">12</span></span></p></td>
<td><p><span data-ttu-id="f5104-242">Возвращает индексы, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f5104-243">(ИНДЕКСЫ строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-246">INDEX_NAME</span></span><br />
<span data-ttu-id="f5104-247">ТИП</span><span class="sxs-lookup"><span data-stu-id="f5104-247">TYPE</span></span><br />
<span data-ttu-id="f5104-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-250">8</span><span class="sxs-lookup"><span data-stu-id="f5104-250">8</span></span></p></td>
<td><p><span data-ttu-id="f5104-251">Возвращает столбцы, определенные в каталоге, ограниченные как ключи данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="f5104-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="f5104-252">(Набор строк KEY_COLUMN_USAGE служит для указания)</span><span class="sxs-lookup"><span data-stu-id="f5104-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f5104-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f5104-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="f5104-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-258">TABLE_NAME</span></span><br />
<span data-ttu-id="f5104-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-261">35</span><span class="sxs-lookup"><span data-stu-id="f5104-261">35</span></span></p></td>
<td><p><span data-ttu-id="f5104-262">Возвращает сведения о доступных в измерении уровней.</span><span class="sxs-lookup"><span data-stu-id="f5104-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="f5104-263">(Уровни строк \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="f5104-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f5104-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-266">CUBE_NAME</span></span><br />
<span data-ttu-id="f5104-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="f5104-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-272">36</span><span class="sxs-lookup"><span data-stu-id="f5104-272">36</span></span></p></td>
<td><p><span data-ttu-id="f5104-273">Возвращает сведения о доступных мер.</span><span class="sxs-lookup"><span data-stu-id="f5104-273">Returns information about the available measures.</span></span> <span data-ttu-id="f5104-274">(Набор строк меры \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="f5104-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f5104-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-277">CUBE_NAME</span></span><br />
<span data-ttu-id="f5104-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="f5104-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-281">38</span><span class="sxs-lookup"><span data-stu-id="f5104-281">38</span></span></p></td>
<td><p><span data-ttu-id="f5104-282">Возвращает сведения о доступных членов.</span><span class="sxs-lookup"><span data-stu-id="f5104-282">Returns information about the available members.</span></span> <span data-ttu-id="f5104-283">(Строк MEMBERS \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="f5104-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f5104-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-286">CUBE_NAME</span></span><br />
<span data-ttu-id="f5104-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="f5104-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="f5104-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="f5104-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="f5104-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="f5104-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5104-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="f5104-295">Оператор дерева (Дополнительные сведения см. в OLE DB для OLAP документации.)</span><span class="sxs-lookup"><span data-stu-id="f5104-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-297">28</span><span class="sxs-lookup"><span data-stu-id="f5104-297">28</span></span></p></td>
<td><p><span data-ttu-id="f5104-298">Возвращает столбцы первичных ключей, определенные в каталоге данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="f5104-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="f5104-299">(PRIMARY_KEYS строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-304">29</span><span class="sxs-lookup"><span data-stu-id="f5104-304">29</span></span></p></td>
<td><p><span data-ttu-id="f5104-305">Возвращает сведения о столбцах наборы строк, возвращаемых процедурами.</span><span class="sxs-lookup"><span data-stu-id="f5104-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="f5104-306">(PROCEDURE_COLUMNS строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="f5104-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="f5104-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-312">26</span><span class="sxs-lookup"><span data-stu-id="f5104-312">26</span></span></p></td>
<td><p><span data-ttu-id="f5104-313">Возвращает сведения о параметрах и кодах возврата процедур.</span><span class="sxs-lookup"><span data-stu-id="f5104-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="f5104-314">(PROCEDURE_PARAMETERS строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="f5104-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="f5104-318">ИМЯ_ПАРАМЕТРА</span><span class="sxs-lookup"><span data-stu-id="f5104-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-320">16</span><span class="sxs-lookup"><span data-stu-id="f5104-320">16</span></span></p></td>
<td><p><span data-ttu-id="f5104-321">Возвращает процедуры, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f5104-322">(ПРОЦЕДУРЫ строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="f5104-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="f5104-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5104-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-328">37</span><span class="sxs-lookup"><span data-stu-id="f5104-328">37</span></span></p></td>
<td><p><span data-ttu-id="f5104-329">Возвращает сведения о свойствах, доступных для каждого уровня измерения.</span><span class="sxs-lookup"><span data-stu-id="f5104-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="f5104-330">(Набор строк свойства \*)</span><span class="sxs-lookup"><span data-stu-id="f5104-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f5104-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="f5104-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f5104-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-333">CUBE_NAME</span></span><br />
<span data-ttu-id="f5104-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f5104-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5104-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="f5104-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-341">-1</span><span class="sxs-lookup"><span data-stu-id="f5104-341">-1</span></span></p></td>
<td><p><span data-ttu-id="f5104-342">Используется, если поставщик определяет нестандартного схемы запросов.</span><span class="sxs-lookup"><span data-stu-id="f5104-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="f5104-343">&lt;Поставщика&gt;</span><span class="sxs-lookup"><span data-stu-id="f5104-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-345">22</span><span class="sxs-lookup"><span data-stu-id="f5104-345">22</span></span></p></td>
<td><p><span data-ttu-id="f5104-346">Возвращает типы данных (базовый), поддерживаемых поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="f5104-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="f5104-347">(Строк PROVIDER_TYPES)</span><span class="sxs-lookup"><span data-stu-id="f5104-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5104-348">DATA_TYPE</span></span><br />
<span data-ttu-id="f5104-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="f5104-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-351">9</span><span class="sxs-lookup"><span data-stu-id="f5104-351">9</span></span></p></td>
<td><p><span data-ttu-id="f5104-352">Возвращает ссылочные ограничения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f5104-353">(REFERENTIAL_CONSTRAINTS строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f5104-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f5104-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-358">17</span><span class="sxs-lookup"><span data-stu-id="f5104-358">17</span></span></p></td>
<td><p><span data-ttu-id="f5104-359">Возвращает схемы (объекты базы данных), принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="f5104-360">(СХЕМ строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="f5104-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f5104-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="f5104-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-365">18</span><span class="sxs-lookup"><span data-stu-id="f5104-365">18</span></span></p></td>
<td><p><span data-ttu-id="f5104-366">Возвращает уровни соответствия, параметры и языки меньшинств, поддерживаемые данными обработки реализации SQL, определенные в каталоге.</span><span class="sxs-lookup"><span data-stu-id="f5104-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="f5104-367">(SQL_LANGUAGES строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-368">&lt;Отсутствует&gt;</span><span class="sxs-lookup"><span data-stu-id="f5104-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-370">19</span><span class="sxs-lookup"><span data-stu-id="f5104-370">19</span></span></p></td>
<td><p><span data-ttu-id="f5104-371">Возвращает статистику, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f5104-372">(СТАТИСТИКА строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-377">10</span><span class="sxs-lookup"><span data-stu-id="f5104-377">10</span></span></p></td>
<td><p><span data-ttu-id="f5104-378">Возвращает табличные ограничения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f5104-379">(Набор строк TABLE_CONSTRAINTS служит для указания)</span><span class="sxs-lookup"><span data-stu-id="f5104-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f5104-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f5104-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="f5104-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-385">TABLE_NAME</span></span><br />
<span data-ttu-id="f5104-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5104-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-388">14</span><span class="sxs-lookup"><span data-stu-id="f5104-388">14</span></span></p></td>
<td><p><span data-ttu-id="f5104-389">Возвращает привилегии для таблиц, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="f5104-390">(TABLE_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-393">TABLE_NAME</span></span><br />
<span data-ttu-id="f5104-394">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="f5104-394">GRANTOR</span></span><br />
<span data-ttu-id="f5104-395">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="f5104-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-397">20</span><span class="sxs-lookup"><span data-stu-id="f5104-397">20</span></span></p></td>
<td><p><span data-ttu-id="f5104-398">Возвращает таблицы (включая представления) определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5104-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f5104-399">(Набор строк таблицы)</span><span class="sxs-lookup"><span data-stu-id="f5104-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-402">TABLE_NAME</span></span><br />
<span data-ttu-id="f5104-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5104-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-405">21</span><span class="sxs-lookup"><span data-stu-id="f5104-405">21</span></span></p></td>
<td><p><span data-ttu-id="f5104-406">Возвращает преобразования знаков, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5104-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f5104-407">(Переводы строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="f5104-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="f5104-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-412">39</span><span class="sxs-lookup"><span data-stu-id="f5104-412">39</span></span></p></td>
<td><p><span data-ttu-id="f5104-413">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="f5104-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-415">15</span><span class="sxs-lookup"><span data-stu-id="f5104-415">15</span></span></p></td>
<td><p><span data-ttu-id="f5104-416">Возвращает привилегии USAGE для объектов, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="f5104-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="f5104-417">(USAGE_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="f5104-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="f5104-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="f5104-421">ТИП_ОБЪЕКТА</span><span class="sxs-lookup"><span data-stu-id="f5104-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="f5104-422">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="f5104-422">GRANTOR</span></span><br />
<span data-ttu-id="f5104-423">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="f5104-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-425">24</span><span class="sxs-lookup"><span data-stu-id="f5104-425">24</span></span></p></td>
<td><p><span data-ttu-id="f5104-426">Возвращает столбцы, в которых просматриваемые таблицы, определенные в каталоге и принадлежащие указанному пользователю зависят.</span><span class="sxs-lookup"><span data-stu-id="f5104-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="f5104-427">(VIEW_COLUMN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="f5104-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="f5104-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-432">23</span><span class="sxs-lookup"><span data-stu-id="f5104-432">23</span></span></p></td>
<td><p><span data-ttu-id="f5104-433">Возвращает представления, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5104-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f5104-434">(Набор строк ПРЕДСТАВЛЕНИЯ)</span><span class="sxs-lookup"><span data-stu-id="f5104-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f5104-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f5104-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f5104-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f5104-439">25</span><span class="sxs-lookup"><span data-stu-id="f5104-439">25</span></span></p></td>
<td><p><span data-ttu-id="f5104-440">Возвращает таблиц, в котором просматриваемые таблицы, определенные в каталоге и принадлежащие указанному пользователю зависят.</span><span class="sxs-lookup"><span data-stu-id="f5104-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="f5104-441">(VIEW_TABLE_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="f5104-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f5104-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5104-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="f5104-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5104-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="f5104-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="f5104-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f5104-445">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f5104-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="f5104-446">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f5104-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5104-447">Constant</span><span class="sxs-lookup"><span data-stu-id="f5104-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5104-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="f5104-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="f5104-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="f5104-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="f5104-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="f5104-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="f5104-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="f5104-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="f5104-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="f5104-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="f5104-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="f5104-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="f5104-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="f5104-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="f5104-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="f5104-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="f5104-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="f5104-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="f5104-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="f5104-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="f5104-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="f5104-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="f5104-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="f5104-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5104-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="f5104-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f5104-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="f5104-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="f5104-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="f5104-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="f5104-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="f5104-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="f5104-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="f5104-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="f5104-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="f5104-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="f5104-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="f5104-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="f5104-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="f5104-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5104-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="f5104-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5104-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="f5104-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

