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
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="b900b-102">Индекс динамических свойств ADO</span><span class="sxs-lookup"><span data-stu-id="b900b-102">ADO dynamic property index</span></span>

<span data-ttu-id="b900b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b900b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b900b-104">Поставщики данных, поставщики служб и компоненты службы могут добавлять динамические свойства в коллекции **свойств** неподтвершенных объектов [Connection](connection-object-ado.md) и [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b900b-104">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="b900b-105">При открываемом объекте поставщик может также вставлять дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="b900b-105">A given provider may also insert additional properties when these objects are opened.</span></span> <span data-ttu-id="b900b-106">Некоторые из этих свойств перечислены в разделе ["Динамические свойства ADO".](ado-dynamic-properties.md)</span><span class="sxs-lookup"><span data-stu-id="b900b-106">Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section.</span></span> <span data-ttu-id="b900b-107">Дополнительные перечислены в разделе "Конкретные поставщики" [в разделе "Приложение А. Поставщики".](appendix-a-providers.md)</span><span class="sxs-lookup"><span data-stu-id="b900b-107">More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="b900b-108">В таблице ниже приведен перекрестный индекс имен ADO и OLE DB для каждого стандартного динамического свойства поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b900b-108">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span> <span data-ttu-id="b900b-109">Поставщики могут добавлять больше свойств, чем указано здесь.</span><span class="sxs-lookup"><span data-stu-id="b900b-109">Your providers may add more properties than listed here.</span></span> <span data-ttu-id="b900b-110">Конкретные сведения о динамических свойствах, характерных для конкретного поставщика, см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="b900b-110">For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="b900b-111">Справочник программиста OLE DB относится к имени свойства ADO по термину "Description".</span><span class="sxs-lookup"><span data-stu-id="b900b-111">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="b900b-112">Дополнительные сведения об этих стандартных свойствах можно найти в справочнике программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b900b-112">You can find more information about these standard properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="b900b-113">Найщите имя свойства OLE DB в индексе или см. следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="b900b-113">Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="b900b-114">Приложение C. Свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="b900b-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="b900b-115">Поддерживаемые свойства службы курсора</span><span class="sxs-lookup"><span data-stu-id="b900b-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="b900b-116">Поддерживаемые свойства поставщика сохраняемости</span><span class="sxs-lookup"><span data-stu-id="b900b-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="b900b-117">Поддерживаемые свойства OLE DB поставщика remoting</span><span class="sxs-lookup"><span data-stu-id="b900b-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="b900b-118">Заметки</span><span class="sxs-lookup"><span data-stu-id="b900b-118">Remarks</span></span>

<span data-ttu-id="b900b-119">Номера заметок, используемые в перекрестных индексах:</span><span class="sxs-lookup"><span data-stu-id="b900b-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="b900b-120">(1) Это свойство является boolean флагом, указывающим, следует ли использовать именовамый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b900b-120">(1) This property is a Boolean flag indicating whether the named interface should be used.</span></span> <span data-ttu-id="b900b-121">Эквивалентное имя свойства OLE DB указано, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="b900b-121">The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="b900b-122">(2) Свойство ADO Bookmarkable создается внутренним образом для обеспечения обратной совместимости и сопомечется со свойством OLE DB, DBPROP \_ IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="b900b-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="b900b-123">Это то же свойство, которое соответствует свойству ADO IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="b900b-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="b900b-124">(3) Имя свойства ADO, "Hidden Columns", называется иначе, чем имя свойства OLE DB Description, "Hidden Columns Count".</span><span class="sxs-lookup"><span data-stu-id="b900b-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="b900b-125">(4) Для иерархических записей свойство ADO "Maximum Rows" применяется для всех детей.</span><span class="sxs-lookup"><span data-stu-id="b900b-125">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children.</span></span> <span data-ttu-id="b900b-126">В зависимости от порядка, в котором возвращаются строки, в наборе результатов могут быть все, некоторые или никакие дети для каждого родительского или потерянных детей.</span><span class="sxs-lookup"><span data-stu-id="b900b-126">Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set.</span></span> <span data-ttu-id="b900b-127">Поэтому при повторном подмене иерархических записей идентификатор каждого из них должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="b900b-127">Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique.</span></span> <span data-ttu-id="b900b-128">Как правило, служба формирования данных Майкрософт для [поставщика OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) не допускает различия между свойствами, которые могут наследоваться от родительского, и свойствами, которые не могут быть унаследованы.</span><span class="sxs-lookup"><span data-stu-id="b900b-128">In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="b900b-129">(5) Не применяется.</span><span class="sxs-lookup"><span data-stu-id="b900b-129">(5) Does not apply.</span></span>

<span data-ttu-id="b900b-130">**Динамические свойства подключения**</span><span class="sxs-lookup"><span data-stu-id="b900b-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b900b-131">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="b900b-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="b900b-132">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="b900b-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b900b-133">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="b900b-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="b900b-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="b900b-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="b900b-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="b900b-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="b900b-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="b900b-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="b900b-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="b900b-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-139">Уровни изоляции автозафикса</span><span class="sxs-lookup"><span data-stu-id="b900b-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="b900b-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="b900b-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-141">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="b900b-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="b900b-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="b900b-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-143">Термин каталога</span><span class="sxs-lookup"><span data-stu-id="b900b-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="b900b-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="b900b-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-145">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="b900b-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="b900b-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="b900b-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-147">Время подключения</span><span class="sxs-lookup"><span data-stu-id="b900b-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="b900b-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b900b-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-149">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="b900b-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="b900b-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="b900b-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-151">Источник данных</span><span class="sxs-lookup"><span data-stu-id="b900b-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="b900b-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="b900b-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-153">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="b900b-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="b900b-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="b900b-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-155">Потоковая модель объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="b900b-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="b900b-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="b900b-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="b900b-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="b900b-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="b900b-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-159">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="b900b-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="b900b-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="b900b-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-161">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="b900b-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="b900b-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="b900b-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-163">Поддержка GROUP BY</span><span class="sxs-lookup"><span data-stu-id="b900b-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="b900b-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="b900b-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-165">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="b900b-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="b900b-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="b900b-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-167">Чувствительность к делу идентификатора</span><span class="sxs-lookup"><span data-stu-id="b900b-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="b900b-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="b900b-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-169">Начальный каталог</span><span class="sxs-lookup"><span data-stu-id="b900b-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="b900b-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="b900b-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-171">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="b900b-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="b900b-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="b900b-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-173">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="b900b-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="b900b-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="b900b-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-175">Код локального идентификатора</span><span class="sxs-lookup"><span data-stu-id="b900b-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="b900b-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="b900b-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-177">Расположение</span><span class="sxs-lookup"><span data-stu-id="b900b-177">Location</span></span></p></td>
<td><p><span data-ttu-id="b900b-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="b900b-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-179">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="b900b-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="b900b-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="b900b-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-181">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="b900b-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="b900b-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="b900b-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-183">Максимальный размер строки включает BLOB</span><span class="sxs-lookup"><span data-stu-id="b900b-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="b900b-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="b900b-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-185">Максимальное число таблиц в SELECT</span><span class="sxs-lookup"><span data-stu-id="b900b-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="b900b-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="b900b-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-187">Режим</span><span class="sxs-lookup"><span data-stu-id="b900b-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="b900b-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="b900b-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-189">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="b900b-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="b900b-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="b900b-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-191">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="b900b-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="b900b-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="b900b-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-193">Несколько объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="b900b-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="b900b-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b900b-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-195">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="b900b-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="b900b-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="b900b-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-197">Порядок оценки NULL</span><span class="sxs-lookup"><span data-stu-id="b900b-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="b900b-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="b900b-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-199">Поведение при конкатенации NULL</span><span class="sxs-lookup"><span data-stu-id="b900b-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="b900b-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b900b-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-201">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="b900b-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="b900b-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="b900b-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-203">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="b900b-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="b900b-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="b900b-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-205">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="b900b-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="b900b-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b900b-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-207">Поддержка открытого наборов строк</span><span class="sxs-lookup"><span data-stu-id="b900b-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="b900b-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="b900b-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="b900b-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="b900b-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="b900b-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-211">Доступность выходных параметров</span><span class="sxs-lookup"><span data-stu-id="b900b-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="b900b-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="b900b-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="b900b-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="b900b-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="b900b-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-215">Password</span><span class="sxs-lookup"><span data-stu-id="b900b-215">Password</span></span></p></td>
<td><p><span data-ttu-id="b900b-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="b900b-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-217">Сохранить сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="b900b-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="b900b-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="b900b-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-219">Тип сохраняемого ИД</span><span class="sxs-lookup"><span data-stu-id="b900b-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="b900b-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="b900b-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-221">Подготовка поведения для отменить</span><span class="sxs-lookup"><span data-stu-id="b900b-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="b900b-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b900b-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-223">Подготовка поведения фиксации</span><span class="sxs-lookup"><span data-stu-id="b900b-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="b900b-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b900b-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-225">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="b900b-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="b900b-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="b900b-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="b900b-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="b900b-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="b900b-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-229">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="b900b-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="b900b-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="b900b-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-231">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="b900b-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="b900b-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="b900b-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-233">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="b900b-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="b900b-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="b900b-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-235">Read-Only данных</span><span class="sxs-lookup"><span data-stu-id="b900b-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="b900b-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="b900b-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-237">Преобразование наборов строк в команде</span><span class="sxs-lookup"><span data-stu-id="b900b-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="b900b-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="b900b-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-239">Термин схемы</span><span class="sxs-lookup"><span data-stu-id="b900b-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="b900b-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="b900b-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-241">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="b900b-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="b900b-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="b900b-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-243">SQL поддержки</span><span class="sxs-lookup"><span data-stu-id="b900b-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="b900b-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="b900b-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-245">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="b900b-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="b900b-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="b900b-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-247">Поддержка ветвей</span><span class="sxs-lookup"><span data-stu-id="b900b-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="b900b-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="b900b-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="b900b-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="b900b-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="b900b-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-251">DDL транзакции</span><span class="sxs-lookup"><span data-stu-id="b900b-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="b900b-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="b900b-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-253">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="b900b-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="b900b-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="b900b-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-255">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="b900b-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="b900b-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="b900b-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-257">Окне Окне</span><span class="sxs-lookup"><span data-stu-id="b900b-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="b900b-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="b900b-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b900b-259">**Динамические свойства recordset**</span><span class="sxs-lookup"><span data-stu-id="b900b-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="b900b-260">Обратите **внимание, что динамические** свойства объекта **Recordset** выходить за пределы области (становятся недоступными) при закрытии **объекта Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b900b-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b900b-261">ADO Property Name</span><span class="sxs-lookup"><span data-stu-id="b900b-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="b900b-262">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="b900b-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b900b-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="b900b-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="b900b-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="b900b-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="b900b-266">(1)</span><span class="sxs-lookup"><span data-stu-id="b900b-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b900b-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="b900b-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b900b-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="b900b-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b900b-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="b900b-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="b900b-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="b900b-274">(1)</span><span class="sxs-lookup"><span data-stu-id="b900b-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="b900b-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="b900b-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="b900b-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="b900b-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="b900b-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="b900b-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="b900b-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="b900b-282">(1)</span><span class="sxs-lookup"><span data-stu-id="b900b-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b900b-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="b900b-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="b900b-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="b900b-286">(1)</span><span class="sxs-lookup"><span data-stu-id="b900b-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="b900b-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="b900b-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b900b-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="b900b-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b900b-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="b900b-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b900b-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="b900b-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="b900b-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="b900b-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="b900b-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="b900b-298">(1)</span><span class="sxs-lookup"><span data-stu-id="b900b-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="b900b-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="b900b-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b900b-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="b900b-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="b900b-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="b900b-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="b900b-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="b900b-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b900b-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="b900b-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="b900b-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="b900b-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-311">IStream</span><span class="sxs-lookup"><span data-stu-id="b900b-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="b900b-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b900b-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="b900b-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="b900b-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-315">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="b900b-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="b900b-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="b900b-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="b900b-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="b900b-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="b900b-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-319">Асинхронная обработка наборов строк</span><span class="sxs-lookup"><span data-stu-id="b900b-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="b900b-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="b900b-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-321">Автоматический пересчет</span><span class="sxs-lookup"><span data-stu-id="b900b-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="b900b-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="b900b-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-323">Фоновое извлечение размера</span><span class="sxs-lookup"><span data-stu-id="b900b-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="b900b-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="b900b-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-325">Приоритет фонового потока</span><span class="sxs-lookup"><span data-stu-id="b900b-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="b900b-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="b900b-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-327">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="b900b-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="b900b-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="b900b-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-329">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="b900b-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="b900b-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b900b-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-331">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="b900b-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="b900b-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="b900b-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="b900b-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="b900b-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="b900b-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="b900b-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="b900b-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b900b-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-337">Кэш child Rows</span><span class="sxs-lookup"><span data-stu-id="b900b-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="b900b-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-339">Отложенные столбцы кэша</span><span class="sxs-lookup"><span data-stu-id="b900b-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="b900b-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="b900b-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-341">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="b900b-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="b900b-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-343">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="b900b-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="b900b-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b900b-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-345">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="b900b-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="b900b-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-347">Для написываемых столбцов</span><span class="sxs-lookup"><span data-stu-id="b900b-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="b900b-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="b900b-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-349">Время простоя команды</span><span class="sxs-lookup"><span data-stu-id="b900b-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="b900b-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b900b-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-351">Версия курсора</span><span class="sxs-lookup"><span data-stu-id="b900b-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="b900b-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="b900b-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-353">Отложить столбец</span><span class="sxs-lookup"><span data-stu-id="b900b-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="b900b-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="b900b-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-355">Задержка обновлений объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="b900b-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="b900b-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b900b-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="b900b-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="b900b-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b900b-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-359">Операции фильтрации</span><span class="sxs-lookup"><span data-stu-id="b900b-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="b900b-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="b900b-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-361">Поиск операций</span><span class="sxs-lookup"><span data-stu-id="b900b-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="b900b-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="b900b-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-363">Скрытые столбцы (количество)</span><span class="sxs-lookup"><span data-stu-id="b900b-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="b900b-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="b900b-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-365">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="b900b-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="b900b-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-367">Строки Immobile</span><span class="sxs-lookup"><span data-stu-id="b900b-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="b900b-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-369">Начальный размер извлечения</span><span class="sxs-lookup"><span data-stu-id="b900b-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="b900b-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="b900b-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-371">Литеральные закладки</span><span class="sxs-lookup"><span data-stu-id="b900b-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b900b-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b900b-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-373">Идентификатор строки литералов</span><span class="sxs-lookup"><span data-stu-id="b900b-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b900b-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="b900b-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-375">Сохранение состояния изменения</span><span class="sxs-lookup"><span data-stu-id="b900b-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="b900b-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="b900b-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-377">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="b900b-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="b900b-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-379">Максимальное число ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="b900b-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="b900b-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-381">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="b900b-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="b900b-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-383">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="b900b-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="b900b-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="b900b-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-385">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="b900b-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="b900b-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="b900b-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-387">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="b900b-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="b900b-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="b900b-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-389">Transacted объектов</span><span class="sxs-lookup"><span data-stu-id="b900b-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="b900b-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="b900b-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-391">Видимые изменения других</span><span class="sxs-lookup"><span data-stu-id="b900b-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="b900b-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="b900b-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-393">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="b900b-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="b900b-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="b900b-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-395">Собственные изменения, видимые</span><span class="sxs-lookup"><span data-stu-id="b900b-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="b900b-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="b900b-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-397">Собственные вставки видимые</span><span class="sxs-lookup"><span data-stu-id="b900b-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="b900b-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="b900b-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-399">Сохранение при отменить</span><span class="sxs-lookup"><span data-stu-id="b900b-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="b900b-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b900b-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-401">Сохранение при фиксации</span><span class="sxs-lookup"><span data-stu-id="b900b-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="b900b-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b900b-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-403">Private1</span><span class="sxs-lookup"><span data-stu-id="b900b-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="b900b-404">(5)</span><span class="sxs-lookup"><span data-stu-id="b900b-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-405">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="b900b-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="b900b-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="b900b-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="b900b-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="b900b-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="b900b-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-409">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="b900b-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="b900b-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-411">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="b900b-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="b900b-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="b900b-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="b900b-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="b900b-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="b900b-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="b900b-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="b900b-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="b900b-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-417">Возврат ожидающих вставки</span><span class="sxs-lookup"><span data-stu-id="b900b-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="b900b-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="b900b-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-419">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="b900b-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="b900b-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-421">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="b900b-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="b900b-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-423">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="b900b-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="b900b-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-425">Привилегии строк</span><span class="sxs-lookup"><span data-stu-id="b900b-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="b900b-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b900b-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-427">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="b900b-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="b900b-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-429">Модель потоков по строкам</span><span class="sxs-lookup"><span data-stu-id="b900b-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="b900b-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="b900b-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-431">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="b900b-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="b900b-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-433">Уведомление об отмене удаления строки</span><span class="sxs-lookup"><span data-stu-id="b900b-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="b900b-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-435">Уведомление об отмене вставки строки</span><span class="sxs-lookup"><span data-stu-id="b900b-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="b900b-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-437">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="b900b-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="b900b-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="b900b-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="b900b-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-441">Уведомление о выпуске rowset</span><span class="sxs-lookup"><span data-stu-id="b900b-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="b900b-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="b900b-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-443">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="b900b-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="b900b-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b900b-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-445">Курсор сервера</span><span class="sxs-lookup"><span data-stu-id="b900b-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="b900b-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="b900b-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-447">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="b900b-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b900b-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="b900b-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-449">Удостоверение строки strong</span><span class="sxs-lookup"><span data-stu-id="b900b-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b900b-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="b900b-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-451">Уникальный каталог</span><span class="sxs-lookup"><span data-stu-id="b900b-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="b900b-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="b900b-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-453">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="b900b-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="b900b-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="b900b-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-455">Уникальная схема</span><span class="sxs-lookup"><span data-stu-id="b900b-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="b900b-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="b900b-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-457">Уникальная таблица</span><span class="sxs-lookup"><span data-stu-id="b900b-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="b900b-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="b900b-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="b900b-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="b900b-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="b900b-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-461">Условия обновления</span><span class="sxs-lookup"><span data-stu-id="b900b-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="b900b-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="b900b-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b900b-463">Обновление resync</span><span class="sxs-lookup"><span data-stu-id="b900b-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="b900b-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="b900b-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b900b-465">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="b900b-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b900b-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b900b-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

