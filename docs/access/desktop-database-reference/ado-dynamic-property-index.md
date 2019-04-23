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
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="6c269-102">Индекс динамических свойств ADO</span><span class="sxs-lookup"><span data-stu-id="6c269-102">ADO dynamic property index</span></span>

<span data-ttu-id="6c269-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c269-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c269-104">Поставщики данных, поставщики услуг и компоненты служб могут добавлять динамические свойства в коллекции **свойств** неоткрытого [подключения](connection-object-ado.md) и объектов [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6c269-104">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="6c269-105">Заданный поставщик может также вставлять дополнительные свойства при открытии этих объектов.</span><span class="sxs-lookup"><span data-stu-id="6c269-105">A given provider may also insert additional properties when these objects are opened.</span></span> <span data-ttu-id="6c269-106">Некоторые из этих свойств перечислены в разделе [динамические свойства ADO](ado-dynamic-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="6c269-106">Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section.</span></span> <span data-ttu-id="6c269-107">Дополнительные сведения приведены в разделе конкретные поставщики в разделе [приложение A: поставщики](appendix-a-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="6c269-107">More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="6c269-108">Приведенная ниже таблица является перекрестным индексом имен ADO и OLE DB для каждого стандартного динамического свойства поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6c269-108">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span> <span data-ttu-id="6c269-109">Поставщики могут добавлять больше свойств, чем указано здесь.</span><span class="sxs-lookup"><span data-stu-id="6c269-109">Your providers may add more properties than listed here.</span></span> <span data-ttu-id="6c269-110">Конкретные сведения о динамических свойствах, связанных с поставщиками, можно найти в документации по поставщику.</span><span class="sxs-lookup"><span data-stu-id="6c269-110">For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="6c269-111">Справочник программиста OLE DB ссылается на имя свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="6c269-111">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="6c269-112">Дополнительные сведения об этих стандартных свойствах можно найти в справочнике программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6c269-112">You can find more information about these standard properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="6c269-113">Найдите имя свойства OLE DB в индексе или ознакомьтесь со следующими разделами:</span><span class="sxs-lookup"><span data-stu-id="6c269-113">Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="6c269-114">Приложение C: свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6c269-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="6c269-115">Поддерживаемые свойства службы курсора</span><span class="sxs-lookup"><span data-stu-id="6c269-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="6c269-116">Поддерживаемые свойства поставщика сохраняемости</span><span class="sxs-lookup"><span data-stu-id="6c269-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="6c269-117">Поддерживаемые свойства OLE DB поставщика удаленного взаимодействия</span><span class="sxs-lookup"><span data-stu-id="6c269-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="6c269-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="6c269-118">Remarks</span></span>

<span data-ttu-id="6c269-119">Номера заМеток, используемые в перекрестном индексе:</span><span class="sxs-lookup"><span data-stu-id="6c269-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="6c269-120">(1) это свойство является логическим флагом, указывающим, следует ли использовать именованный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6c269-120">(1) This property is a Boolean flag indicating whether the named interface should be used.</span></span> <span data-ttu-id="6c269-121">Эквивалентное имя свойства OLE DB указано, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="6c269-121">The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="6c269-122">(2) свойство ADO "Bookmarkd" создается внутренне для обратной совместимости и сопоставляется со свойством OLE DB, ДБПРОП\_ировсетлокате.</span><span class="sxs-lookup"><span data-stu-id="6c269-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="6c269-123">Это то же свойство, которое соответствует свойству ADO, Ировсетлокате.</span><span class="sxs-lookup"><span data-stu-id="6c269-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="6c269-124">(3) имя свойства ADO, "Hidden Columns", называется иначе, чем описание имени свойства OLE DB, "число скрытых столбцов".</span><span class="sxs-lookup"><span data-stu-id="6c269-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="6c269-125">(4) для иерархических наборов записей свойство ADO "Maximum Rows" применяется ко всем дочерним элементам.</span><span class="sxs-lookup"><span data-stu-id="6c269-125">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children.</span></span> <span data-ttu-id="6c269-126">В зависимости от порядка, в котором возвращаются строки, могут иметься все, некоторые или не дочерние элементы для каждого родительского или потерянного дочерних элементов в наборе результатов.</span><span class="sxs-lookup"><span data-stu-id="6c269-126">Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set.</span></span> <span data-ttu-id="6c269-127">Таким образом, при изменении формы иерархических наборов записей идентификаторы для каждого потомка должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="6c269-127">Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique.</span></span> <span data-ttu-id="6c269-128">Как правило, поставщик [службы формирования данных Майкрософт для OLE DB (мсдаташапе)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) не позволяет различать свойства, которые могут быть унаследованы от родительского элемента, и те, которые не могут быть унаследованы.</span><span class="sxs-lookup"><span data-stu-id="6c269-128">In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="6c269-129">(5) не применяется.</span><span class="sxs-lookup"><span data-stu-id="6c269-129">(5) Does not apply.</span></span>

<span data-ttu-id="6c269-130">**Динамические свойства подключения**</span><span class="sxs-lookup"><span data-stu-id="6c269-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c269-131">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="6c269-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6c269-132">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6c269-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c269-133">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="6c269-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="6c269-134">ДБПРОП_АКТИВЕСЕССИОНС</span><span class="sxs-lookup"><span data-stu-id="6c269-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-135">Асинчабле Abort</span><span class="sxs-lookup"><span data-stu-id="6c269-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="6c269-136">ДБПРОП_АСИНКТКСНАБОРТ</span><span class="sxs-lookup"><span data-stu-id="6c269-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-137">Фиксация Асинчабле</span><span class="sxs-lookup"><span data-stu-id="6c269-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="6c269-138">ДБПРОП_АСИНКТНКСКОММИТ</span><span class="sxs-lookup"><span data-stu-id="6c269-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-139">Уровни изоляции для автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="6c269-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="6c269-140">ДБПРОП_СЕСС_АУТОКОММИТИСОЛЕВЕЛС</span><span class="sxs-lookup"><span data-stu-id="6c269-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-141">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="6c269-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="6c269-142">ДБПРОП_КАТАЛОГЛОКАТИОН</span><span class="sxs-lookup"><span data-stu-id="6c269-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-143">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="6c269-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="6c269-144">ДБПРОП_КАТАЛОГТЕРМ</span><span class="sxs-lookup"><span data-stu-id="6c269-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-145">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="6c269-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="6c269-146">ДБПРОП_КОЛУМНДЕФИНИТИОН</span><span class="sxs-lookup"><span data-stu-id="6c269-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-147">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="6c269-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="6c269-148">ДБПРОП_ИНИТ_ТИМЕАУТ</span><span class="sxs-lookup"><span data-stu-id="6c269-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-149">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="6c269-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="6c269-150">ДБПРОП_КУРРЕНТКАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="6c269-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-151">Источник данных</span><span class="sxs-lookup"><span data-stu-id="6c269-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="6c269-152">ДБПРОП_ИНИТ_ДАТАСАУРЦЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-153">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="6c269-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="6c269-154">ДБПРОП_ДАТАСАУРЦЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-155">Модель потоков объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="6c269-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6c269-156">ДБПРОП_ДСОСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="6c269-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-157">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="6c269-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="6c269-158">ДБПРОП_ДБМСНАМЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-159">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="6c269-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="6c269-160">ДБПРОП_ДБМСВЕР</span><span class="sxs-lookup"><span data-stu-id="6c269-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-161">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="6c269-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="6c269-162">ДБПРОП_ИНИТ_ПРОВИДЕРСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="6c269-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-163">ГРУППИРОВКа по поддержке</span><span class="sxs-lookup"><span data-stu-id="6c269-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="6c269-164">ДБПРОП_ГРАУПБИ</span><span class="sxs-lookup"><span data-stu-id="6c269-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-165">Поддержка гетерогенных таблиц</span><span class="sxs-lookup"><span data-stu-id="6c269-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="6c269-166">ДБПРОП_ХЕТЕРОЖЕНЕАУСТАБЛЕС</span><span class="sxs-lookup"><span data-stu-id="6c269-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-167">Чувствительность к регистру идентификаторов</span><span class="sxs-lookup"><span data-stu-id="6c269-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="6c269-168">ДБПРОП_ИДЕНТИФИЕРКАСЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-169">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="6c269-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="6c269-170">ДБПРОП_ИНИТ_КАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="6c269-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-171">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="6c269-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="6c269-172">ДБПРОП_СУППОРТЕДТКСНИСОЛЕВЕЛС</span><span class="sxs-lookup"><span data-stu-id="6c269-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-173">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="6c269-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="6c269-174">ДБПРОП_СУППОРТЕДТКСНИСОРЕТАИН</span><span class="sxs-lookup"><span data-stu-id="6c269-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-175">Идентификатор языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="6c269-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="6c269-176">ДБПРОП_ИНИТ_ЛЦИД</span><span class="sxs-lookup"><span data-stu-id="6c269-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-177">Расположение</span><span class="sxs-lookup"><span data-stu-id="6c269-177">Location</span></span></p></td>
<td><p><span data-ttu-id="6c269-178">ДБПРОП_ИНИТ_ЛОКАТИОН</span><span class="sxs-lookup"><span data-stu-id="6c269-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-179">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="6c269-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="6c269-180">ДБПРОП_МАКСИНДЕКССИЗЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-181">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="6c269-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="6c269-182">ДБПРОП_МАКСРОВСИЗЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-183">Максимальный размер строки включает большой ДВОИЧный объект</span><span class="sxs-lookup"><span data-stu-id="6c269-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="6c269-184">ДБПРОП_МАКСРОВСИЗЕИНКЛУДЕСБЛОБ</span><span class="sxs-lookup"><span data-stu-id="6c269-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-185">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="6c269-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="6c269-186">ДБПРОП_МАКСТАБЛЕСИНСЕЛЕКТ</span><span class="sxs-lookup"><span data-stu-id="6c269-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-187">Режим</span><span class="sxs-lookup"><span data-stu-id="6c269-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="6c269-188">ДБПРОП_ИНИТ_МОДЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-189">Наборы параметров с несколькими параметрами</span><span class="sxs-lookup"><span data-stu-id="6c269-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="6c269-190">ДБПРОП_МУЛТИПЛЕПАРАМСЕТС</span><span class="sxs-lookup"><span data-stu-id="6c269-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-191">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="6c269-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="6c269-192">ДБПРОП_МУЛТИПЛЕРЕСУЛТС</span><span class="sxs-lookup"><span data-stu-id="6c269-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-193">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="6c269-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6c269-194">ДБПРОП_МУЛТИПЛЕСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="6c269-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-195">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="6c269-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="6c269-196">ДБПРОП_МУЛТИТАБЛЕУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-197">Порядок сортировки NULL</span><span class="sxs-lookup"><span data-stu-id="6c269-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="6c269-198">ДБПРОП_НУЛЛКОЛЛАТИОН</span><span class="sxs-lookup"><span data-stu-id="6c269-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-199">Поведение сцепления со ЗНАЧЕНИЕМ NULL</span><span class="sxs-lookup"><span data-stu-id="6c269-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="6c269-200">ДБПРОП_КОНКАТНУЛЛБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="6c269-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-201">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="6c269-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="6c269-202">ДБПРОП_ИНИТ_ОЛЕДБСЕРВИЦЕС</span><span class="sxs-lookup"><span data-stu-id="6c269-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-203">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="6c269-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="6c269-204">ДБПРОП_ПРОВИДЕРОЛЕДБВЕР</span><span class="sxs-lookup"><span data-stu-id="6c269-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-205">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="6c269-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="6c269-206">ДБПРОП_ОЛЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="6c269-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-207">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="6c269-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="6c269-208">ДБПРОП_ОПЕНРОВСЕТСУППОРТ</span><span class="sxs-lookup"><span data-stu-id="6c269-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-209">УПОРЯДОЧЕНие по столбцам в списке выборки</span><span class="sxs-lookup"><span data-stu-id="6c269-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="6c269-210">ДБПРОП_ОРДЕРБИКОЛУМНСИНСЕЛЕКТ</span><span class="sxs-lookup"><span data-stu-id="6c269-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-211">Доступность выходного параметра</span><span class="sxs-lookup"><span data-stu-id="6c269-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="6c269-212">ДБПРОП_АУТПУТПАРАМЕТЕРАВАИЛАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="6c269-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-213">Передача по параметрам доступа ref</span><span class="sxs-lookup"><span data-stu-id="6c269-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="6c269-214">ДБПРОП_БИРЕФАКЦЕССОРС</span><span class="sxs-lookup"><span data-stu-id="6c269-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-215">Пароль</span><span class="sxs-lookup"><span data-stu-id="6c269-215">Password</span></span></p></td>
<td><p><span data-ttu-id="6c269-216">ДБПРОП_АУС_ПАССВОРД</span><span class="sxs-lookup"><span data-stu-id="6c269-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-217">Сохранение сведений о безопасности</span><span class="sxs-lookup"><span data-stu-id="6c269-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="6c269-218">ДБПРОП_АУС_ПЕРСИСТ_СЕНСИТИВЕ_АУСИНФО</span><span class="sxs-lookup"><span data-stu-id="6c269-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-219">Тип постоянного идентификатора</span><span class="sxs-lookup"><span data-stu-id="6c269-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="6c269-220">ДБПРОП_ПЕРСИСТЕНТИДТИПЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-221">Действие по подготовке к прерыванию</span><span class="sxs-lookup"><span data-stu-id="6c269-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="6c269-222">ДБПРОП_ПРЕПАРЕАБОРТБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="6c269-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-223">Подготовка режима фиксации</span><span class="sxs-lookup"><span data-stu-id="6c269-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="6c269-224">ДБПРОП_ПРЕПАРЕКОММИТБЕХАВИОР</span><span class="sxs-lookup"><span data-stu-id="6c269-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-225">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="6c269-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="6c269-226">ДБПРОП_ПРОЦЕДУРЕТЕРМ</span><span class="sxs-lookup"><span data-stu-id="6c269-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="6c269-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="6c269-228">ДБПРОП_ИНИТ_ПРОМПТ</span><span class="sxs-lookup"><span data-stu-id="6c269-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-229">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="6c269-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="6c269-230">ДБПРОП_ПРОВИДЕРФРИЕНДЛИНАМЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-231">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="6c269-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="6c269-232">ДБПРОП_ПРОВИДЕРФИЛЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-233">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="6c269-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="6c269-234">ДБПРОП_ПРОВИДЕРВЕР</span><span class="sxs-lookup"><span data-stu-id="6c269-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-235">Источник данных, предназначенный только для чтения</span><span class="sxs-lookup"><span data-stu-id="6c269-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="6c269-236">ДБПРОП_ДАТАСАУРЦЕРЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="6c269-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-237">Преобразования наборов строк для команды</span><span class="sxs-lookup"><span data-stu-id="6c269-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="6c269-238">ДБПРОП_РОВСЕТКОНВЕРСИОНСОНКОММАНД</span><span class="sxs-lookup"><span data-stu-id="6c269-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-239">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="6c269-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="6c269-240">ДБПРОП_СЧЕМАТЕРМ</span><span class="sxs-lookup"><span data-stu-id="6c269-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-241">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="6c269-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="6c269-242">ДБПРОП_СЧЕМАУСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-243">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="6c269-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="6c269-244">ДБПРОП_СКЛСУППОРТ</span><span class="sxs-lookup"><span data-stu-id="6c269-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-245">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="6c269-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="6c269-246">ДБПРОП_СТРУКТУРЕДСТОРАЖЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-247">Поддержка вложенных запросов</span><span class="sxs-lookup"><span data-stu-id="6c269-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="6c269-248">ДБПРОП_СУБКУЕРИЕС</span><span class="sxs-lookup"><span data-stu-id="6c269-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-249">Табличный термин</span><span class="sxs-lookup"><span data-stu-id="6c269-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="6c269-250">ДБПРОП_ТАБЛЕТЕРМ</span><span class="sxs-lookup"><span data-stu-id="6c269-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-251">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="6c269-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="6c269-252">ДБПРОП_СУППОРТЕДТКСНДДЛ</span><span class="sxs-lookup"><span data-stu-id="6c269-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-253">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="6c269-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="6c269-254">ДБПРОП_АУС_УСЕРИД</span><span class="sxs-lookup"><span data-stu-id="6c269-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-255">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="6c269-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="6c269-256">ДБПРОП_УСЕРНАМЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-257">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="6c269-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="6c269-258">ДБПРОП_ИНИТ_ХВНД</span><span class="sxs-lookup"><span data-stu-id="6c269-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c269-259">**Динамические свойства Recordset**</span><span class="sxs-lookup"><span data-stu-id="6c269-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="6c269-260">Обратите внимание, что **динамические свойства** объекта **Recordset** выходят из области действия (становятся недоступными) при закрытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6c269-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c269-261">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="6c269-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6c269-262">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6c269-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c269-263">Иакцессор</span><span class="sxs-lookup"><span data-stu-id="6c269-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="6c269-264">ДБПРОП_ИАКЦЕССОР (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-265">Ичаптередровсет</span><span class="sxs-lookup"><span data-stu-id="6c269-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="6c269-266">1,1</span><span class="sxs-lookup"><span data-stu-id="6c269-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-267">Иколумнсинфо</span><span class="sxs-lookup"><span data-stu-id="6c269-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="6c269-268">ДБПРОП_ИКОЛУМНСИНФО (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-269">Иколумнсровсет</span><span class="sxs-lookup"><span data-stu-id="6c269-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="6c269-270">ДБПРОП_ИКОЛУМНСРОВСЕТ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-271">Иконнектионпоинтконтаинер</span><span class="sxs-lookup"><span data-stu-id="6c269-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="6c269-272">ДБПРОП_ИКОННЕКТИОНПОИНТКОНТАИНЕР (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-273">Иконверттипе</span><span class="sxs-lookup"><span data-stu-id="6c269-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="6c269-274">1,1</span><span class="sxs-lookup"><span data-stu-id="6c269-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="6c269-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="6c269-276">ДБПРОП_ИЛОККБИТЕС (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="6c269-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="6c269-278">ДБПРОП_ИРОВСЕТ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-279">Идбасинчстатус</span><span class="sxs-lookup"><span data-stu-id="6c269-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="6c269-280">ДБПРОП_ИДБАСИНЧСТАТУС (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-281">Ипарентровсет</span><span class="sxs-lookup"><span data-stu-id="6c269-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="6c269-282">1,1</span><span class="sxs-lookup"><span data-stu-id="6c269-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-283">Ировсетчанже</span><span class="sxs-lookup"><span data-stu-id="6c269-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="6c269-284">ДБПРОП_ИРОВСЕТЧАНЖЕ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-285">Ировсетексактскролл</span><span class="sxs-lookup"><span data-stu-id="6c269-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="6c269-286">1,1</span><span class="sxs-lookup"><span data-stu-id="6c269-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-287">Ировсетфинд</span><span class="sxs-lookup"><span data-stu-id="6c269-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="6c269-288">ДБПРОП_ИРОВСЕТФИНД (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-289">Ировсетидентити</span><span class="sxs-lookup"><span data-stu-id="6c269-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="6c269-290">ДБПРОП_ИРОВСЕТИДЕНТИТИ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-291">Ировсетинфо</span><span class="sxs-lookup"><span data-stu-id="6c269-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="6c269-292">ДБПРОП_ИРОВСЕТИНФО (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-293">Ировсетлокате</span><span class="sxs-lookup"><span data-stu-id="6c269-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="6c269-294">ДБПРОП_ИРОВСЕТЛОКАТЕ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-295">Ировсетрефреш</span><span class="sxs-lookup"><span data-stu-id="6c269-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="6c269-296">ДБПРОП_ИРОВСЕТРЕФРЕШ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-297">Ировсетресинч</span><span class="sxs-lookup"><span data-stu-id="6c269-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="6c269-298">1,1</span><span class="sxs-lookup"><span data-stu-id="6c269-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-299">Ировсетскролл</span><span class="sxs-lookup"><span data-stu-id="6c269-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="6c269-300">ДБПРОП_ИРОВСЕТСКРОЛЛ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-301">Ировсетупдате</span><span class="sxs-lookup"><span data-stu-id="6c269-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="6c269-302">ДБПРОП_ИРОВСЕТУПДАТЕ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-303">Ировсетвиев</span><span class="sxs-lookup"><span data-stu-id="6c269-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="6c269-304">ДБПРОП_ИРОВСЕТВИЕВ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-305">Ировсетиндекс</span><span class="sxs-lookup"><span data-stu-id="6c269-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="6c269-306">ДБПРОП_ИРОВСЕТИНДЕКС (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-307">Исекуентиалстреам</span><span class="sxs-lookup"><span data-stu-id="6c269-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="6c269-308">ДБПРОП_ИСЕКУЕНТИАЛСТРЕАМ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-309">Содержим</span><span class="sxs-lookup"><span data-stu-id="6c269-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="6c269-310">ДБПРОП_ИСТОРАЖЕ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-311">IStream</span><span class="sxs-lookup"><span data-stu-id="6c269-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="6c269-312">ДБПРОП_ИСТРЕАМ (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-313">Исуппортерроринфо</span><span class="sxs-lookup"><span data-stu-id="6c269-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="6c269-314">ДБПРОП_ИСУППОРТЕРРОРИНФО (1)</span><span class="sxs-lookup"><span data-stu-id="6c269-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-315">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="6c269-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="6c269-316">ДБПРОП_АКЦЕССОРДЕР</span><span class="sxs-lookup"><span data-stu-id="6c269-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-317">Набор строк только для добавления</span><span class="sxs-lookup"><span data-stu-id="6c269-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="6c269-318">ДБПРОП_АППЕНДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="6c269-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-319">Асинхронная обработка наборов строк</span><span class="sxs-lookup"><span data-stu-id="6c269-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="6c269-320">ДБПРОП_РОВСЕТ_АСИНЧ</span><span class="sxs-lookup"><span data-stu-id="6c269-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-321">Автоматическое перерасчет</span><span class="sxs-lookup"><span data-stu-id="6c269-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="6c269-322">ДБПРОП_АДК_АУТОРЕКАЛК</span><span class="sxs-lookup"><span data-stu-id="6c269-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-323">Размер фоновой загрузки</span><span class="sxs-lookup"><span data-stu-id="6c269-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="6c269-324">ДБПРОП_АСИНЧФЕТЧСИЗЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-325">Приоритет фонового потока</span><span class="sxs-lookup"><span data-stu-id="6c269-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="6c269-326">ДБПРОП_АСИНЧСРЕАДПРИОРИТИ</span><span class="sxs-lookup"><span data-stu-id="6c269-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-327">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="6c269-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="6c269-328">ДБПРОП_АДК_БАТЧСИЗЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-329">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="6c269-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6c269-330">ДБПРОП_БЛОККИНГСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="6c269-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-331">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="6c269-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="6c269-332">ДБПРОП_БУКМАРКТИПЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="6c269-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="6c269-334">ДБПРОП_ИРОВСЕТЛОКАТЕ (2)</span><span class="sxs-lookup"><span data-stu-id="6c269-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-335">Упорядоченные закладки</span><span class="sxs-lookup"><span data-stu-id="6c269-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="6c269-336">ДБПРОП_ОРДЕРЕДБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="6c269-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-337">ДоЧерние строки кэша</span><span class="sxs-lookup"><span data-stu-id="6c269-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-338">ДБПРОП_АДК_КАЧЕЧИЛДРОВС</span><span class="sxs-lookup"><span data-stu-id="6c269-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-339">Кэширование отложенных столбцов</span><span class="sxs-lookup"><span data-stu-id="6c269-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="6c269-340">ДБПРОП_КАЧЕДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="6c269-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-341">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="6c269-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-342">ДБПРОП_ЧАНЖЕИНСЕРТЕДРОВС</span><span class="sxs-lookup"><span data-stu-id="6c269-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-343">Права на столбцы</span><span class="sxs-lookup"><span data-stu-id="6c269-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="6c269-344">ДБПРОП_КОЛУМНРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="6c269-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-345">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="6c269-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-346">ДБПРОП_НОТИФИКОЛУМНСЕТ</span><span class="sxs-lookup"><span data-stu-id="6c269-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-347">Столбец доступен для записи</span><span class="sxs-lookup"><span data-stu-id="6c269-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="6c269-348">ДБПРОП_МАЙВРИТЕКОЛУМН</span><span class="sxs-lookup"><span data-stu-id="6c269-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-349">Время ожидания команды</span><span class="sxs-lookup"><span data-stu-id="6c269-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="6c269-350">ДБПРОП_КОММАНДТИМЕАУТ</span><span class="sxs-lookup"><span data-stu-id="6c269-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-351">Версия обработчика курсора</span><span class="sxs-lookup"><span data-stu-id="6c269-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="6c269-352">ДБПРОП_АДК_ЦЕВЕР</span><span class="sxs-lookup"><span data-stu-id="6c269-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-353">ОтКладывание столбца</span><span class="sxs-lookup"><span data-stu-id="6c269-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="6c269-354">ДБПРОП_ДЕФЕРРЕД</span><span class="sxs-lookup"><span data-stu-id="6c269-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-355">ОтКладывание обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="6c269-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="6c269-356">ДБПРОП_ДЕЛАЙСТОРАЖЕОБЖЕКТС</span><span class="sxs-lookup"><span data-stu-id="6c269-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-357">Извлечение назад</span><span class="sxs-lookup"><span data-stu-id="6c269-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="6c269-358">ДБПРОП_КАНФЕТЧБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="6c269-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-359">Операции фильтра</span><span class="sxs-lookup"><span data-stu-id="6c269-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="6c269-360">ДБПРОП_ФИЛТЕРКОМПАРЕОПС</span><span class="sxs-lookup"><span data-stu-id="6c269-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-361">Операции поиска</span><span class="sxs-lookup"><span data-stu-id="6c269-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="6c269-362">ДБПРОП_ФИНДКОМПАРЕОПС</span><span class="sxs-lookup"><span data-stu-id="6c269-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-363">Скрытые столбцы (количество)</span><span class="sxs-lookup"><span data-stu-id="6c269-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="6c269-364">ДБПРОП_ХИДДЕНКОЛУМНС (3)</span><span class="sxs-lookup"><span data-stu-id="6c269-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-365">Удержание строк</span><span class="sxs-lookup"><span data-stu-id="6c269-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-366">ДБПРОП_КАНХОЛДРОВС</span><span class="sxs-lookup"><span data-stu-id="6c269-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-367">Строки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="6c269-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-368">ДБПРОП_ИММОБИЛЕРОВС</span><span class="sxs-lookup"><span data-stu-id="6c269-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-369">Размер начальной извлечения</span><span class="sxs-lookup"><span data-stu-id="6c269-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="6c269-370">ДБПРОП_АСИНЧПРЕФЕТЧСИЗЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-371">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="6c269-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6c269-372">ДБПРОП_ЛИТЕРАЛБУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="6c269-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-373">Идентификация строк литералов</span><span class="sxs-lookup"><span data-stu-id="6c269-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6c269-374">ДБПРОП_ЛИТЕРАЛИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="6c269-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-375">Ведение состояния изменения</span><span class="sxs-lookup"><span data-stu-id="6c269-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="6c269-376">ДБПРОП_АДК_МАИНТАИНЧАНЖЕСТАТУС</span><span class="sxs-lookup"><span data-stu-id="6c269-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-377">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="6c269-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-378">ДБПРОП_МАКСОПЕНРОВС</span><span class="sxs-lookup"><span data-stu-id="6c269-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-379">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="6c269-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-380">ДБПРОП_МАКСПЕНДИНГРОВС</span><span class="sxs-lookup"><span data-stu-id="6c269-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-381">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="6c269-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-382">ДБПРОП_МАКСРОВС (4)</span><span class="sxs-lookup"><span data-stu-id="6c269-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-383">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="6c269-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="6c269-384">ДБПРОП_МЕМОРЮСАЖЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-385">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="6c269-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="6c269-386">ДБПРОП_НОТИФИКАТИОНГРАНУЛАРИТИ</span><span class="sxs-lookup"><span data-stu-id="6c269-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-387">Этапы уведомления</span><span class="sxs-lookup"><span data-stu-id="6c269-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="6c269-388">ДБПРОП_НОТИФИКАТИОНФАСЕС</span><span class="sxs-lookup"><span data-stu-id="6c269-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-389">Объекты, транзакционные</span><span class="sxs-lookup"><span data-stu-id="6c269-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="6c269-390">ДБПРОП_ТРАНСАКТЕДОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="6c269-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-391">Видны другие изменения</span><span class="sxs-lookup"><span data-stu-id="6c269-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6c269-392">ДБПРОП_ОСЕРУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-393">Видимые вставки других пользователей</span><span class="sxs-lookup"><span data-stu-id="6c269-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6c269-394">ДБПРОП_ОСЕРИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="6c269-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-395">Видны изменения</span><span class="sxs-lookup"><span data-stu-id="6c269-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6c269-396">ДБПРОП_ОВНУПДАТЕДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-397">Отображение собственных вставок</span><span class="sxs-lookup"><span data-stu-id="6c269-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6c269-398">ДБПРОП_ОВНИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="6c269-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-399">Сохранение при прерывании</span><span class="sxs-lookup"><span data-stu-id="6c269-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="6c269-400">ДБПРОП_АБОРТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-401">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="6c269-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="6c269-402">ДБПРОП_КОММИТПРЕСЕРВЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-403">Private1</span><span class="sxs-lookup"><span data-stu-id="6c269-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="6c269-404">17:00</span><span class="sxs-lookup"><span data-stu-id="6c269-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-405">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="6c269-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="6c269-406">ДБПРОП_КУИККРЕСТАРТ</span><span class="sxs-lookup"><span data-stu-id="6c269-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-407">Повторные события</span><span class="sxs-lookup"><span data-stu-id="6c269-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="6c269-408">ДБПРОП_РИНТРАНТЕВЕНТС</span><span class="sxs-lookup"><span data-stu-id="6c269-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-409">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="6c269-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-410">ДБПРОП_РЕМОВЕДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="6c269-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-411">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="6c269-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="6c269-412">ДБПРОП_РЕПОРТМУЛТИПЛЕЧАНЖЕС</span><span class="sxs-lookup"><span data-stu-id="6c269-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-413">Изменение имени фигуры</span><span class="sxs-lookup"><span data-stu-id="6c269-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="6c269-414">ДБПРОП_АДК_РЕШАПЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-415">Команда Resync</span><span class="sxs-lookup"><span data-stu-id="6c269-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="6c269-416">ДБПРОП_АДК_КУСТОМРЕСИНЧ</span><span class="sxs-lookup"><span data-stu-id="6c269-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-417">Возврат ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="6c269-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="6c269-418">ДБПРОП_РЕТУРНПЕНДИНГИНСЕРТС</span><span class="sxs-lookup"><span data-stu-id="6c269-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-419">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="6c269-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-420">ДБПРОП_НОТИФИРОВДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-421">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="6c269-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-422">ДБПРОП_НОТИФИРОВФИРСТЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-423">Уведомление о вставке строк</span><span class="sxs-lookup"><span data-stu-id="6c269-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-424">ДБПРОП_НОТИФИРОВИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="6c269-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-425">Права на строки</span><span class="sxs-lookup"><span data-stu-id="6c269-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="6c269-426">ДБПРОП_РОВРЕСТРИКТ</span><span class="sxs-lookup"><span data-stu-id="6c269-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-427">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="6c269-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-428">ДБПРОП_НОТИФИРОВРЕСИНЧ</span><span class="sxs-lookup"><span data-stu-id="6c269-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-429">Потоковая модель для строк</span><span class="sxs-lookup"><span data-stu-id="6c269-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6c269-430">ДБПРОП_РОВСРЕАДМОДЕЛ</span><span class="sxs-lookup"><span data-stu-id="6c269-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-431">Уведомление об отмене изменения строки</span><span class="sxs-lookup"><span data-stu-id="6c269-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-432">ДБПРОП_НОТИФИРОВУНДОЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-433">Уведомление о отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="6c269-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-434">ДБПРОП_НОТИФИРОВУНДОДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-435">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="6c269-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-436">ДБПРОП_НОТИФИРОВУНДОИНСЕРТ</span><span class="sxs-lookup"><span data-stu-id="6c269-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-437">Уведомление об обновлении строк</span><span class="sxs-lookup"><span data-stu-id="6c269-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-438">ДБПРОП_НОТИФИРОВУПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-439">Уведомление об изменении положения при получении набора строк</span><span class="sxs-lookup"><span data-stu-id="6c269-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-440">ДБПРОП_НОТИФИРОВСЕТФЕТЧПОСИТИОНЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-441">Уведомление о выПуске набора строк</span><span class="sxs-lookup"><span data-stu-id="6c269-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="6c269-442">ДБПРОП_НОТИФИРОВСЕТРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-443">ПроКрутка назад</span><span class="sxs-lookup"><span data-stu-id="6c269-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="6c269-444">ДБПРОП_КАНСКРОЛЛБАККВАРДС</span><span class="sxs-lookup"><span data-stu-id="6c269-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-445">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="6c269-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="6c269-446">ДБПРОП_СЕРВЕРКУРСОР</span><span class="sxs-lookup"><span data-stu-id="6c269-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-447">Пропуск удаленных закладок</span><span class="sxs-lookup"><span data-stu-id="6c269-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6c269-448">ДБПРОП_БУКМАРКСКИППЕД</span><span class="sxs-lookup"><span data-stu-id="6c269-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-449">Строгая идентификация строк</span><span class="sxs-lookup"><span data-stu-id="6c269-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6c269-450">ДБПРОП_СТРОНГИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="6c269-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-451">Уникальный каталог</span><span class="sxs-lookup"><span data-stu-id="6c269-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="6c269-452">ДБПРОП_АДК_УНИКУЕКАТАЛОГ</span><span class="sxs-lookup"><span data-stu-id="6c269-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-453">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="6c269-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="6c269-454">ДБПРОП_УНИКУЕРОВС</span><span class="sxs-lookup"><span data-stu-id="6c269-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-455">Уникальная схема</span><span class="sxs-lookup"><span data-stu-id="6c269-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="6c269-456">ДБПРОП_АДК_УНИКУЕСЧЕМА</span><span class="sxs-lookup"><span data-stu-id="6c269-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-457">Уникальная таблица</span><span class="sxs-lookup"><span data-stu-id="6c269-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="6c269-458">ДБПРОП_АДК_УНИКУЕТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="6c269-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-459">Обновление</span><span class="sxs-lookup"><span data-stu-id="6c269-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="6c269-460">ДБПРОП_УПДАТАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="6c269-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-461">Условия обновления</span><span class="sxs-lookup"><span data-stu-id="6c269-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="6c269-462">ДБПРОП_АДК_УПДАТЕКРИТЕРИА</span><span class="sxs-lookup"><span data-stu-id="6c269-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c269-463">Повторная синхронизация обновлений</span><span class="sxs-lookup"><span data-stu-id="6c269-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="6c269-464">ДБПРОП_АДК_УПДАТЕРЕСИНК</span><span class="sxs-lookup"><span data-stu-id="6c269-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c269-465">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="6c269-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6c269-466">ДБПРОП_БУКМАРКС</span><span class="sxs-lookup"><span data-stu-id="6c269-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

