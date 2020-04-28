---
title: Индекс динамических свойств ADO
TOCTitle: ADO dynamic property index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bfe788923d623300edac28f0f27534b3ffd8b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283403"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="35db4-102">Индекс динамических свойств ADO</span><span class="sxs-lookup"><span data-stu-id="35db4-102">ADO dynamic property index</span></span>

<span data-ttu-id="35db4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35db4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35db4-104">Поставщики данных, поставщики услуг и компоненты служб могут добавлять динамические свойства в коллекции **свойств** неоткрытого [подключения](connection-object-ado.md) и объектов [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="35db4-104">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="35db4-105">Заданный поставщик может также вставлять дополнительные свойства при открытии этих объектов.</span><span class="sxs-lookup"><span data-stu-id="35db4-105">A given provider may also insert additional properties when these objects are opened.</span></span> <span data-ttu-id="35db4-106">Некоторые из этих свойств перечислены в разделе [динамические свойства ADO](ado-dynamic-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="35db4-106">Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section.</span></span> <span data-ttu-id="35db4-107">Дополнительные сведения приведены в разделе конкретные поставщики в разделе [приложение A: поставщики](appendix-a-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="35db4-107">More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="35db4-108">Приведенная ниже таблица является перекрестным индексом имен ADO и OLE DB для каждого стандартного динамического свойства поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="35db4-108">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span> <span data-ttu-id="35db4-109">Поставщики могут добавлять больше свойств, чем указано здесь.</span><span class="sxs-lookup"><span data-stu-id="35db4-109">Your providers may add more properties than listed here.</span></span> <span data-ttu-id="35db4-110">Конкретные сведения о динамических свойствах, связанных с поставщиками, можно найти в документации по поставщику.</span><span class="sxs-lookup"><span data-stu-id="35db4-110">For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="35db4-111">Справочник программиста OLE DB ссылается на имя свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="35db4-111">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="35db4-112">Дополнительные сведения об этих стандартных свойствах можно найти в справочнике программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="35db4-112">You can find more information about these standard properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="35db4-113">Найдите имя свойства OLE DB в индексе или ознакомьтесь со следующими разделами:</span><span class="sxs-lookup"><span data-stu-id="35db4-113">Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="35db4-114">Приложение C: свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="35db4-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="35db4-115">Поддерживаемые свойства службы курсора</span><span class="sxs-lookup"><span data-stu-id="35db4-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="35db4-116">Поддерживаемые свойства поставщика сохраняемости</span><span class="sxs-lookup"><span data-stu-id="35db4-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="35db4-117">Поддерживаемые свойства OLE DB поставщика удаленного взаимодействия</span><span class="sxs-lookup"><span data-stu-id="35db4-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="35db4-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="35db4-118">Remarks</span></span>

<span data-ttu-id="35db4-119">Номера заметок, используемые в перекрестном индексе:</span><span class="sxs-lookup"><span data-stu-id="35db4-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="35db4-120">(1) это свойство является логическим флагом, указывающим, следует ли использовать именованный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="35db4-120">(1) This property is a Boolean flag indicating whether the named interface should be used.</span></span> <span data-ttu-id="35db4-121">Эквивалентное имя свойства OLE DB указано, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="35db4-121">The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="35db4-122">(2) свойство ADO "Bookmarkd" создается внутренне для обратной совместимости и сопоставляется со свойством OLE DB, ДБПРОП\_ировсетлокате.</span><span class="sxs-lookup"><span data-stu-id="35db4-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="35db4-123">Это то же свойство, которое соответствует свойству ADO, Ировсетлокате.</span><span class="sxs-lookup"><span data-stu-id="35db4-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="35db4-124">(3) имя свойства ADO, "Hidden Columns", называется иначе, чем описание имени свойства OLE DB, "число скрытых столбцов".</span><span class="sxs-lookup"><span data-stu-id="35db4-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="35db4-125">(4) для иерархических наборов записей свойство ADO "Maximum Rows" применяется ко всем дочерним элементам.</span><span class="sxs-lookup"><span data-stu-id="35db4-125">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children.</span></span> <span data-ttu-id="35db4-126">В зависимости от порядка, в котором возвращаются строки, могут иметься все, некоторые или не дочерние элементы для каждого родительского или потерянного дочерних элементов в наборе результатов.</span><span class="sxs-lookup"><span data-stu-id="35db4-126">Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set.</span></span> <span data-ttu-id="35db4-127">Таким образом, при изменении формы иерархических наборов записей идентификаторы для каждого потомка должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="35db4-127">Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique.</span></span> <span data-ttu-id="35db4-128">Как правило, поставщик [службы формирования данных Майкрософт для OLE DB (мсдаташапе)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) не позволяет различать свойства, которые могут быть унаследованы от родительского элемента, и те, которые не могут быть унаследованы.</span><span class="sxs-lookup"><span data-stu-id="35db4-128">In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="35db4-129">(5) не применяется.</span><span class="sxs-lookup"><span data-stu-id="35db4-129">(5) Does not apply.</span></span>

<span data-ttu-id="35db4-130">**Динамические свойства подключения**</span><span class="sxs-lookup"><span data-stu-id="35db4-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35db4-131">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="35db4-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="35db4-132">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="35db4-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35db4-133">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="35db4-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="35db4-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="35db4-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-135">Асинчабле Abort</span><span class="sxs-lookup"><span data-stu-id="35db4-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="35db4-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="35db4-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-137">Фиксация асинчабле</span><span class="sxs-lookup"><span data-stu-id="35db4-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="35db4-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="35db4-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-139">Уровни изоляции для автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="35db4-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="35db4-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="35db4-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-141">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="35db4-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="35db4-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="35db4-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-143">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="35db4-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="35db4-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="35db4-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-145">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="35db4-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="35db4-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="35db4-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-147">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="35db4-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="35db4-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="35db4-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-149">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="35db4-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="35db4-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="35db4-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-151">Источник данных</span><span class="sxs-lookup"><span data-stu-id="35db4-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="35db4-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="35db4-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-153">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="35db4-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="35db4-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="35db4-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-155">Модель потоков объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="35db4-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="35db4-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="35db4-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-157">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="35db4-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="35db4-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="35db4-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-159">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="35db4-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="35db4-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="35db4-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-161">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="35db4-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="35db4-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="35db4-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-163">ГРУППИРОВКа по поддержке</span><span class="sxs-lookup"><span data-stu-id="35db4-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="35db4-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="35db4-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-165">Поддержка гетерогенных таблиц</span><span class="sxs-lookup"><span data-stu-id="35db4-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="35db4-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="35db4-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-167">Чувствительность к регистру идентификаторов</span><span class="sxs-lookup"><span data-stu-id="35db4-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="35db4-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="35db4-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-169">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="35db4-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="35db4-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35db4-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-171">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="35db4-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="35db4-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="35db4-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-173">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="35db4-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="35db4-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="35db4-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-175">Идентификатор языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="35db4-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="35db4-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="35db4-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-177">Расположение</span><span class="sxs-lookup"><span data-stu-id="35db4-177">Location</span></span></p></td>
<td><p><span data-ttu-id="35db4-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="35db4-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-179">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="35db4-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="35db4-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="35db4-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-181">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="35db4-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="35db4-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="35db4-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-183">Максимальный размер строки включает большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="35db4-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="35db4-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="35db4-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-185">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="35db4-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="35db4-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="35db4-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-187">Режим</span><span class="sxs-lookup"><span data-stu-id="35db4-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="35db4-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="35db4-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-189">Наборы параметров с несколькими параметрами</span><span class="sxs-lookup"><span data-stu-id="35db4-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="35db4-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="35db4-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-191">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="35db4-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="35db4-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="35db4-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-193">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="35db4-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="35db4-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="35db4-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-195">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="35db4-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="35db4-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="35db4-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-197">Порядок сортировки NULL</span><span class="sxs-lookup"><span data-stu-id="35db4-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="35db4-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="35db4-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-199">Поведение сцепления со значением NULL</span><span class="sxs-lookup"><span data-stu-id="35db4-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="35db4-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="35db4-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-201">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="35db4-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="35db4-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="35db4-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-203">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="35db4-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="35db4-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="35db4-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-205">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="35db4-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="35db4-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="35db4-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-207">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="35db4-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="35db4-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="35db4-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-209">УПОРЯДОЧЕНие по столбцам в списке выборки</span><span class="sxs-lookup"><span data-stu-id="35db4-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="35db4-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="35db4-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-211">Доступность выходного параметра</span><span class="sxs-lookup"><span data-stu-id="35db4-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="35db4-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="35db4-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-213">Передача по параметрам доступа ref</span><span class="sxs-lookup"><span data-stu-id="35db4-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="35db4-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="35db4-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-215">Password</span><span class="sxs-lookup"><span data-stu-id="35db4-215">Password</span></span></p></td>
<td><p><span data-ttu-id="35db4-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="35db4-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-217">Сохранение сведений о безопасности</span><span class="sxs-lookup"><span data-stu-id="35db4-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="35db4-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="35db4-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-219">Тип постоянного идентификатора</span><span class="sxs-lookup"><span data-stu-id="35db4-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="35db4-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="35db4-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-221">Действие по подготовке к прерыванию</span><span class="sxs-lookup"><span data-stu-id="35db4-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="35db4-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="35db4-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-223">Подготовка режима фиксации</span><span class="sxs-lookup"><span data-stu-id="35db4-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="35db4-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="35db4-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-225">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="35db4-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="35db4-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="35db4-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="35db4-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="35db4-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="35db4-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-229">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="35db4-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="35db4-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="35db4-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-231">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="35db4-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="35db4-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="35db4-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-233">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="35db4-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="35db4-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="35db4-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-235">Источник данных, предназначенный только для чтения</span><span class="sxs-lookup"><span data-stu-id="35db4-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="35db4-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="35db4-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-237">Преобразования наборов строк для команды</span><span class="sxs-lookup"><span data-stu-id="35db4-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="35db4-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="35db4-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-239">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="35db4-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="35db4-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="35db4-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-241">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="35db4-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="35db4-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="35db4-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-243">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="35db4-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="35db4-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="35db4-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-245">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="35db4-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="35db4-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="35db4-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-247">Поддержка вложенных запросов</span><span class="sxs-lookup"><span data-stu-id="35db4-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="35db4-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="35db4-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-249">Табличный термин</span><span class="sxs-lookup"><span data-stu-id="35db4-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="35db4-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="35db4-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-251">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="35db4-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="35db4-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="35db4-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-253">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="35db4-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="35db4-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="35db4-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-255">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="35db4-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="35db4-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="35db4-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-257">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="35db4-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="35db4-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="35db4-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="35db4-259">**Динамические свойства Recordset**</span><span class="sxs-lookup"><span data-stu-id="35db4-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="35db4-260">Обратите внимание, что **динамические свойства** объекта **Recordset** выходят из области действия (становятся недоступными) при закрытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="35db4-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35db4-261">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="35db4-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="35db4-262">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="35db4-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35db4-263">иакцессор</span><span class="sxs-lookup"><span data-stu-id="35db4-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="35db4-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-265">ичаптередровсет</span><span class="sxs-lookup"><span data-stu-id="35db4-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="35db4-266">1,1</span><span class="sxs-lookup"><span data-stu-id="35db4-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-267">иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="35db4-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="35db4-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-269">иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="35db4-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="35db4-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-271">иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="35db4-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="35db4-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-273">иконверттипе</span><span class="sxs-lookup"><span data-stu-id="35db4-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="35db4-274">1,1</span><span class="sxs-lookup"><span data-stu-id="35db4-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="35db4-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="35db4-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="35db4-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="35db4-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-279">идбасинчстатус</span><span class="sxs-lookup"><span data-stu-id="35db4-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="35db4-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-281">ипарентровсет</span><span class="sxs-lookup"><span data-stu-id="35db4-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="35db4-282">1,1</span><span class="sxs-lookup"><span data-stu-id="35db4-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-283">ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="35db4-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="35db4-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-285">ировсетексактскролл</span><span class="sxs-lookup"><span data-stu-id="35db4-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="35db4-286">1,1</span><span class="sxs-lookup"><span data-stu-id="35db4-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-287">ировсетфинд</span><span class="sxs-lookup"><span data-stu-id="35db4-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="35db4-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-289">ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="35db4-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="35db4-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-291">ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="35db4-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="35db4-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-293">ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="35db4-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="35db4-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-295">ировсетрефреш</span><span class="sxs-lookup"><span data-stu-id="35db4-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="35db4-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-297">ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="35db4-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="35db4-298">1,1</span><span class="sxs-lookup"><span data-stu-id="35db4-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-299">ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="35db4-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="35db4-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-301">ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="35db4-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="35db4-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-303">ировсетвиев</span><span class="sxs-lookup"><span data-stu-id="35db4-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="35db4-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-305">ировсетиндекс</span><span class="sxs-lookup"><span data-stu-id="35db4-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="35db4-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-307">исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="35db4-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="35db4-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-309">Содержим</span><span class="sxs-lookup"><span data-stu-id="35db4-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="35db4-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-311">IStream</span><span class="sxs-lookup"><span data-stu-id="35db4-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="35db4-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-313">исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="35db4-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="35db4-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="35db4-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-315">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="35db4-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="35db4-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="35db4-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-317">Набор строк только для добавления</span><span class="sxs-lookup"><span data-stu-id="35db4-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="35db4-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="35db4-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-319">Асинхронная обработка наборов строк</span><span class="sxs-lookup"><span data-stu-id="35db4-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="35db4-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="35db4-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-321">Автоматическое перерасчет</span><span class="sxs-lookup"><span data-stu-id="35db4-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="35db4-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="35db4-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-323">Размер фоновой загрузки</span><span class="sxs-lookup"><span data-stu-id="35db4-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="35db4-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="35db4-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-325">Приоритет фонового потока</span><span class="sxs-lookup"><span data-stu-id="35db4-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="35db4-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="35db4-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-327">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="35db4-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="35db4-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="35db4-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-329">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="35db4-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="35db4-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="35db4-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-331">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="35db4-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="35db4-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="35db4-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="35db4-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="35db4-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="35db4-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-335">Упорядоченные закладки</span><span class="sxs-lookup"><span data-stu-id="35db4-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="35db4-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="35db4-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-337">Дочерние строки кэша</span><span class="sxs-lookup"><span data-stu-id="35db4-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="35db4-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-339">Кэширование отложенных столбцов</span><span class="sxs-lookup"><span data-stu-id="35db4-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="35db4-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="35db4-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-341">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="35db4-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="35db4-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-343">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="35db4-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="35db4-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="35db4-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-345">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="35db4-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="35db4-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-347">Столбец доступен для записи</span><span class="sxs-lookup"><span data-stu-id="35db4-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="35db4-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="35db4-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-349">Время ожидания команды</span><span class="sxs-lookup"><span data-stu-id="35db4-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="35db4-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="35db4-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-351">Версия обработчика курсора</span><span class="sxs-lookup"><span data-stu-id="35db4-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="35db4-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="35db4-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-353">Откладывание столбца</span><span class="sxs-lookup"><span data-stu-id="35db4-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="35db4-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="35db4-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-355">Откладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="35db4-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="35db4-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="35db4-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-357">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="35db4-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="35db4-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="35db4-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-359">Операции фильтра</span><span class="sxs-lookup"><span data-stu-id="35db4-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="35db4-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="35db4-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-361">Операции поиска</span><span class="sxs-lookup"><span data-stu-id="35db4-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="35db4-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="35db4-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-363">Скрытые столбцы (количество)</span><span class="sxs-lookup"><span data-stu-id="35db4-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="35db4-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="35db4-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-365">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="35db4-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="35db4-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-367">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="35db4-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="35db4-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-369">Размер начальной извлечения</span><span class="sxs-lookup"><span data-stu-id="35db4-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="35db4-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="35db4-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-371">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="35db4-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="35db4-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="35db4-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-373">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="35db4-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="35db4-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="35db4-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-375">Ведение состояния изменения</span><span class="sxs-lookup"><span data-stu-id="35db4-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="35db4-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="35db4-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-377">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="35db4-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="35db4-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-379">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="35db4-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="35db4-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-381">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="35db4-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="35db4-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-383">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="35db4-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="35db4-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="35db4-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-385">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="35db4-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="35db4-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="35db4-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-387">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="35db4-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="35db4-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="35db4-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-389">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="35db4-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="35db4-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="35db4-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-391">Видны другие изменения</span><span class="sxs-lookup"><span data-stu-id="35db4-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="35db4-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="35db4-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-393">Видимые вставки других пользователей</span><span class="sxs-lookup"><span data-stu-id="35db4-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="35db4-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="35db4-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-395">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="35db4-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="35db4-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="35db4-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-397">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="35db4-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="35db4-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="35db4-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-399">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="35db4-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="35db4-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="35db4-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-401">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="35db4-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="35db4-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="35db4-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-403">Private1</span><span class="sxs-lookup"><span data-stu-id="35db4-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="35db4-404">17:00</span><span class="sxs-lookup"><span data-stu-id="35db4-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-405">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="35db4-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="35db4-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="35db4-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-407">Повторные события</span><span class="sxs-lookup"><span data-stu-id="35db4-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="35db4-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="35db4-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-409">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="35db4-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="35db4-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-411">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="35db4-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="35db4-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="35db4-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-413">Изменение имени фигуры</span><span class="sxs-lookup"><span data-stu-id="35db4-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="35db4-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="35db4-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-415">Команда Resync</span><span class="sxs-lookup"><span data-stu-id="35db4-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="35db4-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="35db4-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-417">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="35db4-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="35db4-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="35db4-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-419">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="35db4-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="35db4-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-421">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="35db4-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="35db4-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-423">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="35db4-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="35db4-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-425">Права на строки</span><span class="sxs-lookup"><span data-stu-id="35db4-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="35db4-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="35db4-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-427">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="35db4-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="35db4-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-429">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="35db4-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="35db4-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="35db4-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-431">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="35db4-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="35db4-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-433">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="35db4-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="35db4-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-435">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="35db4-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="35db4-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-437">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="35db4-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="35db4-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-439">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="35db4-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="35db4-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-441">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="35db4-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="35db4-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="35db4-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-443">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="35db4-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="35db4-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="35db4-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-445">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="35db4-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="35db4-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="35db4-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-447">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="35db4-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="35db4-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="35db4-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-449">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="35db4-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="35db4-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="35db4-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-451">Уникальный каталог</span><span class="sxs-lookup"><span data-stu-id="35db4-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="35db4-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="35db4-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-453">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="35db4-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="35db4-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="35db4-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-455">Уникальная схема</span><span class="sxs-lookup"><span data-stu-id="35db4-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="35db4-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="35db4-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-457">Уникальная таблица</span><span class="sxs-lookup"><span data-stu-id="35db4-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="35db4-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="35db4-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-459">Обновление</span><span class="sxs-lookup"><span data-stu-id="35db4-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="35db4-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="35db4-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-461">Условия обновления</span><span class="sxs-lookup"><span data-stu-id="35db4-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="35db4-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="35db4-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35db4-463">Повторная синхронизация обновлений</span><span class="sxs-lookup"><span data-stu-id="35db4-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="35db4-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="35db4-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35db4-465">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="35db4-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="35db4-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="35db4-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

