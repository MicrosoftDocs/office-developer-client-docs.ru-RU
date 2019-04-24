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
# <a name="schemaenum"></a><span data-ttu-id="4a3e9-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="4a3e9-102">SchemaEnum</span></span>

<span data-ttu-id="4a3e9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a3e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a3e9-104">Указывает тип **набора записей** схемы, извлекаемый методом [OpenSchema](openschema-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4a3e9-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a3e9-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="4a3e9-105">Remarks</span></span>

<span data-ttu-id="4a3e9-106">Дополнительные сведения о функции и столбцах, возвращаемых для каждой константы ADO, можно найти в разделах, посвященных приложению Б справочника по программированию для *программистОв OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="4a3e9-107">Имя каждого раздела указано в скобках в разделе Описание следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="4a3e9-108">Дополнительные сведения о функции и столбцах, возвращаемых для каждой константы ADO MD, можно найти в разделах Chapter 23 документации по *OLE DB для OLAP* .</span><span class="sxs-lookup"><span data-stu-id="4a3e9-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="4a3e9-109">Имя каждого раздела указано в круглых скобках и помечено звездочкой (\*) в столбце Описание следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="4a3e9-110">Переведите типы данных столбцов в документации OLE DB на типы данных ADO, обратившись к столбцу Description раздела ADO [DataTypeEnum](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="4a3e9-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="4a3e9-111">Например, тип данных OLE DB для **\_DbType встр** эквивалентен типу данных ADO **адвчар**.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="4a3e9-112">ADO создает аналогичные схеме результаты для констант, **адсчемадбинфокэйвордс** и **адсчемадбинфолитералс**.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="4a3e9-113">ADO создает объект **Recordset**, а затем заполняет каждую строку значениями, возвращаемыми соответственно с помощью методов **идбинфо::** и **идбинфо:: жетлитералинфо** .</span><span class="sxs-lookup"><span data-stu-id="4a3e9-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="4a3e9-114">Дополнительные сведения об этих методах можно найти в разделе Идбинфо *справки программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="4a3e9-115">Константа</span><span class="sxs-lookup"><span data-stu-id="4a3e9-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="4a3e9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4a3e9-116">Value</span></span></p></th>
<th><p><span data-ttu-id="4a3e9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4a3e9-117">Description</span></span></p></th>
<th><p><span data-ttu-id="4a3e9-118">Столбцы ограничений</span><span class="sxs-lookup"><span data-stu-id="4a3e9-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-119"><strong>Адсчемаассертс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-120">нуль</span><span class="sxs-lookup"><span data-stu-id="4a3e9-120">0</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-121">Возвращает утверждения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4a3e9-122">(Набор строк УТВЕРЖДЕНий)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-123">КОНСТРАИНТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-124">КОНСТРАИНТ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-125">КОНСТРАИНТ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-126"><strong>Адсчемакаталогс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-127">1,1</span><span class="sxs-lookup"><span data-stu-id="4a3e9-127">1</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-128">Возвращает физические атрибуты, связанные с каталогами, доступными из СУБД.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="4a3e9-129">(Набор строк для каталога)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-130">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-131"><strong>Адсчемачарактерсетс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-132">2</span><span class="sxs-lookup"><span data-stu-id="4a3e9-132">2</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-133">Возвращает наборы символов, определенные в каталоге и доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4a3e9-134">(Набор строк ЧАРАКТЕР_СЕТС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-135">ЧАРАКТЕР_СЕТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-136">ЧАРАКТЕР_СЕТ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-137">ЧАРАКТЕР_СЕТ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-138"><strong>Адсчемачеккконстраинтс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-139">17:00</span><span class="sxs-lookup"><span data-stu-id="4a3e9-139">5</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-140">Возвращает проверочные ограничения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4a3e9-141">(Набор строк CHECK_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-142">КОНСТРАИНТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-143">КОНСТРАИНТ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-144">КОНСТРАИНТ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-145"><strong>Адсчемаколлатионс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-146">4</span><span class="sxs-lookup"><span data-stu-id="4a3e9-146">3</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-147">Возвращает параметры сортировки символов, определенные в каталоге и доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4a3e9-148">(Набор строк для параметров сортировки)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-149">КОЛЛАТИОН_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-150">КОЛЛАТИОН_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-151">КОЛЛАТИОН_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-152"><strong>Адсчемаколумнпривилежес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-153">13</span><span class="sxs-lookup"><span data-stu-id="4a3e9-153">13</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-154">Возвращает привилегии для столбцов таблиц, определенных в каталоге и доступных определенному пользователю или предоставленных им.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4a3e9-155">(Набор строк КОЛУМН_ПРИВИЛЕЖЕС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-156">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-157">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-158">TABLE_NAME</span></span><br />
<span data-ttu-id="4a3e9-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="4a3e9-160">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-160">GRANTOR</span></span><br />
<span data-ttu-id="4a3e9-161">ПРАВА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-162"><strong>Адсчемаколумнс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-163">SP4</span><span class="sxs-lookup"><span data-stu-id="4a3e9-163">4</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-164">Возвращает столбцы таблиц (в том числе представлений), определенных в каталоге и доступных определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4a3e9-165">(Набор строк COLUMNs)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-166">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-167">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-168">TABLE_NAME</span></span><br />
<span data-ttu-id="4a3e9-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-170"><strong>Адсчемаколумнсдомаинусаже</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-171">-11:00</span><span class="sxs-lookup"><span data-stu-id="4a3e9-171">11</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-172">Возвращает столбцы, определенные в каталоге, зависящие от домена, определенного в каталоге и принадлежащего указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4a3e9-173">(Набор строк КОЛУМН_ДОМАИН_УСАЖЕ)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-174">ДОМАИН_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-175">ДОМАИН_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-176">ИМЯ_ДОМЕНА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="4a3e9-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-178"><strong>Адсчемаконстраинтколумнусаже</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-179">ICMPv6</span><span class="sxs-lookup"><span data-stu-id="4a3e9-179">6</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-180">Возвращает столбцы, используемые ссылочными ограничениями, уникальными ограничениями, проверочными ограничениями и утверждениями, определенными в каталоге и принадлежащими заданному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4a3e9-181">(Набор строк КОНСТРАИНТ_КОЛУМН_УСАЖЕ)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-182">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-183">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-184">TABLE_NAME</span></span><br />
<span data-ttu-id="4a3e9-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-186"><strong>Адсчемаконстраинттаблеусаже</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-187">см</span><span class="sxs-lookup"><span data-stu-id="4a3e9-187">7</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-188">Возвращает таблицы, используемые ссылочными ограничениями, уникальными ограничениями, проверочными ограничениями и утверждениями, определенными в каталоге и принадлежащими определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4a3e9-189">(Набор строк КОНСТРАИНТ_ТАБЛЕ_УСАЖЕ)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-190">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-191">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-193"><strong>Адсчемакубес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-194">32</span><span class="sxs-lookup"><span data-stu-id="4a3e9-194">32</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-195">Возвращает сведения о доступных кубах в схеме (или каталоге, если поставщик не поддерживает схемы).</span><span class="sxs-lookup"><span data-stu-id="4a3e9-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="4a3e9-196">(Набор строк для КУБОВ \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-197">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="4a3e9-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4a3e9-199">КУБЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-200"><strong>Адсчемадбинфокэйвордс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-201">более</span><span class="sxs-lookup"><span data-stu-id="4a3e9-201">30</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-202">Возвращает список ключевых слов, относящихся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="4a3e9-203">(Идбинфо:: заРезервированные слова \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-204">&lt;Видим&gt;</span><span class="sxs-lookup"><span data-stu-id="4a3e9-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-205"><strong>Адсчемадбинфолитералс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-206">длиной</span><span class="sxs-lookup"><span data-stu-id="4a3e9-206">31</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-207">Возвращает список литералов, характерных для каждого поставщика, используемых в текстовых командах.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="4a3e9-208">(Идбинфо:: Жетлитералинфо \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-209">&lt;Видим&gt;</span><span class="sxs-lookup"><span data-stu-id="4a3e9-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-210"><strong>Адсчемадименсионс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-211">33</span><span class="sxs-lookup"><span data-stu-id="4a3e9-211">33</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-212">Возвращает сведения об измерениях в заданном кубе.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="4a3e9-213">Он содержит по одной строке для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-213">It has one row for each dimension.</span></span> <span data-ttu-id="4a3e9-214">(Набор строк измерений \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-215">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="4a3e9-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4a3e9-217">КУБЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-217">CUBE_NAME</span></span><br />
<span data-ttu-id="4a3e9-218">ДИМЕНСИОН_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="4a3e9-219">ДИМЕНСИОН_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-220"><strong>Адсчемафореигнкэйс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-221">27</span><span class="sxs-lookup"><span data-stu-id="4a3e9-221">27</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-222">Возвращает столбцы внешнего ключа, определенные в каталоге конкретным пользователем.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="4a3e9-223">(Набор строк ФОРЕИГН_КЭЙС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-224">ПК_ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-225">ПК_ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-226">ПК_ТАБЛЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="4a3e9-227">ФК_ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-228">ФК_ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-229">ФК_ТАБЛЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-230"><strong>Адсчемахиерарчиес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-231">34</span><span class="sxs-lookup"><span data-stu-id="4a3e9-231">34</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-232">Возвращает сведения о иерархиях, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="4a3e9-233">(Набор строк "ИЕРАРХИИ" \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-234">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="4a3e9-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4a3e9-236">КУБЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-236">CUBE_NAME</span></span><br />
<span data-ttu-id="4a3e9-237">ДИМЕНСИОН_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-238">ХИЕРАРЧИ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="4a3e9-239">ХИЕРАРЧИ_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-240"><strong>Адсчемаиндексес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-241">12</span><span class="sxs-lookup"><span data-stu-id="4a3e9-241">12</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-242">Возвращает индексы, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4a3e9-243">(Набор строк INDEXES)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-244">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-245">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-246">ИНДЕКС_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-246">INDEX_NAME</span></span><br />
<span data-ttu-id="4a3e9-247">Тип</span><span class="sxs-lookup"><span data-stu-id="4a3e9-247">TYPE</span></span><br />
<span data-ttu-id="4a3e9-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-249"><strong>Адсчемакэйколумнусаже</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-250">8,5</span><span class="sxs-lookup"><span data-stu-id="4a3e9-250">8</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-251">Возвращает столбцы, определенные в каталоге и ограниченные ключами определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="4a3e9-252">(Набор строк КЭЙ_КОЛУМН_УСАЖЕ)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-253">КОНСТРАИНТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-254">КОНСТРАИНТ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-255">КОНСТРАИНТ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="4a3e9-256">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-257">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-258">TABLE_NAME</span></span><br />
<span data-ttu-id="4a3e9-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-260"><strong>Адсчемалевелс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-261">35</span><span class="sxs-lookup"><span data-stu-id="4a3e9-261">35</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-262">Возвращает сведения об уровнях, доступных в измерении.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="4a3e9-263">(Набор строк "уровни" \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-264">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="4a3e9-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4a3e9-266">КУБЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-266">CUBE_NAME</span></span><br />
<span data-ttu-id="4a3e9-267">ДИМЕНСИОН_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-268">ХИЕРАРЧИ_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-269">ЛЕВЕЛ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="4a3e9-270">ЛЕВЕЛ_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-271"><strong>Адсчемамеасурес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-272">36</span><span class="sxs-lookup"><span data-stu-id="4a3e9-272">36</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-273">Возвращает сведения о доступных показателях.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-273">Returns information about the available measures.</span></span> <span data-ttu-id="4a3e9-274">(Набор "меры" \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-275">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="4a3e9-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4a3e9-277">КУБЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-277">CUBE_NAME</span></span><br />
<span data-ttu-id="4a3e9-278">МЕАСУРЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="4a3e9-279">МЕАСУРЕ_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-280"><strong>Адсчемамемберс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-281">38</span><span class="sxs-lookup"><span data-stu-id="4a3e9-281">38</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-282">Возвращает сведения о доступных членах.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-282">Returns information about the available members.</span></span> <span data-ttu-id="4a3e9-283">(Набор строк "элементы" \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-284">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="4a3e9-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4a3e9-286">КУБЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-286">CUBE_NAME</span></span><br />
<span data-ttu-id="4a3e9-287">ДИМЕНСИОН_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-288">ХИЕРАРЧИ_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-289">ЛЕВЕЛ_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-290">ЛЕВЕЛ_НУМБЕР</span><span class="sxs-lookup"><span data-stu-id="4a3e9-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="4a3e9-291">МЕМБЕР_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="4a3e9-292">МЕМБЕР_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-293">МЕМБЕР_КАПТИОН</span><span class="sxs-lookup"><span data-stu-id="4a3e9-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="4a3e9-294">МЕМБЕР_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="4a3e9-295">Оператор Tree (Дополнительные сведения см. в документации по OLE DB for OLAP.)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-296"><strong>Адсчемапримарикэйс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-297">8</span><span class="sxs-lookup"><span data-stu-id="4a3e9-297">28</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-298">Возвращает столбцы первичного ключа, определенные в каталоге указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="4a3e9-299">(Набор строк ПРИМАРИ_КЭЙС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-300">ПК_ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-301">ПК_ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-302">ПК_ТАБЛЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-303"><strong>Адсчемапроцедуреколумнс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-304">суммируемых</span><span class="sxs-lookup"><span data-stu-id="4a3e9-304">29</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-305">Возвращает сведения о столбцах наборов строк, возвращаемых процедурами.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="4a3e9-306">(Набор строк ПРОЦЕДУРЕ_КОЛУМНС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-307">ПРОЦЕДУРЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-308">ПРОЦЕДУРЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-309">ПРОЦЕДУРЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4a3e9-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-311"><strong>Адсчемапроцедурепараметерс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-312">26</span><span class="sxs-lookup"><span data-stu-id="4a3e9-312">26</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-313">Возвращает сведения о параметрах и кодах возврата процедур.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="4a3e9-314">(Набор строк ПРОЦЕДУРЕ_ПАРАМЕТЕРС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-315">ПРОЦЕДУРЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-316">ПРОЦЕДУРЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-317">ПРОЦЕДУРЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4a3e9-318">ПАРАМЕТЕР_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-319"><strong>Адсчемапроцедурес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-320">столбцов</span><span class="sxs-lookup"><span data-stu-id="4a3e9-320">16</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-321">Возвращает процедуры, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4a3e9-322">(Набор строк процедур)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-323">ПРОЦЕДУРЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-324">ПРОЦЕДУРЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-325">ПРОЦЕДУРЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4a3e9-326">ПРОЦЕДУРЕ_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-327"><strong>Адсчемапропертиес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-328">37</span><span class="sxs-lookup"><span data-stu-id="4a3e9-328">37</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-329">Возвращает сведения о доступных свойствах для каждого уровня измерения.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="4a3e9-330">(Набор строк "Свойства" \*)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-331">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="4a3e9-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4a3e9-333">КУБЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-333">CUBE_NAME</span></span><br />
<span data-ttu-id="4a3e9-334">ДИМЕНСИОН_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-335">ХИЕРАРЧИ_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-336">ЛЕВЕЛ_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-337">МЕМБЕР_УНИКУЕ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4a3e9-338">ПРОПЕРТИ_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="4a3e9-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-340"><strong>АдсчемапровидерспеЦифик</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-341">–1</span><span class="sxs-lookup"><span data-stu-id="4a3e9-341">-1</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-342">Используется, если поставщик определяет собственные нестандартные запросы схемы.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-343">&lt;Характерные для поставщика&gt;</span><span class="sxs-lookup"><span data-stu-id="4a3e9-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-344"><strong>Адсчемапровидертипес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-345">22</span><span class="sxs-lookup"><span data-stu-id="4a3e9-345">22</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-346">Возвращает (базовые) типы данных, поддерживаемые поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="4a3e9-347">(Набор строк ПРОВИДЕР_ТИПЕС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4a3e9-348">DATA_TYPE</span></span><br />
<span data-ttu-id="4a3e9-349">БЕСТ_МАТЧ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-350"><strong>Адсчемареферентиалконстраинтс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-351">10</span><span class="sxs-lookup"><span data-stu-id="4a3e9-351">9</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-352">Возвращает ссылочные ограничения, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4a3e9-353">(Набор строк РЕФЕРЕНТИАЛ_КОНСТРАИНТС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-354">КОНСТРАИНТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-355">КОНСТРАИНТ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-356">КОНСТРАИНТ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-357"><strong>Адсчемасчемата</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-358">17</span><span class="sxs-lookup"><span data-stu-id="4a3e9-358">17</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-359">Возвращает схемы (объекты базы данных), принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="4a3e9-360">(Набор строк СЧЕМАТА)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-361">КАТАЛОГ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="4a3e9-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4a3e9-363">СЧЕМА_ОВНЕР</span><span class="sxs-lookup"><span data-stu-id="4a3e9-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-364"><strong>Адсчемаскллангуажес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-365">0,18</span><span class="sxs-lookup"><span data-stu-id="4a3e9-365">18</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-366">Возвращает уровни соответствия, параметры и диалекты, поддерживаемые данными обработки SQL, определенными в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="4a3e9-367">(Набор строк СКЛ_ЛАНГУАЖЕС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-368">&lt;Видим&gt;</span><span class="sxs-lookup"><span data-stu-id="4a3e9-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-369"><strong>Адсчемастатистикс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-370">19</span><span class="sxs-lookup"><span data-stu-id="4a3e9-370">19</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-371">Возвращает статистику, определенную в каталоге, принадлежащем указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4a3e9-372">(Набор строк статистики)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-373">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-374">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-376"><strong>Адсчематаблеконстраинтс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-377">десяти</span><span class="sxs-lookup"><span data-stu-id="4a3e9-377">10</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-378">Возвращает ограничения таблицы, определенные в каталоге и принадлежащие указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4a3e9-379">(Набор строк ТАБЛЕ_КОНСТРАИНТС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-380">КОНСТРАИНТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-381">КОНСТРАИНТ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-382">КОНСТРАИНТ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="4a3e9-383">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-384">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-385">TABLE_NAME</span></span><br />
<span data-ttu-id="4a3e9-386">КОНСТРАИНТ_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-387"><strong>Адсчематаблепривилежес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-388">14</span><span class="sxs-lookup"><span data-stu-id="4a3e9-388">14</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-389">Возвращает привилегии для таблиц, определенных в каталоге и доступных определенному пользователю или предоставленных им.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4a3e9-390">(Набор строк ТАБЛЕ_ПРИВИЛЕЖЕС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-391">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-392">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-393">TABLE_NAME</span></span><br />
<span data-ttu-id="4a3e9-394">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-394">GRANTOR</span></span><br />
<span data-ttu-id="4a3e9-395">ПРАВА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-396"><strong>Адсчематаблес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-397">двадцать</span><span class="sxs-lookup"><span data-stu-id="4a3e9-397">20</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-398">Возвращает таблицы (в том числе представления), определенные в каталоге и доступные определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4a3e9-399">(Набор строк таблицы)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-400">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-401">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-402">TABLE_NAME</span></span><br />
<span data-ttu-id="4a3e9-403">ТАБЛЕ_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-404"><strong>Адсчематранслатионс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-405">21</span><span class="sxs-lookup"><span data-stu-id="4a3e9-405">21</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-406">Возвращает преобразования символов, определенные в каталоге и доступные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4a3e9-407">(Набор строк преобразования)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-408">ТРАНСЛАТИОН_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-409">ТРАНСЛАТИОН_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-410">ТРАНСЛАТИОН_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-411"><strong>Адсчематрустис</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-412">39</span><span class="sxs-lookup"><span data-stu-id="4a3e9-412">39</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-413">Зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-414"><strong>Адсчемаусажепривилежес</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-415">означает</span><span class="sxs-lookup"><span data-stu-id="4a3e9-415">15</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-416">Возвращает привилегии на использование объектов, определенных в каталоге и доступных определенному пользователю или предоставленных им.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4a3e9-417">(Набор строк УСАЖЕ_ПРИВИЛЕЖЕС)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-418">ОБЖЕКТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-419">ОБЖЕКТ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="4a3e9-421">ОБЖЕКТ_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="4a3e9-422">ПРЕДОСТАВЛЕНИЕИЛИ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-422">GRANTOR</span></span><br />
<span data-ttu-id="4a3e9-423">ПРАВА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-424"><strong>Адсчемавиевколумнусаже</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-425">открыт</span><span class="sxs-lookup"><span data-stu-id="4a3e9-425">24</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-426">Возвращает столбцы, от которых зависят просмотренные таблицы, определенные в каталоге и принадлежащие определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="4a3e9-427">(Набор строк ВИЕВ_КОЛУМН_УСАЖЕ)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-428">ВИЕВ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-429">ВИЕВ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-430">ВИЕВ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-431"><strong>Адсчемавиевс</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-432">23</span><span class="sxs-lookup"><span data-stu-id="4a3e9-432">23</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-433">Возвращает представления, определенные в каталоге и доступные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4a3e9-434">(Набор строк представления)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-435">ТАБЛЕ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-436">ТАБЛЕ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4a3e9-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-438"><strong>Адсчемавиевтаблеусаже</strong></span><span class="sxs-lookup"><span data-stu-id="4a3e9-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4a3e9-439">25</span><span class="sxs-lookup"><span data-stu-id="4a3e9-439">25</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-440">Возвращает таблицы, в которых все просмотренные таблицы, определенные в каталоге и принадлежащие определенному пользователю, зависят от них.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="4a3e9-441">(Набор строк ВИЕВ_ТАБЛЕ_УСАЖЕ)</span><span class="sxs-lookup"><span data-stu-id="4a3e9-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4a3e9-442">ВИЕВ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="4a3e9-443">ВИЕВ_СЧЕМА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="4a3e9-444">ВИЕВ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4a3e9-445">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="4a3e9-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="4a3e9-446">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="4a3e9-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a3e9-447">Константа</span><span class="sxs-lookup"><span data-stu-id="4a3e9-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-448">Адоенумс. Schema. ASSERTs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-449">Адоенумс. Schema. CATALOGs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-450">Адоенумс. Schema. ЧАРАКТЕРСЕТС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-451">Адоенумс. Schema. ЧЕКККОНСТРАИНТС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-452">Адоенумс. Schema. Collation</span><span class="sxs-lookup"><span data-stu-id="4a3e9-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-453">Адоенумс. Schema. КОЛУМНПРИВИЛЕЖЕС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-454">Адоенумс. Schema. COLUMNs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-455">Адоенумс. Schema. КОЛУМНСДОМАИНУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-456">Адоенумс. Schema. КОНСТРАИНТКОЛУМНУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-457">Адоенумс. Schema. КОНСТРАИНТТАБЛЕУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-458">Адоенумс. Schema. CUBEs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-459">Адоенумс. Schema. ДБИНФОКЭЙВОРДС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-460">Адоенумс. Schema. ДБИНФОЛИТЕРАЛС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-461">Адоенумс. Schema. DIMENSIONs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-462">Адоенумс. Schema. ФОРЕИГНКЭЙС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-463">Адоенумс. Schema. ИЕРАРХИИ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-464">Адоенумс. Schema. INDEXES</span><span class="sxs-lookup"><span data-stu-id="4a3e9-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-465">Адоенумс. Schema. КЭЙКОЛУМНУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-466">Адоенумс. Schema. LEVELs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-467">Адоенумс. Schema. MEASUREs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-468">Адоенумс. Schema. MEMBERs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-469">Адоенумс. Schema. ПРИМАРИКЭЙС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-470">Адоенумс. Schema. ПРОЦЕДУРЕКОЛУМНС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-471">Адоенумс. Schema. ПРОЦЕДУРЕПАРАМЕТЕРС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-472">Адоенумс. Schema. процедуры</span><span class="sxs-lookup"><span data-stu-id="4a3e9-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-473">Адоенумс. Schema. PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4a3e9-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-474">Адоенумс. Schema. ПРОВИДЕРСПЕЦИФИК</span><span class="sxs-lookup"><span data-stu-id="4a3e9-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-475">Адоенумс. Schema. ПРОВИДЕРТИПЕС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-476">Адоенумс. Schema. РЕФЕРЕНТИАЛКОНТРАИНТС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-477">Адоенумс. Schema. СЧЕМАТА</span><span class="sxs-lookup"><span data-stu-id="4a3e9-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-478">Адоенумс. Schema. СКЛЛАНГУАЖЕС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-479">Адоенумс. Schema. STATISTICS</span><span class="sxs-lookup"><span data-stu-id="4a3e9-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-480">Адоенумс. Schema. ТАБЛЕКОНСТРАИНТС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-481">Адоенумс. Schema. ТАБЛЕПРИВИЛЕЖЕС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-482">Адоенумс. Schema. TABLEs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-483">Адоенумс. Schema. translation</span><span class="sxs-lookup"><span data-stu-id="4a3e9-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-484">Адоенумс. Schema. ДОВЕРЕНные лица</span><span class="sxs-lookup"><span data-stu-id="4a3e9-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-485">Адоенумс. Schema. УСАЖЕПРИВИЛЕЖЕС</span><span class="sxs-lookup"><span data-stu-id="4a3e9-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-486">Адоенумс. Schema. ВИЕВКОЛУМНУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a3e9-487">Адоенумс. Schema. VIEWs</span><span class="sxs-lookup"><span data-stu-id="4a3e9-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a3e9-488">Адоенумс. Schema. ВИЕВТАБЛЕУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="4a3e9-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

