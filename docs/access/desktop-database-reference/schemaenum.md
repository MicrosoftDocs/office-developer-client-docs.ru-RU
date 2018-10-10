---
title: SchemaEnum (Справочник по для настольных баз данных Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e928271d61cf38232014db1c67482ca6d47fd863
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482813"
---
# <a name="schemaenum"></a><span data-ttu-id="3032f-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="3032f-102">SchemaEnum</span></span>


<span data-ttu-id="3032f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3032f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3032f-104">Указывает тип схемы [OpenSchema](openschema-method-ado.md) метод извлекает **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3032f-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

<span data-ttu-id="3032f-105">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3032f-105">**Remarks**</span></span>

<span data-ttu-id="3032f-106">Дополнительные сведения о функции и столбцов, возвращаемых для каждого константа ADO можно найти в разделах приложение Б *Справочнике программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="3032f-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="3032f-107">Имя каждого раздела отображается в скобки в разделе Описание в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="3032f-107">The name of each topic is listed in parentheses in the Description section of the table below.</span></span>

<span data-ttu-id="3032f-108">Дополнительные сведения о функции и столбцов, возвращаемых для каждого ADO MD константу можно найти в разделах Глава 23 документации *OLE DB для OLAP* .</span><span class="sxs-lookup"><span data-stu-id="3032f-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="3032f-109">Имя каждого раздела приведены в скобках и помеченные звездочкой (\*) в столбце Описание в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="3032f-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the table below.</span></span>

<span data-ttu-id="3032f-110">Преобразования типов данных столбцов в документации по OLE DB для типов данных ADO с помощью ссылки на столбец описание раздела ADO [DataTypeEnum](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="3032f-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="3032f-111">Например, тип данных OLE DB из **DBTYPE\_WSTR** соответствует типу данных ADO из **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="3032f-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="3032f-112">ADO создает аналогичную схемы результаты для константы, **adSchemaDBInfoKeywords** и **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="3032f-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="3032f-113">ADO создает **набор записей**, а затем заполняет каждую строку значения, возвращаемые методы **IDBInfo::GetKeywords** и **IDBInfo::GetLiteralInfo** соответственно.</span><span class="sxs-lookup"><span data-stu-id="3032f-113">ADO creates a **Recordset**, then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="3032f-114">Дополнительные сведения об этих методов можно найти в разделе IDBInfo *Справочник программиста OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="3032f-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference.*</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3032f-115">Константа</span><span class="sxs-lookup"><span data-stu-id="3032f-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="3032f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3032f-116">Value</span></span></p></th>
<th><p><span data-ttu-id="3032f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="3032f-117">Description</span></span></p></th>
<th><p><span data-ttu-id="3032f-118">Ограничение столбцов</span><span class="sxs-lookup"><span data-stu-id="3032f-118">Constraint Columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3032f-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-120">0</span><span class="sxs-lookup"><span data-stu-id="3032f-120">0</span></span></p></td>
<td><p><span data-ttu-id="3032f-121">Возвращает утверждения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="3032f-122">(УТВЕРЖДЕНИЯ строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="3032f-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="3032f-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-127">1</span><span class="sxs-lookup"><span data-stu-id="3032f-127">1</span></span></p></td>
<td><p><span data-ttu-id="3032f-128">Возвращает физические атрибуты, связанные с каталогами, доступными из СУБД.</span><span class="sxs-lookup"><span data-stu-id="3032f-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="3032f-129">(КАТАЛОГИ строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-132">2</span><span class="sxs-lookup"><span data-stu-id="3032f-132">2</span></span></p></td>
<td><p><span data-ttu-id="3032f-133">Возвращает наборы символов, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3032f-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="3032f-134">(CHARACTER_SETS строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="3032f-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="3032f-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-139">5</span><span class="sxs-lookup"><span data-stu-id="3032f-139">5</span></span></p></td>
<td><p><span data-ttu-id="3032f-140">Возвращает ограничения проверки, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="3032f-141">(CHECK_CONSTRAINTS строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="3032f-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="3032f-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-146">3</span><span class="sxs-lookup"><span data-stu-id="3032f-146">3</span></span></p></td>
<td><p><span data-ttu-id="3032f-147">Возвращает параметры сортировки символов, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3032f-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="3032f-148">(Параметры СОРТИРОВКИ строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="3032f-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="3032f-151">АРГУМЕНТ COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-153">13</span><span class="sxs-lookup"><span data-stu-id="3032f-153">13</span></span></p></td>
<td><p><span data-ttu-id="3032f-154">Возвращает привилегии для столбцов таблиц, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="3032f-155">(COLUMN_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-158">TABLE_NAME</span></span><br />
<span data-ttu-id="3032f-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="3032f-160">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="3032f-160">GRANTOR</span></span><br />
<span data-ttu-id="3032f-161">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="3032f-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-163">4</span><span class="sxs-lookup"><span data-stu-id="3032f-163">4</span></span></p></td>
<td><p><span data-ttu-id="3032f-164">Возвращает столбцы таблиц (включая представления) определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3032f-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="3032f-165">(СТОЛБЦЫ строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-168">TABLE_NAME</span></span><br />
<span data-ttu-id="3032f-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-171">11</span><span class="sxs-lookup"><span data-stu-id="3032f-171">11</span></span></p></td>
<td><p><span data-ttu-id="3032f-172">Возвращает столбцы, определенные в каталоге, зависящие от домена, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="3032f-173">(COLUMN_DOMAIN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="3032f-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="3032f-176">ИМЯ_ДОМЕНА</span><span class="sxs-lookup"><span data-stu-id="3032f-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="3032f-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-179">6</span><span class="sxs-lookup"><span data-stu-id="3032f-179">6</span></span></p></td>
<td><p><span data-ttu-id="3032f-180">Возвращает число столбцов, используемых ссылочные ограничения, ограничения уникальности, ограничения и утверждения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="3032f-181">(CONSTRAINT_COLUMN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-184">TABLE_NAME</span></span><br />
<span data-ttu-id="3032f-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-187">7</span><span class="sxs-lookup"><span data-stu-id="3032f-187">7</span></span></p></td>
<td><p><span data-ttu-id="3032f-188">Возвращает таблицы, используемые ссылочные ограничения, ограничения уникальности, ограничения и утверждения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="3032f-189">(CONSTRAINT_TABLE_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-194">32</span><span class="sxs-lookup"><span data-stu-id="3032f-194">32</span></span></p></td>
<td><p><span data-ttu-id="3032f-195">Возвращает сведения о доступных кубов в схемы (или каталога, если поставщик не поддерживает схемы).</span><span class="sxs-lookup"><span data-stu-id="3032f-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="3032f-196">(КУБЫ строк \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="3032f-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="3032f-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-201">30</span><span class="sxs-lookup"><span data-stu-id="3032f-201">30</span></span></p></td>
<td><p><span data-ttu-id="3032f-202">Возвращает список ключевых слов, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="3032f-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="3032f-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-204">&lt;Отсутствует&gt;</span><span class="sxs-lookup"><span data-stu-id="3032f-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-206">31</span><span class="sxs-lookup"><span data-stu-id="3032f-206">31</span></span></p></td>
<td><p><span data-ttu-id="3032f-207">Возвращает список литералов от поставщика, используемых в текст команды.</span><span class="sxs-lookup"><span data-stu-id="3032f-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="3032f-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-209">&lt;Отсутствует&gt;</span><span class="sxs-lookup"><span data-stu-id="3032f-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-211">33</span><span class="sxs-lookup"><span data-stu-id="3032f-211">33</span></span></p></td>
<td><p><span data-ttu-id="3032f-212">Возвращает сведения о размеры данного куба.</span><span class="sxs-lookup"><span data-stu-id="3032f-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="3032f-213">Она содержится одна строка для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="3032f-213">It has one row for each dimension.</span></span> <span data-ttu-id="3032f-214">(РАЗМЕРЫ строк \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="3032f-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="3032f-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-217">CUBE_NAME</span></span><br />
<span data-ttu-id="3032f-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="3032f-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-221">27</span><span class="sxs-lookup"><span data-stu-id="3032f-221">27</span></span></p></td>
<td><p><span data-ttu-id="3032f-222">Возвращает столбцы внешнего ключа, определенные в каталоге данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="3032f-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="3032f-223">(FOREIGN_KEYS строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="3032f-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-231">34</span><span class="sxs-lookup"><span data-stu-id="3032f-231">34</span></span></p></td>
<td><p><span data-ttu-id="3032f-232">Возвращает сведения о иерархий, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="3032f-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="3032f-233">(ИЕРАРХИИ строк \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="3032f-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="3032f-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-236">CUBE_NAME</span></span><br />
<span data-ttu-id="3032f-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="3032f-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-241">12</span><span class="sxs-lookup"><span data-stu-id="3032f-241">12</span></span></p></td>
<td><p><span data-ttu-id="3032f-242">Возвращает индексы, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="3032f-243">(ИНДЕКСЫ строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-246">INDEX_NAME</span></span><br />
<span data-ttu-id="3032f-247">ТИП</span><span class="sxs-lookup"><span data-stu-id="3032f-247">TYPE</span></span><br />
<span data-ttu-id="3032f-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-250">8</span><span class="sxs-lookup"><span data-stu-id="3032f-250">8</span></span></p></td>
<td><p><span data-ttu-id="3032f-251">Возвращает столбцы, определенные в каталоге, ограниченные как ключи данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="3032f-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="3032f-252">(Набор строк KEY_COLUMN_USAGE служит для указания)</span><span class="sxs-lookup"><span data-stu-id="3032f-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="3032f-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="3032f-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="3032f-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-258">TABLE_NAME</span></span><br />
<span data-ttu-id="3032f-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-261">35</span><span class="sxs-lookup"><span data-stu-id="3032f-261">35</span></span></p></td>
<td><p><span data-ttu-id="3032f-262">Возвращает сведения о доступных в измерении уровней.</span><span class="sxs-lookup"><span data-stu-id="3032f-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="3032f-263">(Уровни строк \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="3032f-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="3032f-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-266">CUBE_NAME</span></span><br />
<span data-ttu-id="3032f-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="3032f-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-272">36</span><span class="sxs-lookup"><span data-stu-id="3032f-272">36</span></span></p></td>
<td><p><span data-ttu-id="3032f-273">Возвращает сведения о доступных мер.</span><span class="sxs-lookup"><span data-stu-id="3032f-273">Returns information about the available measures.</span></span> <span data-ttu-id="3032f-274">(Набор строк меры \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="3032f-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="3032f-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-277">CUBE_NAME</span></span><br />
<span data-ttu-id="3032f-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="3032f-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-281">38</span><span class="sxs-lookup"><span data-stu-id="3032f-281">38</span></span></p></td>
<td><p><span data-ttu-id="3032f-282">Возвращает сведения о доступных членов.</span><span class="sxs-lookup"><span data-stu-id="3032f-282">Returns information about the available members.</span></span> <span data-ttu-id="3032f-283">(Строк MEMBERS \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="3032f-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="3032f-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-286">CUBE_NAME</span></span><br />
<span data-ttu-id="3032f-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="3032f-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="3032f-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="3032f-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="3032f-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="3032f-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="3032f-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="3032f-295">Оператор дерева (Дополнительные сведения см. в OLE DB для OLAP документации.)</span><span class="sxs-lookup"><span data-stu-id="3032f-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-297">28</span><span class="sxs-lookup"><span data-stu-id="3032f-297">28</span></span></p></td>
<td><p><span data-ttu-id="3032f-298">Возвращает столбцы первичных ключей, определенные в каталоге данным пользователем.</span><span class="sxs-lookup"><span data-stu-id="3032f-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="3032f-299">(PRIMARY_KEYS строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-304">29</span><span class="sxs-lookup"><span data-stu-id="3032f-304">29</span></span></p></td>
<td><p><span data-ttu-id="3032f-305">Возвращает сведения о столбцах наборы строк, возвращаемых процедурами.</span><span class="sxs-lookup"><span data-stu-id="3032f-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="3032f-306">(PROCEDURE_COLUMNS строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="3032f-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="3032f-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-312">26</span><span class="sxs-lookup"><span data-stu-id="3032f-312">26</span></span></p></td>
<td><p><span data-ttu-id="3032f-313">Возвращает сведения о параметрах и кодах возврата процедур.</span><span class="sxs-lookup"><span data-stu-id="3032f-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="3032f-314">(PROCEDURE_PARAMETERS строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="3032f-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="3032f-318">ИМЯ_ПАРАМЕТРА</span><span class="sxs-lookup"><span data-stu-id="3032f-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-320">16</span><span class="sxs-lookup"><span data-stu-id="3032f-320">16</span></span></p></td>
<td><p><span data-ttu-id="3032f-321">Возвращает процедуры, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="3032f-322">(ПРОЦЕДУРЫ строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="3032f-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="3032f-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3032f-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-328">37</span><span class="sxs-lookup"><span data-stu-id="3032f-328">37</span></span></p></td>
<td><p><span data-ttu-id="3032f-329">Возвращает сведения о свойствах, доступных для каждого уровня измерения.</span><span class="sxs-lookup"><span data-stu-id="3032f-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="3032f-330">(Набор строк свойства \*)</span><span class="sxs-lookup"><span data-stu-id="3032f-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="3032f-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="3032f-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="3032f-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-333">CUBE_NAME</span></span><br />
<span data-ttu-id="3032f-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="3032f-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="3032f-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="3032f-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-341">-1</span><span class="sxs-lookup"><span data-stu-id="3032f-341">-1</span></span></p></td>
<td><p><span data-ttu-id="3032f-342">Используется, если поставщик определяет нестандартного схемы запросов.</span><span class="sxs-lookup"><span data-stu-id="3032f-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="3032f-343">&lt;Поставщика&gt;</span><span class="sxs-lookup"><span data-stu-id="3032f-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-345">22</span><span class="sxs-lookup"><span data-stu-id="3032f-345">22</span></span></p></td>
<td><p><span data-ttu-id="3032f-346">Возвращает типы данных (базовый), поддерживаемых поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="3032f-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="3032f-347">(Строк PROVIDER_TYPES)</span><span class="sxs-lookup"><span data-stu-id="3032f-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="3032f-348">DATA_TYPE</span></span><br />
<span data-ttu-id="3032f-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="3032f-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-351">9</span><span class="sxs-lookup"><span data-stu-id="3032f-351">9</span></span></p></td>
<td><p><span data-ttu-id="3032f-352">Возвращает ссылочные ограничения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="3032f-353">(REFERENTIAL_CONSTRAINTS строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="3032f-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="3032f-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-358">17</span><span class="sxs-lookup"><span data-stu-id="3032f-358">17</span></span></p></td>
<td><p><span data-ttu-id="3032f-359">Возвращает схемы (объекты базы данных), принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="3032f-360">(СХЕМ строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="3032f-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="3032f-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="3032f-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-365">18</span><span class="sxs-lookup"><span data-stu-id="3032f-365">18</span></span></p></td>
<td><p><span data-ttu-id="3032f-366">Возвращает уровни соответствия, параметры и языки меньшинств, поддерживаемые данными обработки реализации SQL, определенные в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3032f-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="3032f-367">(SQL_LANGUAGES строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-368">&lt;Отсутствует&gt;</span><span class="sxs-lookup"><span data-stu-id="3032f-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-370">19</span><span class="sxs-lookup"><span data-stu-id="3032f-370">19</span></span></p></td>
<td><p><span data-ttu-id="3032f-371">Возвращает статистику, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="3032f-372">(СТАТИСТИКА строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-377">10</span><span class="sxs-lookup"><span data-stu-id="3032f-377">10</span></span></p></td>
<td><p><span data-ttu-id="3032f-378">Возвращает табличные ограничения, определенные в каталоге, принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="3032f-379">(Набор строк TABLE_CONSTRAINTS служит для указания)</span><span class="sxs-lookup"><span data-stu-id="3032f-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="3032f-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="3032f-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="3032f-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-385">TABLE_NAME</span></span><br />
<span data-ttu-id="3032f-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="3032f-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-388">14</span><span class="sxs-lookup"><span data-stu-id="3032f-388">14</span></span></p></td>
<td><p><span data-ttu-id="3032f-389">Возвращает привилегии для таблиц, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="3032f-390">(TABLE_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-393">TABLE_NAME</span></span><br />
<span data-ttu-id="3032f-394">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="3032f-394">GRANTOR</span></span><br />
<span data-ttu-id="3032f-395">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="3032f-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-397">20</span><span class="sxs-lookup"><span data-stu-id="3032f-397">20</span></span></p></td>
<td><p><span data-ttu-id="3032f-398">Возвращает таблицы (включая представления) определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3032f-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="3032f-399">(Набор строк таблицы)</span><span class="sxs-lookup"><span data-stu-id="3032f-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-402">TABLE_NAME</span></span><br />
<span data-ttu-id="3032f-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3032f-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-405">21</span><span class="sxs-lookup"><span data-stu-id="3032f-405">21</span></span></p></td>
<td><p><span data-ttu-id="3032f-406">Возвращает преобразования знаков, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3032f-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="3032f-407">(Переводы строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="3032f-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="3032f-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-412">39</span><span class="sxs-lookup"><span data-stu-id="3032f-412">39</span></span></p></td>
<td><p><span data-ttu-id="3032f-413">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="3032f-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-415">15</span><span class="sxs-lookup"><span data-stu-id="3032f-415">15</span></span></p></td>
<td><p><span data-ttu-id="3032f-416">Возвращает привилегии USAGE для объектов, определенные в каталоге, доступных для или предоставленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="3032f-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="3032f-417">(USAGE_PRIVILEGES строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="3032f-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="3032f-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="3032f-421">ТИП_ОБЪЕКТА</span><span class="sxs-lookup"><span data-stu-id="3032f-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="3032f-422">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="3032f-422">GRANTOR</span></span><br />
<span data-ttu-id="3032f-423">ОБЪЕКТ, ПОЛУЧАЮЩИЙ</span><span class="sxs-lookup"><span data-stu-id="3032f-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-425">24</span><span class="sxs-lookup"><span data-stu-id="3032f-425">24</span></span></p></td>
<td><p><span data-ttu-id="3032f-426">Возвращает столбцы, в которых просматриваемые таблицы, определенные в каталоге и принадлежащие указанному пользователю зависят.</span><span class="sxs-lookup"><span data-stu-id="3032f-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="3032f-427">(VIEW_COLUMN_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="3032f-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="3032f-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-432">23</span><span class="sxs-lookup"><span data-stu-id="3032f-432">23</span></span></p></td>
<td><p><span data-ttu-id="3032f-433">Возвращает представления, определенные в каталоге, доступных пользователям определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3032f-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="3032f-434">(Набор строк ПРЕДСТАВЛЕНИЯ)</span><span class="sxs-lookup"><span data-stu-id="3032f-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="3032f-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="3032f-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="3032f-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="3032f-439">25</span><span class="sxs-lookup"><span data-stu-id="3032f-439">25</span></span></p></td>
<td><p><span data-ttu-id="3032f-440">Возвращает таблиц, в котором просматриваемые таблицы, определенные в каталоге и принадлежащие указанному пользователю зависят.</span><span class="sxs-lookup"><span data-stu-id="3032f-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="3032f-441">(VIEW_TABLE_USAGE строк)</span><span class="sxs-lookup"><span data-stu-id="3032f-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="3032f-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3032f-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="3032f-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="3032f-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="3032f-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="3032f-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3032f-445">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="3032f-445">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="3032f-446">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3032f-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3032f-447">Constant</span><span class="sxs-lookup"><span data-stu-id="3032f-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3032f-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="3032f-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="3032f-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="3032f-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="3032f-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="3032f-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="3032f-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="3032f-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="3032f-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="3032f-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="3032f-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="3032f-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="3032f-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="3032f-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="3032f-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="3032f-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="3032f-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="3032f-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="3032f-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="3032f-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="3032f-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="3032f-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="3032f-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="3032f-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3032f-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="3032f-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3032f-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="3032f-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="3032f-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="3032f-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="3032f-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="3032f-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="3032f-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="3032f-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="3032f-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="3032f-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="3032f-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="3032f-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="3032f-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="3032f-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3032f-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="3032f-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3032f-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="3032f-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

