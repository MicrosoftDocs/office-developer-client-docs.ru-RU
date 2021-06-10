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
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="c234d-102">Индекс динамических свойств ADO</span><span class="sxs-lookup"><span data-stu-id="c234d-102">ADO dynamic property index</span></span>

<span data-ttu-id="c234d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c234d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c234d-104">Поставщики данных, поставщики услуг и компоненты служб могут добавлять динамические свойства в коллекции **свойств** незапертых объектов [Подключения](connection-object-ado.md) и [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c234d-104">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="c234d-105">Данный поставщик может также вставить дополнительные свойства при открывлении этих объектов.</span><span class="sxs-lookup"><span data-stu-id="c234d-105">A given provider may also insert additional properties when these objects are opened.</span></span> <span data-ttu-id="c234d-106">Некоторые из этих свойств перечислены в разделе [ADO Dynamic Properties.](ado-dynamic-properties.md)</span><span class="sxs-lookup"><span data-stu-id="c234d-106">Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section.</span></span> <span data-ttu-id="c234d-107">Дополнительные статьи перечислены в разделе [Приложение A: Providers.](appendix-a-providers.md)</span><span class="sxs-lookup"><span data-stu-id="c234d-107">More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="c234d-108">Ниже приведен перекрестный индекс имен ADO и OLE DB для каждого стандартного динамического свойства поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c234d-108">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span> <span data-ttu-id="c234d-109">Поставщики могут добавлять больше свойств, чем указано здесь.</span><span class="sxs-lookup"><span data-stu-id="c234d-109">Your providers may add more properties than listed here.</span></span> <span data-ttu-id="c234d-110">Сведения о динамических свойствах конкретного поставщика см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="c234d-110">For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="c234d-111">Ссылка программиста OLE DB относится к имени свойства ADO по термину "Описание".</span><span class="sxs-lookup"><span data-stu-id="c234d-111">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="c234d-112">Дополнительные сведения об этих стандартных свойствах можно найти в справке программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c234d-112">You can find more information about these standard properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="c234d-113">Поиск имени свойства OLE DB в Индексе или см. следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="c234d-113">Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="c234d-114">Приложение C: OLE DB Properties</span><span class="sxs-lookup"><span data-stu-id="c234d-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="c234d-115">Поддерживаемые свойства службы cursor</span><span class="sxs-lookup"><span data-stu-id="c234d-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="c234d-116">Поддерживаемые свойства поставщика сохраняемости</span><span class="sxs-lookup"><span data-stu-id="c234d-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="c234d-117">Поддерживаемые свойства OLE DB поставщика remoting</span><span class="sxs-lookup"><span data-stu-id="c234d-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="c234d-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="c234d-118">Remarks</span></span>

<span data-ttu-id="c234d-119">Номера примечание, используемые в перекрестных индексах:</span><span class="sxs-lookup"><span data-stu-id="c234d-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="c234d-120">(1) Это свойство — флаг Boolean, указывающий, следует ли использовать названный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c234d-120">(1) This property is a Boolean flag indicating whether the named interface should be used.</span></span> <span data-ttu-id="c234d-121">Эквивалентное имя свойства OLE DB перечислены, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="c234d-121">The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="c234d-122">(2) Свойство ADO "Bookmarkable" создается внутренне для обратной совместимости и сопопомечается с свойством OLE DB, DBPROP \_ IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="c234d-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="c234d-123">Это то же свойство, которое соответствует свойству ADO IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="c234d-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="c234d-124">(3) Имя свойства ADO , "Скрытые столбцы", называется иначе, чем имя свойства OLE DB Описание, "Скрытые столбцы кол".</span><span class="sxs-lookup"><span data-stu-id="c234d-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="c234d-125">(4) Для иерархических записей свойство ADO "Maximum Rows" применяется во всех детях.</span><span class="sxs-lookup"><span data-stu-id="c234d-125">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children.</span></span> <span data-ttu-id="c234d-126">В зависимости от порядка, в котором возвращаются строки, в наборе результатов могут быть все, некоторые или нет детей для каждого родителя или детей-сирот.</span><span class="sxs-lookup"><span data-stu-id="c234d-126">Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set.</span></span> <span data-ttu-id="c234d-127">Поэтому при переописывке иерархических записей идентификатор для каждого ребенка должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="c234d-127">Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique.</span></span> <span data-ttu-id="c234d-128">Как правило, служба формирования данных Майкрософт для [поставщика OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) не позволяет проводить различие между свойствами, которые могут наследоваться от родителя, и свойствами, которые не могут быть унаследованы.</span><span class="sxs-lookup"><span data-stu-id="c234d-128">In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="c234d-129">(5) Не применяется.</span><span class="sxs-lookup"><span data-stu-id="c234d-129">(5) Does not apply.</span></span>

<span data-ttu-id="c234d-130">**Динамические свойства подключения**</span><span class="sxs-lookup"><span data-stu-id="c234d-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c234d-131">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c234d-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c234d-132">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c234d-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c234d-133">Активные сеансы</span><span class="sxs-lookup"><span data-stu-id="c234d-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="c234d-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="c234d-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="c234d-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="c234d-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="c234d-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="c234d-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="c234d-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="c234d-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-139">Уровни изоляции автокоммита</span><span class="sxs-lookup"><span data-stu-id="c234d-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c234d-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c234d-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-141">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="c234d-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="c234d-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="c234d-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-143">Термин Каталог</span><span class="sxs-lookup"><span data-stu-id="c234d-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="c234d-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="c234d-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-145">Определение столбцов</span><span class="sxs-lookup"><span data-stu-id="c234d-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="c234d-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="c234d-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-147">Подключение Время от времени</span><span class="sxs-lookup"><span data-stu-id="c234d-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="c234d-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c234d-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-149">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="c234d-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="c234d-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="c234d-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-151">Источник данных</span><span class="sxs-lookup"><span data-stu-id="c234d-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="c234d-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="c234d-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-153">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="c234d-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="c234d-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="c234d-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-155">Модель потоковой обработки объектов источника данных</span><span class="sxs-lookup"><span data-stu-id="c234d-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c234d-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c234d-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-157">Имя DBMS</span><span class="sxs-lookup"><span data-stu-id="c234d-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="c234d-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="c234d-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-159">Версия DBMS</span><span class="sxs-lookup"><span data-stu-id="c234d-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="c234d-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="c234d-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-161">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="c234d-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="c234d-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="c234d-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-163">Поддержка GROUP BY</span><span class="sxs-lookup"><span data-stu-id="c234d-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="c234d-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="c234d-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-165">Гетерогенная поддержка таблиц</span><span class="sxs-lookup"><span data-stu-id="c234d-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="c234d-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="c234d-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-167">Чувствительность к делу идентификатора</span><span class="sxs-lookup"><span data-stu-id="c234d-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="c234d-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="c234d-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-169">Начальный каталог</span><span class="sxs-lookup"><span data-stu-id="c234d-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="c234d-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c234d-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-171">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="c234d-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c234d-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c234d-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-173">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="c234d-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="c234d-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="c234d-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-175">Идентификатор locale</span><span class="sxs-lookup"><span data-stu-id="c234d-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="c234d-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="c234d-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-177">Расположение</span><span class="sxs-lookup"><span data-stu-id="c234d-177">Location</span></span></p></td>
<td><p><span data-ttu-id="c234d-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="c234d-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-179">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="c234d-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="c234d-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="c234d-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-181">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="c234d-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="c234d-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="c234d-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-183">Максимальный размер строки включает BLOB</span><span class="sxs-lookup"><span data-stu-id="c234d-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="c234d-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="c234d-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-185">Максимальные таблицы в SELECT</span><span class="sxs-lookup"><span data-stu-id="c234d-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="c234d-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="c234d-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-187">Режим</span><span class="sxs-lookup"><span data-stu-id="c234d-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="c234d-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="c234d-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-189">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="c234d-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="c234d-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="c234d-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-191">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="c234d-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="c234d-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="c234d-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-193">Несколько служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="c234d-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c234d-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c234d-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-195">Обновление с несколькими таблицами</span><span class="sxs-lookup"><span data-stu-id="c234d-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="c234d-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="c234d-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-197">Порядок коллансирования NULL</span><span class="sxs-lookup"><span data-stu-id="c234d-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="c234d-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="c234d-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-199">NULL Concatenation Behaviour</span><span class="sxs-lookup"><span data-stu-id="c234d-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="c234d-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c234d-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-201">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="c234d-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="c234d-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="c234d-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-203">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="c234d-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="c234d-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="c234d-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-205">Поддержка объектов OLE</span><span class="sxs-lookup"><span data-stu-id="c234d-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="c234d-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c234d-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-207">Поддержка open Rowset</span><span class="sxs-lookup"><span data-stu-id="c234d-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="c234d-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c234d-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="c234d-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="c234d-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="c234d-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-211">Доступность параметров вывода</span><span class="sxs-lookup"><span data-stu-id="c234d-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="c234d-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="c234d-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="c234d-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="c234d-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="c234d-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-215">Password</span><span class="sxs-lookup"><span data-stu-id="c234d-215">Password</span></span></p></td>
<td><p><span data-ttu-id="c234d-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="c234d-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-217">Сохраняются сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="c234d-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="c234d-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="c234d-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-219">Тип сохраняемого ID</span><span class="sxs-lookup"><span data-stu-id="c234d-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="c234d-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="c234d-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-221">Подготовка поведения прервать</span><span class="sxs-lookup"><span data-stu-id="c234d-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="c234d-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c234d-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-223">Подготовка поведения фиксации</span><span class="sxs-lookup"><span data-stu-id="c234d-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="c234d-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c234d-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-225">Термин процедуры</span><span class="sxs-lookup"><span data-stu-id="c234d-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="c234d-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="c234d-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="c234d-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="c234d-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="c234d-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-229">Удобное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c234d-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="c234d-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="c234d-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-231">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c234d-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="c234d-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="c234d-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-233">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="c234d-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="c234d-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="c234d-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-235">Read-Only источник данных</span><span class="sxs-lookup"><span data-stu-id="c234d-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="c234d-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="c234d-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-237">Преобразования rowset в командной строке</span><span class="sxs-lookup"><span data-stu-id="c234d-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="c234d-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="c234d-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-239">Термин Схемы</span><span class="sxs-lookup"><span data-stu-id="c234d-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="c234d-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="c234d-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-241">Использование схемы</span><span class="sxs-lookup"><span data-stu-id="c234d-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="c234d-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="c234d-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-243">SQL Поддержка</span><span class="sxs-lookup"><span data-stu-id="c234d-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="c234d-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c234d-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-245">Структурированные служба хранилища</span><span class="sxs-lookup"><span data-stu-id="c234d-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="c234d-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="c234d-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-247">Поддержка subquery</span><span class="sxs-lookup"><span data-stu-id="c234d-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="c234d-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="c234d-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-249">Термин Таблица</span><span class="sxs-lookup"><span data-stu-id="c234d-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="c234d-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="c234d-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-251">DDL транзакций</span><span class="sxs-lookup"><span data-stu-id="c234d-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="c234d-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="c234d-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-253">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="c234d-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="c234d-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="c234d-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-255">имя пользователя;</span><span class="sxs-lookup"><span data-stu-id="c234d-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="c234d-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="c234d-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-257">Ручка окна</span><span class="sxs-lookup"><span data-stu-id="c234d-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="c234d-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="c234d-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c234d-259">**Динамические свойства Recordset**</span><span class="sxs-lookup"><span data-stu-id="c234d-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="c234d-260">Обратите внимание, **что динамические свойства** объекта **Recordset** выйдут из сферы действия (становятся недоступными) при закрытии **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="c234d-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c234d-261">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c234d-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c234d-262">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c234d-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c234d-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="c234d-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="c234d-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="c234d-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="c234d-266">(1)</span><span class="sxs-lookup"><span data-stu-id="c234d-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c234d-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="c234d-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c234d-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="c234d-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c234d-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="c234d-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="c234d-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="c234d-274">(1)</span><span class="sxs-lookup"><span data-stu-id="c234d-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="c234d-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="c234d-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="c234d-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="c234d-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="c234d-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="c234d-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="c234d-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="c234d-282">(1)</span><span class="sxs-lookup"><span data-stu-id="c234d-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c234d-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="c234d-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="c234d-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="c234d-286">(1)</span><span class="sxs-lookup"><span data-stu-id="c234d-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="c234d-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="c234d-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c234d-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="c234d-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c234d-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="c234d-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c234d-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="c234d-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="c234d-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="c234d-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="c234d-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="c234d-298">(1)</span><span class="sxs-lookup"><span data-stu-id="c234d-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c234d-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="c234d-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c234d-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="c234d-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="c234d-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="c234d-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="c234d-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="c234d-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c234d-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="c234d-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="c234d-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="c234d-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-311">IStream</span><span class="sxs-lookup"><span data-stu-id="c234d-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="c234d-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c234d-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="c234d-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="c234d-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-315">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="c234d-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="c234d-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="c234d-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="c234d-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="c234d-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="c234d-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-319">Асинхронная обработка rowset</span><span class="sxs-lookup"><span data-stu-id="c234d-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="c234d-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="c234d-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-321">Автоматический пересчет</span><span class="sxs-lookup"><span data-stu-id="c234d-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="c234d-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="c234d-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-323">Размер фоновой выборки</span><span class="sxs-lookup"><span data-stu-id="c234d-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="c234d-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="c234d-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-325">Приоритет фоновых потоков</span><span class="sxs-lookup"><span data-stu-id="c234d-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="c234d-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="c234d-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-327">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="c234d-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="c234d-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="c234d-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-329">Блокировка служба хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="c234d-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c234d-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c234d-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-331">Тип закладок</span><span class="sxs-lookup"><span data-stu-id="c234d-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="c234d-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="c234d-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="c234d-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="c234d-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="c234d-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-335">Закладки заказать</span><span class="sxs-lookup"><span data-stu-id="c234d-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="c234d-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c234d-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-337">Детские строки кэша</span><span class="sxs-lookup"><span data-stu-id="c234d-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="c234d-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-339">Отложенные столбцы кэша</span><span class="sxs-lookup"><span data-stu-id="c234d-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="c234d-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="c234d-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-341">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="c234d-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="c234d-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-343">Привилегии столбца</span><span class="sxs-lookup"><span data-stu-id="c234d-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="c234d-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c234d-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-345">Уведомление о наборе столбцов</span><span class="sxs-lookup"><span data-stu-id="c234d-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="c234d-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-347">Колонка Writable</span><span class="sxs-lookup"><span data-stu-id="c234d-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="c234d-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="c234d-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-349">Командный выход</span><span class="sxs-lookup"><span data-stu-id="c234d-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="c234d-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c234d-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-351">Версия двигателя cursor</span><span class="sxs-lookup"><span data-stu-id="c234d-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="c234d-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="c234d-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-353">Столбец Отсрочка</span><span class="sxs-lookup"><span data-stu-id="c234d-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="c234d-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="c234d-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-355">Задержка служба хранилища обновлений объектов</span><span class="sxs-lookup"><span data-stu-id="c234d-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="c234d-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c234d-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="c234d-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="c234d-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c234d-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-359">Операции фильтрации</span><span class="sxs-lookup"><span data-stu-id="c234d-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="c234d-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="c234d-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-361">Поиск операций</span><span class="sxs-lookup"><span data-stu-id="c234d-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="c234d-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="c234d-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-363">Скрытые столбцы (count)</span><span class="sxs-lookup"><span data-stu-id="c234d-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="c234d-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="c234d-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-365">Строки удержания</span><span class="sxs-lookup"><span data-stu-id="c234d-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="c234d-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="c234d-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="c234d-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-369">Начальный размер fetch</span><span class="sxs-lookup"><span data-stu-id="c234d-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="c234d-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="c234d-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-371">Буквальные закладки</span><span class="sxs-lookup"><span data-stu-id="c234d-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c234d-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c234d-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-373">Удостоверение буквальных строк</span><span class="sxs-lookup"><span data-stu-id="c234d-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c234d-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c234d-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-375">Сохранение состояния изменений</span><span class="sxs-lookup"><span data-stu-id="c234d-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="c234d-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="c234d-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-377">Максимальные открытые строки</span><span class="sxs-lookup"><span data-stu-id="c234d-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="c234d-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-379">Максимальное количество ожидающих строк</span><span class="sxs-lookup"><span data-stu-id="c234d-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="c234d-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-381">Максимальные строки</span><span class="sxs-lookup"><span data-stu-id="c234d-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="c234d-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-383">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="c234d-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="c234d-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="c234d-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-385">Детализация уведомлений</span><span class="sxs-lookup"><span data-stu-id="c234d-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="c234d-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="c234d-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-387">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="c234d-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="c234d-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="c234d-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="c234d-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="c234d-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="c234d-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-391">Видимые изменения других</span><span class="sxs-lookup"><span data-stu-id="c234d-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c234d-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c234d-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-393">Видимые вставки других</span><span class="sxs-lookup"><span data-stu-id="c234d-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c234d-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="c234d-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-395">Собственные изменения Видимые</span><span class="sxs-lookup"><span data-stu-id="c234d-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c234d-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c234d-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-397">Собственные вставки Видимые</span><span class="sxs-lookup"><span data-stu-id="c234d-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c234d-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="c234d-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-399">Сохранение на abort</span><span class="sxs-lookup"><span data-stu-id="c234d-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="c234d-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c234d-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-401">Сохранение на коммит</span><span class="sxs-lookup"><span data-stu-id="c234d-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="c234d-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c234d-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-403">Private1</span><span class="sxs-lookup"><span data-stu-id="c234d-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="c234d-404">(5)</span><span class="sxs-lookup"><span data-stu-id="c234d-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-405">Быстрая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="c234d-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="c234d-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="c234d-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-407">События для повторного антуламента</span><span class="sxs-lookup"><span data-stu-id="c234d-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="c234d-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="c234d-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-409">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="c234d-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="c234d-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-411">Отчет о нескольких изменениях</span><span class="sxs-lookup"><span data-stu-id="c234d-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="c234d-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c234d-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-413">Переописываю имя</span><span class="sxs-lookup"><span data-stu-id="c234d-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="c234d-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="c234d-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-415">Команда Resync</span><span class="sxs-lookup"><span data-stu-id="c234d-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="c234d-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c234d-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-417">Возвращение ожидающих вставок</span><span class="sxs-lookup"><span data-stu-id="c234d-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="c234d-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="c234d-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-419">Уведомление об удалении строки</span><span class="sxs-lookup"><span data-stu-id="c234d-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="c234d-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-421">Уведомление о первом изменении строки</span><span class="sxs-lookup"><span data-stu-id="c234d-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="c234d-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-423">Уведомление о вставке строки</span><span class="sxs-lookup"><span data-stu-id="c234d-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="c234d-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-425">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="c234d-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="c234d-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c234d-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-427">Уведомление о повторной синхронизации строк</span><span class="sxs-lookup"><span data-stu-id="c234d-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c234d-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-429">Модель потоков строки</span><span class="sxs-lookup"><span data-stu-id="c234d-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c234d-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c234d-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-431">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="c234d-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="c234d-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-433">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="c234d-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="c234d-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-435">Уведомление об отмене строки</span><span class="sxs-lookup"><span data-stu-id="c234d-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="c234d-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-437">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="c234d-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="c234d-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="c234d-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="c234d-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-441">Уведомление о выпуске Rowset</span><span class="sxs-lookup"><span data-stu-id="c234d-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="c234d-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="c234d-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-443">Прокрутите назад</span><span class="sxs-lookup"><span data-stu-id="c234d-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="c234d-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c234d-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-445">Курсор сервера</span><span class="sxs-lookup"><span data-stu-id="c234d-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="c234d-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="c234d-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-447">Пропустить удаленные закладки</span><span class="sxs-lookup"><span data-stu-id="c234d-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c234d-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="c234d-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-449">Удостоверение Strong Row</span><span class="sxs-lookup"><span data-stu-id="c234d-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c234d-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c234d-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-451">Уникальный каталог</span><span class="sxs-lookup"><span data-stu-id="c234d-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="c234d-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="c234d-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-453">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="c234d-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="c234d-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="c234d-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-455">Уникальная схема</span><span class="sxs-lookup"><span data-stu-id="c234d-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="c234d-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="c234d-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-457">Уникальная таблица</span><span class="sxs-lookup"><span data-stu-id="c234d-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="c234d-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="c234d-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="c234d-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="c234d-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="c234d-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-461">Критерии обновления</span><span class="sxs-lookup"><span data-stu-id="c234d-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="c234d-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="c234d-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c234d-463">Обновление Resync</span><span class="sxs-lookup"><span data-stu-id="c234d-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="c234d-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="c234d-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c234d-465">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="c234d-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c234d-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c234d-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

