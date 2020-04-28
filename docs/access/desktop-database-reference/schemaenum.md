---
title: Счемаенум (Справочник по базам данных Access на компьютере)
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
# <a name="schemaenum"></a><span data-ttu-id="108ba-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="108ba-102">SchemaEnum</span></span>

<span data-ttu-id="108ba-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="108ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="108ba-104">Указывает тип **набора записей** схемы, извлекаемый методом [OpenSchema](openschema-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="108ba-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="108ba-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="108ba-105">Remarks</span></span>

<span data-ttu-id="108ba-106">Дополнительные сведения о функции и столбцах, возвращаемых для каждой константы ADO, можно найти в разделах, посвященных приложению б *справочника по программированию для программистов OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="108ba-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="108ba-107">Имя каждого раздела указано в скобках в разделе Описание следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="108ba-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="108ba-108">Дополнительные сведения о функции и столбцах, возвращаемых для каждой константы ADO MD, можно найти в разделах Chapter 23 документации по *OLE DB для OLAP* .</span><span class="sxs-lookup"><span data-stu-id="108ba-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="108ba-109">Имя каждого раздела указано в круглых скобках и помечено звездочкой (\*) в столбце Описание следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="108ba-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="108ba-110">Переведите типы данных столбцов в документации OLE DB на типы данных ADO, обратившись к столбцу Description раздела ADO [DataTypeEnum](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="108ba-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="108ba-111">Например, тип данных OLE DB для **\_DbType встр** эквивалентен типу данных ADO **адвчар**.</span><span class="sxs-lookup"><span data-stu-id="108ba-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="108ba-112">ADO создает аналогичные схеме результаты для констант, **адсчемадбинфокэйвордс** и **адсчемадбинфолитералс**.</span><span class="sxs-lookup"><span data-stu-id="108ba-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="108ba-113">ADO создает объект **Recordset**, а затем заполняет каждую строку значениями, возвращаемыми соответственно с помощью методов **идбинфо::** и **идбинфо:: жетлитералинфо** .</span><span class="sxs-lookup"><span data-stu-id="108ba-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="108ba-114">Дополнительные сведения об этих методах можно найти в разделе Идбинфо *справки программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="108ba-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="108ba-115">Константа</span><span class="sxs-lookup"><span data-stu-id="108ba-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="108ba-116">Значение</span><span class="sxs-lookup"><span data-stu-id="108ba-116">Value</span></span></p></th>
<th><p><span data-ttu-id="108ba-117">Описание</span><span class="sxs-lookup"><span data-stu-id="108ba-117">Description</span></span></p></th>
<th><p><span data-ttu-id="108ba-118">Столбцы ограничений</span><span class="sxs-lookup"><span data-stu-id="108ba-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="108ba-119"><strong>адсчемаассертс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-120">нуль</span><span class="sxs-lookup"><span data-stu-id="108ba-120">0</span></span></p></td>
<td><p><span data-ttu-id="108ba-121">Возвращает утверждения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="108ba-122">(Набор строк УТВЕРЖДЕНий)</span><span class="sxs-lookup"><span data-stu-id="108ba-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="108ba-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="108ba-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-126"><strong>адсчемакаталогс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-127">1,1</span><span class="sxs-lookup"><span data-stu-id="108ba-127">1</span></span></p></td>
<td><p><span data-ttu-id="108ba-128">Возвращает физические атрибуты, связанные с каталогами, доступными из СУБД.</span><span class="sxs-lookup"><span data-stu-id="108ba-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="108ba-129">(Набор строк для каталога)</span><span class="sxs-lookup"><span data-stu-id="108ba-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-131"><strong>адсчемачарактерсетс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-132">2</span><span class="sxs-lookup"><span data-stu-id="108ba-132">2</span></span></p></td>
<td><p><span data-ttu-id="108ba-133">Возвращает наборы символов, определенные в каталоге и доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="108ba-134">(CHARACTER_SETS набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="108ba-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="108ba-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-138"><strong>адсчемачеккконстраинтс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-139">5 </span><span class="sxs-lookup"><span data-stu-id="108ba-139">5</span></span></p></td>
<td><p><span data-ttu-id="108ba-140">Возвращает проверочные ограничения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="108ba-141">(CHECK_CONSTRAINTS набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="108ba-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="108ba-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-145"><strong>адсчемаколлатионс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-146">4</span><span class="sxs-lookup"><span data-stu-id="108ba-146">3</span></span></p></td>
<td><p><span data-ttu-id="108ba-147">Возвращает параметры сортировки символов, определенные в каталоге и доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="108ba-148">(Набор строк для параметров сортировки)</span><span class="sxs-lookup"><span data-stu-id="108ba-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="108ba-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="108ba-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-152"><strong>адсчемаколумнпривилежес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-153">13</span><span class="sxs-lookup"><span data-stu-id="108ba-153">13</span></span></p></td>
<td><p><span data-ttu-id="108ba-154">Возвращает привилегии для столбцов таблиц, определенных в каталоге и доступных определенному пользователю или предоставленных им.</span><span class="sxs-lookup"><span data-stu-id="108ba-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="108ba-155">(COLUMN_PRIVILEGES набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-158">TABLE_NAME</span></span><br />
<span data-ttu-id="108ba-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="108ba-160">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="108ba-160">GRANTOR</span></span><br />
<span data-ttu-id="108ba-161">ПРАВА</span><span class="sxs-lookup"><span data-stu-id="108ba-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-162"><strong>адсчемаколумнс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-163">4 </span><span class="sxs-lookup"><span data-stu-id="108ba-163">4</span></span></p></td>
<td><p><span data-ttu-id="108ba-164">Возвращает столбцы таблиц (в том числе представлений), определенных в каталоге и доступных определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="108ba-165">(Набор строк COLUMNs)</span><span class="sxs-lookup"><span data-stu-id="108ba-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-168">TABLE_NAME</span></span><br />
<span data-ttu-id="108ba-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-170"><strong>адсчемаколумнсдомаинусаже</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-171">11 </span><span class="sxs-lookup"><span data-stu-id="108ba-171">11</span></span></p></td>
<td><p><span data-ttu-id="108ba-172">Возвращает столбцы, определенные в каталоге, зависящие от домена, определенного в каталоге и принадлежащего указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="108ba-173">(COLUMN_DOMAIN_USAGE набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="108ba-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="108ba-176">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="108ba-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-178"><strong>адсчемаконстраинтколумнусаже</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-179">6 </span><span class="sxs-lookup"><span data-stu-id="108ba-179">6</span></span></p></td>
<td><p><span data-ttu-id="108ba-180">Возвращает столбцы, используемые ссылочными ограничениями, уникальными ограничениями, проверочными ограничениями и утверждениями, определенными в каталоге и принадлежащими заданному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="108ba-181">(CONSTRAINT_COLUMN_USAGE набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-184">TABLE_NAME</span></span><br />
<span data-ttu-id="108ba-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-186"><strong>адсчемаконстраинттаблеусаже</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-187">7 </span><span class="sxs-lookup"><span data-stu-id="108ba-187">7</span></span></p></td>
<td><p><span data-ttu-id="108ba-188">Возвращает таблицы, используемые ссылочными ограничениями, уникальными ограничениями, проверочными ограничениями и утверждениями, определенными в каталоге и принадлежащими определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="108ba-189">(CONSTRAINT_TABLE_USAGE набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-193"><strong>адсчемакубес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-194">32</span><span class="sxs-lookup"><span data-stu-id="108ba-194">32</span></span></p></td>
<td><p><span data-ttu-id="108ba-195">Возвращает сведения о доступных кубах в схеме (или каталоге, если поставщик не поддерживает схемы).</span><span class="sxs-lookup"><span data-stu-id="108ba-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="108ba-196">(Набор строк для КУБОВ \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="108ba-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="108ba-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-200"><strong>адсчемадбинфокэйвордс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-201">более</span><span class="sxs-lookup"><span data-stu-id="108ba-201">30</span></span></p></td>
<td><p><span data-ttu-id="108ba-202">Возвращает список ключевых слов, относящихся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="108ba-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="108ba-203">(Идбинфо:: зарезервированные слова \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-204">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="108ba-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-205"><strong>адсчемадбинфолитералс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-206">длиной</span><span class="sxs-lookup"><span data-stu-id="108ba-206">31</span></span></p></td>
<td><p><span data-ttu-id="108ba-207">Возвращает список литералов, характерных для каждого поставщика, используемых в текстовых командах.</span><span class="sxs-lookup"><span data-stu-id="108ba-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="108ba-208">(Идбинфо:: Жетлитералинфо \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-209">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="108ba-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-210"><strong>адсчемадименсионс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-211">33</span><span class="sxs-lookup"><span data-stu-id="108ba-211">33</span></span></p></td>
<td><p><span data-ttu-id="108ba-212">Возвращает сведения об измерениях в заданном кубе.</span><span class="sxs-lookup"><span data-stu-id="108ba-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="108ba-213">Он содержит по одной строке для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="108ba-213">It has one row for each dimension.</span></span> <span data-ttu-id="108ba-214">(Набор строк измерений \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="108ba-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="108ba-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-217">CUBE_NAME</span></span><br />
<span data-ttu-id="108ba-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="108ba-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-220"><strong>адсчемафореигнкэйс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-221">27</span><span class="sxs-lookup"><span data-stu-id="108ba-221">27</span></span></p></td>
<td><p><span data-ttu-id="108ba-222">Возвращает столбцы внешнего ключа, определенные в каталоге конкретным пользователем.</span><span class="sxs-lookup"><span data-stu-id="108ba-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="108ba-223">(FOREIGN_KEYS набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="108ba-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-230"><strong>адсчемахиерарчиес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-231">34</span><span class="sxs-lookup"><span data-stu-id="108ba-231">34</span></span></p></td>
<td><p><span data-ttu-id="108ba-232">Возвращает сведения о иерархиях, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="108ba-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="108ba-233">(Набор строк "ИЕРАРХИИ" \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="108ba-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="108ba-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-236">CUBE_NAME</span></span><br />
<span data-ttu-id="108ba-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="108ba-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-240"><strong>адсчемаиндексес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-241">12 </span><span class="sxs-lookup"><span data-stu-id="108ba-241">12</span></span></p></td>
<td><p><span data-ttu-id="108ba-242">Возвращает индексы, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="108ba-243">(Набор строк INDEXES)</span><span class="sxs-lookup"><span data-stu-id="108ba-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-246">INDEX_NAME</span></span><br />
<span data-ttu-id="108ba-247">Тип</span><span class="sxs-lookup"><span data-stu-id="108ba-247">TYPE</span></span><br />
<span data-ttu-id="108ba-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-249"><strong>адсчемакэйколумнусаже</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-250">8 </span><span class="sxs-lookup"><span data-stu-id="108ba-250">8</span></span></p></td>
<td><p><span data-ttu-id="108ba-251">Возвращает столбцы, определенные в каталоге и ограниченные ключами определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="108ba-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="108ba-252">(KEY_COLUMN_USAGE набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="108ba-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="108ba-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="108ba-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-258">TABLE_NAME</span></span><br />
<span data-ttu-id="108ba-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-260"><strong>адсчемалевелс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-261">35</span><span class="sxs-lookup"><span data-stu-id="108ba-261">35</span></span></p></td>
<td><p><span data-ttu-id="108ba-262">Возвращает сведения об уровнях, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="108ba-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="108ba-263">(Набор строк "уровни" \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="108ba-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="108ba-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-266">CUBE_NAME</span></span><br />
<span data-ttu-id="108ba-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="108ba-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-271"><strong>адсчемамеасурес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-272">36</span><span class="sxs-lookup"><span data-stu-id="108ba-272">36</span></span></p></td>
<td><p><span data-ttu-id="108ba-273">Возвращает сведения о доступных показателях.</span><span class="sxs-lookup"><span data-stu-id="108ba-273">Returns information about the available measures.</span></span> <span data-ttu-id="108ba-274">(Набор "меры" \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="108ba-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="108ba-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-277">CUBE_NAME</span></span><br />
<span data-ttu-id="108ba-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="108ba-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-280"><strong>адсчемамемберс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-281">38</span><span class="sxs-lookup"><span data-stu-id="108ba-281">38</span></span></p></td>
<td><p><span data-ttu-id="108ba-282">Возвращает сведения о доступных членах.</span><span class="sxs-lookup"><span data-stu-id="108ba-282">Returns information about the available members.</span></span> <span data-ttu-id="108ba-283">(Набор строк "элементы" \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="108ba-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="108ba-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-286">CUBE_NAME</span></span><br />
<span data-ttu-id="108ba-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="108ba-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="108ba-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="108ba-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="108ba-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="108ba-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="108ba-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="108ba-295">Оператор Tree (Дополнительные сведения см. в документации по OLE DB for OLAP.)</span><span class="sxs-lookup"><span data-stu-id="108ba-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-296"><strong>адсчемапримарикэйс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-297">8</span><span class="sxs-lookup"><span data-stu-id="108ba-297">28</span></span></p></td>
<td><p><span data-ttu-id="108ba-298">Возвращает столбцы первичного ключа, определенные в каталоге указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="108ba-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="108ba-299">(PRIMARY_KEYS набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-303"><strong>адсчемапроцедуреколумнс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-304">суммируемых</span><span class="sxs-lookup"><span data-stu-id="108ba-304">29</span></span></p></td>
<td><p><span data-ttu-id="108ba-305">Возвращает сведения о столбцах наборов строк, возвращаемых процедурами.</span><span class="sxs-lookup"><span data-stu-id="108ba-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="108ba-306">(PROCEDURE_COLUMNS набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="108ba-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="108ba-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-311"><strong>адсчемапроцедурепараметерс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-312">26</span><span class="sxs-lookup"><span data-stu-id="108ba-312">26</span></span></p></td>
<td><p><span data-ttu-id="108ba-313">Возвращает сведения о параметрах и кодах возврата процедур.</span><span class="sxs-lookup"><span data-stu-id="108ba-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="108ba-314">(PROCEDURE_PARAMETERS набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="108ba-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="108ba-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-319"><strong>адсчемапроцедурес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-320">16 </span><span class="sxs-lookup"><span data-stu-id="108ba-320">16</span></span></p></td>
<td><p><span data-ttu-id="108ba-321">Возвращает процедуры, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="108ba-322">(Набор строк процедур)</span><span class="sxs-lookup"><span data-stu-id="108ba-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="108ba-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="108ba-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="108ba-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-327"><strong>адсчемапропертиес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-328">37</span><span class="sxs-lookup"><span data-stu-id="108ba-328">37</span></span></p></td>
<td><p><span data-ttu-id="108ba-329">Возвращает сведения о доступных свойствах для каждого уровня измерения.</span><span class="sxs-lookup"><span data-stu-id="108ba-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="108ba-330">(Набор строк "Свойства" \*)</span><span class="sxs-lookup"><span data-stu-id="108ba-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="108ba-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="108ba-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="108ba-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-333">CUBE_NAME</span></span><br />
<span data-ttu-id="108ba-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="108ba-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="108ba-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="108ba-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-340"><strong>адсчемапровидерспеЦифик</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-341">–1</span><span class="sxs-lookup"><span data-stu-id="108ba-341">-1</span></span></p></td>
<td><p><span data-ttu-id="108ba-342">Используется, если поставщик определяет собственные нестандартные запросы схемы.</span><span class="sxs-lookup"><span data-stu-id="108ba-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="108ba-343">&lt;Характерные для поставщика&gt;</span><span class="sxs-lookup"><span data-stu-id="108ba-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-344"><strong>адсчемапровидертипес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-345">22</span><span class="sxs-lookup"><span data-stu-id="108ba-345">22</span></span></p></td>
<td><p><span data-ttu-id="108ba-346">Возвращает (базовые) типы данных, поддерживаемые поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="108ba-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="108ba-347">(PROVIDER_TYPES набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="108ba-348">DATA_TYPE</span></span><br />
<span data-ttu-id="108ba-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="108ba-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-350"><strong>адсчемареферентиалконстраинтс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-351">9 </span><span class="sxs-lookup"><span data-stu-id="108ba-351">9</span></span></p></td>
<td><p><span data-ttu-id="108ba-352">Возвращает ссылочные ограничения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="108ba-353">(REFERENTIAL_CONSTRAINTS набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="108ba-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="108ba-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-357"><strong>адсчемасчемата</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-358">17 </span><span class="sxs-lookup"><span data-stu-id="108ba-358">17</span></span></p></td>
<td><p><span data-ttu-id="108ba-359">Возвращает схемы (объекты базы данных), принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="108ba-360">(Набор строк СЧЕМАТА)</span><span class="sxs-lookup"><span data-stu-id="108ba-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="108ba-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="108ba-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="108ba-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-364"><strong>адсчемаскллангуажес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-365">18 </span><span class="sxs-lookup"><span data-stu-id="108ba-365">18</span></span></p></td>
<td><p><span data-ttu-id="108ba-366">Возвращает уровни соответствия, параметры и диалекты, поддерживаемые данными обработки SQL, определенными в каталоге.</span><span class="sxs-lookup"><span data-stu-id="108ba-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="108ba-367">(SQL_LANGUAGES набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-368">&lt;Нет&gt;</span><span class="sxs-lookup"><span data-stu-id="108ba-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-369"><strong>адсчемастатистикс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-370">19</span><span class="sxs-lookup"><span data-stu-id="108ba-370">19</span></span></p></td>
<td><p><span data-ttu-id="108ba-371">Возвращает статистику, определенную в каталоге, принадлежащем указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="108ba-372">(Набор строк статистики)</span><span class="sxs-lookup"><span data-stu-id="108ba-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-376"><strong>адсчематаблеконстраинтс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-377">10 </span><span class="sxs-lookup"><span data-stu-id="108ba-377">10</span></span></p></td>
<td><p><span data-ttu-id="108ba-378">Возвращает ограничения таблицы, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="108ba-379">(TABLE_CONSTRAINTS набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="108ba-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="108ba-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="108ba-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-385">TABLE_NAME</span></span><br />
<span data-ttu-id="108ba-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="108ba-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-387"><strong>адсчематаблепривилежес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-388">14 </span><span class="sxs-lookup"><span data-stu-id="108ba-388">14</span></span></p></td>
<td><p><span data-ttu-id="108ba-389">Возвращает привилегии для таблиц, определенных в каталоге и доступных определенному пользователю или предоставленных им.</span><span class="sxs-lookup"><span data-stu-id="108ba-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="108ba-390">(TABLE_PRIVILEGES набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-393">TABLE_NAME</span></span><br />
<span data-ttu-id="108ba-394">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="108ba-394">GRANTOR</span></span><br />
<span data-ttu-id="108ba-395">ПРАВА</span><span class="sxs-lookup"><span data-stu-id="108ba-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-396"><strong>адсчематаблес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-397">двадцать</span><span class="sxs-lookup"><span data-stu-id="108ba-397">20</span></span></p></td>
<td><p><span data-ttu-id="108ba-398">Возвращает таблицы (в том числе представления), определенные в каталоге и доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="108ba-399">(Набор строк таблицы)</span><span class="sxs-lookup"><span data-stu-id="108ba-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-402">TABLE_NAME</span></span><br />
<span data-ttu-id="108ba-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="108ba-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-404"><strong>адсчематранслатионс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-405">21</span><span class="sxs-lookup"><span data-stu-id="108ba-405">21</span></span></p></td>
<td><p><span data-ttu-id="108ba-406">Возвращает преобразования символов, определенные в каталоге и доступные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="108ba-407">(Набор строк преобразования)</span><span class="sxs-lookup"><span data-stu-id="108ba-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="108ba-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="108ba-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-411"><strong>адсчематрустис</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-412">39</span><span class="sxs-lookup"><span data-stu-id="108ba-412">39</span></span></p></td>
<td><p><span data-ttu-id="108ba-413">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="108ba-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-414"><strong>адсчемаусажепривилежес</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-415">15 </span><span class="sxs-lookup"><span data-stu-id="108ba-415">15</span></span></p></td>
<td><p><span data-ttu-id="108ba-416">Возвращает привилегии на использование объектов, определенных в каталоге и доступных определенному пользователю или предоставленных им.</span><span class="sxs-lookup"><span data-stu-id="108ba-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="108ba-417">(USAGE_PRIVILEGES набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="108ba-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="108ba-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="108ba-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="108ba-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="108ba-422">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="108ba-422">GRANTOR</span></span><br />
<span data-ttu-id="108ba-423">ПРАВА</span><span class="sxs-lookup"><span data-stu-id="108ba-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-424"><strong>адсчемавиевколумнусаже</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-425">открыт</span><span class="sxs-lookup"><span data-stu-id="108ba-425">24</span></span></p></td>
<td><p><span data-ttu-id="108ba-426">Возвращает столбцы, от которых зависят просмотренные таблицы, определенные в каталоге и принадлежащие определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="108ba-427">(VIEW_COLUMN_USAGE набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="108ba-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="108ba-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-431"><strong>адсчемавиевс</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-432">23</span><span class="sxs-lookup"><span data-stu-id="108ba-432">23</span></span></p></td>
<td><p><span data-ttu-id="108ba-433">Возвращает представления, определенные в каталоге и доступные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="108ba-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="108ba-434">(Набор строк представления)</span><span class="sxs-lookup"><span data-stu-id="108ba-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="108ba-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="108ba-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-438"><strong>адсчемавиевтаблеусаже</strong></span><span class="sxs-lookup"><span data-stu-id="108ba-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="108ba-439">25</span><span class="sxs-lookup"><span data-stu-id="108ba-439">25</span></span></p></td>
<td><p><span data-ttu-id="108ba-440">Возвращает таблицы, в которых все просмотренные таблицы, определенные в каталоге и принадлежащие определенному пользователю, зависят от них.</span><span class="sxs-lookup"><span data-stu-id="108ba-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="108ba-441">(VIEW_TABLE_USAGE набор строк)</span><span class="sxs-lookup"><span data-stu-id="108ba-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="108ba-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="108ba-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="108ba-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="108ba-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="108ba-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="108ba-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="108ba-445">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="108ba-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="108ba-446">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="108ba-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="108ba-447">Константа</span><span class="sxs-lookup"><span data-stu-id="108ba-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="108ba-448">Адоенумс. Schema. ASSERTs</span><span class="sxs-lookup"><span data-stu-id="108ba-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-449">Адоенумс. Schema. CATALOGs</span><span class="sxs-lookup"><span data-stu-id="108ba-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-450">Адоенумс. Schema. ЧАРАКТЕРСЕТС</span><span class="sxs-lookup"><span data-stu-id="108ba-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-451">Адоенумс. Schema. ЧЕКККОНСТРАИНТС</span><span class="sxs-lookup"><span data-stu-id="108ba-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-452">Адоенумс. Schema. Collation</span><span class="sxs-lookup"><span data-stu-id="108ba-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-453">Адоенумс. Schema. КОЛУМНПРИВИЛЕЖЕС</span><span class="sxs-lookup"><span data-stu-id="108ba-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-454">Адоенумс. Schema. COLUMNs</span><span class="sxs-lookup"><span data-stu-id="108ba-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-455">Адоенумс. Schema. КОЛУМНСДОМАИНУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="108ba-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-456">Адоенумс. Schema. КОНСТРАИНТКОЛУМНУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="108ba-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-457">Адоенумс. Schema. КОНСТРАИНТТАБЛЕУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="108ba-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-458">Адоенумс. Schema. CUBEs</span><span class="sxs-lookup"><span data-stu-id="108ba-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-459">Адоенумс. Schema. ДБИНФОКЭЙВОРДС</span><span class="sxs-lookup"><span data-stu-id="108ba-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-460">Адоенумс. Schema. ДБИНФОЛИТЕРАЛС</span><span class="sxs-lookup"><span data-stu-id="108ba-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-461">Адоенумс. Schema. DIMENSIONs</span><span class="sxs-lookup"><span data-stu-id="108ba-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-462">Адоенумс. Schema. ФОРЕИГНКЭЙС</span><span class="sxs-lookup"><span data-stu-id="108ba-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-463">Адоенумс. Schema. ИЕРАРХИИ</span><span class="sxs-lookup"><span data-stu-id="108ba-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-464">Адоенумс. Schema. INDEXES</span><span class="sxs-lookup"><span data-stu-id="108ba-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-465">Адоенумс. Schema. КЭЙКОЛУМНУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="108ba-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-466">Адоенумс. Schema. LEVELs</span><span class="sxs-lookup"><span data-stu-id="108ba-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-467">Адоенумс. Schema. MEASUREs</span><span class="sxs-lookup"><span data-stu-id="108ba-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-468">Адоенумс. Schema. MEMBERs</span><span class="sxs-lookup"><span data-stu-id="108ba-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-469">Адоенумс. Schema. ПРИМАРИКЭЙС</span><span class="sxs-lookup"><span data-stu-id="108ba-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-470">Адоенумс. Schema. ПРОЦЕДУРЕКОЛУМНС</span><span class="sxs-lookup"><span data-stu-id="108ba-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-471">Адоенумс. Schema. ПРОЦЕДУРЕПАРАМЕТЕРС</span><span class="sxs-lookup"><span data-stu-id="108ba-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-472">Адоенумс. Schema. процедуры</span><span class="sxs-lookup"><span data-stu-id="108ba-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-473">Адоенумс. Schema. PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="108ba-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-474">Адоенумс. Schema. ПРОВИДЕРСПЕЦИФИК</span><span class="sxs-lookup"><span data-stu-id="108ba-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-475">Адоенумс. Schema. ПРОВИДЕРТИПЕС</span><span class="sxs-lookup"><span data-stu-id="108ba-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-476">Адоенумс. Schema. РЕФЕРЕНТИАЛКОНТРАИНТС</span><span class="sxs-lookup"><span data-stu-id="108ba-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-477">Адоенумс. Schema. СЧЕМАТА</span><span class="sxs-lookup"><span data-stu-id="108ba-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-478">Адоенумс. Schema. СКЛЛАНГУАЖЕС</span><span class="sxs-lookup"><span data-stu-id="108ba-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-479">Адоенумс. Schema. STATISTICS</span><span class="sxs-lookup"><span data-stu-id="108ba-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-480">Адоенумс. Schema. ТАБЛЕКОНСТРАИНТС</span><span class="sxs-lookup"><span data-stu-id="108ba-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-481">Адоенумс. Schema. ТАБЛЕПРИВИЛЕЖЕС</span><span class="sxs-lookup"><span data-stu-id="108ba-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-482">Адоенумс. Schema. TABLEs</span><span class="sxs-lookup"><span data-stu-id="108ba-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-483">Адоенумс. Schema. translation</span><span class="sxs-lookup"><span data-stu-id="108ba-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-484">Адоенумс. Schema. ДОВЕРЕНные лица</span><span class="sxs-lookup"><span data-stu-id="108ba-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-485">Адоенумс. Schema. УСАЖЕПРИВИЛЕЖЕС</span><span class="sxs-lookup"><span data-stu-id="108ba-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-486">Адоенумс. Schema. ВИЕВКОЛУМНУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="108ba-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="108ba-487">Адоенумс. Schema. VIEWs</span><span class="sxs-lookup"><span data-stu-id="108ba-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="108ba-488">Адоенумс. Schema. ВИЕВТАБЛЕУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="108ba-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

