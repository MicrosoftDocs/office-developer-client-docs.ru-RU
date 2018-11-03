---
title: Индекс динамических свойств ADO
TOCTitle: ADO dynamic property index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19b7ddca0395869b5a1dba4182a123d33e54e66d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947604"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="6823e-102">Индекс динамических свойств ADO</span><span class="sxs-lookup"><span data-stu-id="6823e-102">ADO dynamic property index</span></span>

<span data-ttu-id="6823e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6823e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6823e-104">Поставщики данных, поставщиков услуг и компоненты службы можно добавить динамические свойства коллекции **свойств** объектов неоткрытый [подключения](connection-object-ado.md) и [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6823e-104">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="6823e-105">Данный поставщик также вставить дополнительные свойства при открытии эти объекты.</span><span class="sxs-lookup"><span data-stu-id="6823e-105">A given provider may also insert additional properties when these objects are opened.</span></span> <span data-ttu-id="6823e-106">В разделе [Свойства динамического ADO](ado-dynamic-properties.md) перечислены некоторые из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="6823e-106">Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section.</span></span> <span data-ttu-id="6823e-107">Больше, указанных для конкретных поставщиков в разделе [Приложение а: поставщиков](appendix-a-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="6823e-107">More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="6823e-108">В таблице ниже приведен cross-index имен ADO и OLE DB для каждого стандартных OLE DB поставщика динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="6823e-108">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span> <span data-ttu-id="6823e-109">Ваше поставщики могут добавлять несколько свойств, чем перечисленных здесь.</span><span class="sxs-lookup"><span data-stu-id="6823e-109">Your providers may add more properties than listed here.</span></span> <span data-ttu-id="6823e-110">Определенные сведения о динамических свойств от поставщика обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="6823e-110">For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="6823e-111">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="6823e-111">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="6823e-112">Дополнительные сведения об этих стандартных свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6823e-112">You can find more information about these standard properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="6823e-113">Поиск имени свойства OLE DB в индексе или в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="6823e-113">Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="6823e-114">Приложение c. свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6823e-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="6823e-115">Поддерживаемые свойства службы курсора</span><span class="sxs-lookup"><span data-stu-id="6823e-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="6823e-116">Поддерживаемые свойства поставщика службы сохранения</span><span class="sxs-lookup"><span data-stu-id="6823e-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="6823e-117">Свойства Поддерживаемые OLE DB поставщика удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="6823e-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="6823e-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="6823e-118">Remarks</span></span>

<span data-ttu-id="6823e-119">Обратите внимание на номера, используемые в cross-index.</span><span class="sxs-lookup"><span data-stu-id="6823e-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="6823e-120">(1) это свойство соответствует флаг типа Boolean, указывающее, следует ли использовать данный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6823e-120">(1) This property is a Boolean flag indicating whether the named interface should be used.</span></span> <span data-ttu-id="6823e-121">Имя свойства в эквивалентный OLE DB отображается, если он существует.</span><span class="sxs-lookup"><span data-stu-id="6823e-121">The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="6823e-122">(2) свойство «Bookmarkable» ADO создается внутренне для обратной совместимости и назначается свойству OLE DB DBPROP\_IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="6823e-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="6823e-123">Это то же свойство, которое соответствует свойству ADO IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="6823e-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="6823e-124">(3) ADO имя свойства, «Скрытые столбцы», называется иначе, чем имя свойства OLE DB описания, «Count скрытые столбцы».</span><span class="sxs-lookup"><span data-stu-id="6823e-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="6823e-125">(4) для иерархические наборы записей ADO «Максимальное число строк» свойство получает применять на все дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="6823e-125">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children.</span></span> <span data-ttu-id="6823e-126">В зависимости от того, в том порядке, в котором возвращенных строк может содержать все, некоторые или нет дочерних элементов для каждого родительского или потерянного дочерние элементы в наборе результатов.</span><span class="sxs-lookup"><span data-stu-id="6823e-126">Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set.</span></span> <span data-ttu-id="6823e-127">Таким образом после изменения формы иерархические наборы записей, идентификатор для каждого дочернего должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="6823e-127">Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique.</span></span> <span data-ttu-id="6823e-128">В общем случае поставщика [Услуг формирования Microsoft данных для OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) не разрешает различие между свойства, которые могут наследоваться от родительского сайта и те, которые не могут быть унаследованы.</span><span class="sxs-lookup"><span data-stu-id="6823e-128">In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="6823e-129">(5) не применяется.</span><span class="sxs-lookup"><span data-stu-id="6823e-129">(5) Does not apply.</span></span>

<span data-ttu-id="6823e-130">**Динамические свойства подключения**</span><span class="sxs-lookup"><span data-stu-id="6823e-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6823e-131">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="6823e-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6823e-132">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6823e-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6823e-133">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="6823e-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="6823e-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="6823e-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-135">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="6823e-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="6823e-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="6823e-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-137">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="6823e-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="6823e-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="6823e-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-139">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="6823e-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="6823e-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="6823e-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-141">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="6823e-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="6823e-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="6823e-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-143">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="6823e-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="6823e-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="6823e-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-145">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="6823e-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="6823e-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="6823e-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-147">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="6823e-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="6823e-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6823e-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-149">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="6823e-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="6823e-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="6823e-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-151">Источник данных</span><span class="sxs-lookup"><span data-stu-id="6823e-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="6823e-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="6823e-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-153">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="6823e-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="6823e-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="6823e-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-155">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="6823e-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6823e-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="6823e-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-157">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="6823e-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="6823e-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="6823e-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-159">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="6823e-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="6823e-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="6823e-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-161">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="6823e-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="6823e-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="6823e-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-163">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="6823e-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="6823e-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="6823e-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-165">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="6823e-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="6823e-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="6823e-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-167">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="6823e-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="6823e-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="6823e-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-169">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="6823e-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="6823e-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6823e-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-171">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="6823e-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="6823e-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="6823e-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-173">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="6823e-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="6823e-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="6823e-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-175">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="6823e-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="6823e-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="6823e-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-177">Location</span><span class="sxs-lookup"><span data-stu-id="6823e-177">Location</span></span></p></td>
<td><p><span data-ttu-id="6823e-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="6823e-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-179">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="6823e-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="6823e-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="6823e-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-181">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="6823e-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="6823e-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="6823e-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-183">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="6823e-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="6823e-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="6823e-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-185">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="6823e-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="6823e-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="6823e-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-187">Mode</span><span class="sxs-lookup"><span data-stu-id="6823e-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="6823e-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="6823e-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-189">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="6823e-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="6823e-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="6823e-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-191">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="6823e-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="6823e-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="6823e-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-193">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="6823e-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6823e-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6823e-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-195">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="6823e-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="6823e-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="6823e-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-197">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="6823e-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="6823e-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="6823e-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-199">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="6823e-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="6823e-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6823e-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-201">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="6823e-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="6823e-202">DBPROP_INIT_OLEDBSERVICES, УСТАНОВИТЬ</span><span class="sxs-lookup"><span data-stu-id="6823e-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-203">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="6823e-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="6823e-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="6823e-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-205">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="6823e-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="6823e-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6823e-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-207">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="6823e-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="6823e-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="6823e-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-209">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="6823e-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="6823e-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="6823e-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-211">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="6823e-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="6823e-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="6823e-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-213">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="6823e-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="6823e-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="6823e-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-215">Пароль</span><span class="sxs-lookup"><span data-stu-id="6823e-215">Password</span></span></p></td>
<td><p><span data-ttu-id="6823e-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="6823e-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-217">Сохранять сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="6823e-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="6823e-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="6823e-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-219">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="6823e-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="6823e-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="6823e-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-221">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="6823e-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="6823e-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6823e-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-223">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="6823e-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="6823e-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="6823e-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-225">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="6823e-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="6823e-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="6823e-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-227">Запрос</span><span class="sxs-lookup"><span data-stu-id="6823e-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="6823e-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="6823e-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-229">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="6823e-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="6823e-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="6823e-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-231">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="6823e-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="6823e-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="6823e-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-233">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="6823e-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="6823e-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="6823e-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-235">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="6823e-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="6823e-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="6823e-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-237">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="6823e-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="6823e-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="6823e-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-239">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="6823e-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="6823e-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="6823e-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-241">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="6823e-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="6823e-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="6823e-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-243">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="6823e-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="6823e-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="6823e-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-245">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="6823e-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="6823e-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="6823e-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-247">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="6823e-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="6823e-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="6823e-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-249">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="6823e-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="6823e-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="6823e-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-251">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="6823e-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="6823e-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="6823e-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-253">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="6823e-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="6823e-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="6823e-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-255">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="6823e-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="6823e-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="6823e-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-257">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="6823e-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="6823e-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="6823e-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6823e-259">**Свойства динамической набора записей**</span><span class="sxs-lookup"><span data-stu-id="6823e-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="6823e-260">Обратите внимание, что **Динамические свойства** объекта **набора записей** выйдет из области действия (становятся недоступными) при закрытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6823e-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6823e-261">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="6823e-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="6823e-262">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="6823e-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6823e-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="6823e-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="6823e-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="6823e-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="6823e-266">(1)</span><span class="sxs-lookup"><span data-stu-id="6823e-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="6823e-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="6823e-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="6823e-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="6823e-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="6823e-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="6823e-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="6823e-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="6823e-274">(1)</span><span class="sxs-lookup"><span data-stu-id="6823e-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="6823e-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="6823e-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="6823e-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="6823e-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="6823e-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="6823e-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="6823e-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="6823e-282">(1)</span><span class="sxs-lookup"><span data-stu-id="6823e-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="6823e-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="6823e-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="6823e-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="6823e-286">(1)</span><span class="sxs-lookup"><span data-stu-id="6823e-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="6823e-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="6823e-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="6823e-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="6823e-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="6823e-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="6823e-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="6823e-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="6823e-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="6823e-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="6823e-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="6823e-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="6823e-298">(1)</span><span class="sxs-lookup"><span data-stu-id="6823e-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="6823e-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="6823e-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="6823e-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="6823e-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="6823e-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="6823e-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="6823e-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="6823e-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="6823e-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="6823e-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="6823e-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="6823e-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-311">IStream</span><span class="sxs-lookup"><span data-stu-id="6823e-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="6823e-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="6823e-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="6823e-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="6823e-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-315">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="6823e-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="6823e-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="6823e-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-317">Только для добавления строк</span><span class="sxs-lookup"><span data-stu-id="6823e-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="6823e-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="6823e-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-319">Обработка асинхронных строк</span><span class="sxs-lookup"><span data-stu-id="6823e-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="6823e-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="6823e-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-321">Автоматическое обновление ссылок</span><span class="sxs-lookup"><span data-stu-id="6823e-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="6823e-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="6823e-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-323">Размер выборки фона</span><span class="sxs-lookup"><span data-stu-id="6823e-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="6823e-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="6823e-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-325">Приоритет потока фона</span><span class="sxs-lookup"><span data-stu-id="6823e-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="6823e-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="6823e-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-327">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="6823e-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="6823e-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="6823e-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-329">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="6823e-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="6823e-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6823e-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-331">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="6823e-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="6823e-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="6823e-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="6823e-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="6823e-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="6823e-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-335">Упорядоченные закладки</span><span class="sxs-lookup"><span data-stu-id="6823e-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="6823e-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6823e-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-337">Кэш дочерних строк</span><span class="sxs-lookup"><span data-stu-id="6823e-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="6823e-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-339">Кэш отложенной столбцов</span><span class="sxs-lookup"><span data-stu-id="6823e-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="6823e-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="6823e-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-341">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="6823e-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="6823e-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-343">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="6823e-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="6823e-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="6823e-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-345">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="6823e-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="6823e-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-347">Столбец для записи</span><span class="sxs-lookup"><span data-stu-id="6823e-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="6823e-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6823e-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-349">Время ожидания команды</span><span class="sxs-lookup"><span data-stu-id="6823e-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="6823e-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6823e-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-351">Версия модуля текущей позиции</span><span class="sxs-lookup"><span data-stu-id="6823e-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="6823e-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="6823e-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-353">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="6823e-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="6823e-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="6823e-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-355">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="6823e-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="6823e-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6823e-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-357">Выборку</span><span class="sxs-lookup"><span data-stu-id="6823e-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="6823e-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="6823e-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-359">Операции фильтрации</span><span class="sxs-lookup"><span data-stu-id="6823e-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="6823e-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="6823e-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-361">Найдите операций</span><span class="sxs-lookup"><span data-stu-id="6823e-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="6823e-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="6823e-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-363">Скрытые столбцы (количество)</span><span class="sxs-lookup"><span data-stu-id="6823e-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="6823e-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="6823e-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-365">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="6823e-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="6823e-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-367">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="6823e-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="6823e-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-369">Размер начальной выборки</span><span class="sxs-lookup"><span data-stu-id="6823e-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="6823e-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="6823e-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-371">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="6823e-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6823e-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6823e-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-373">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="6823e-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6823e-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="6823e-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-375">Обслуживание изменений состояния</span><span class="sxs-lookup"><span data-stu-id="6823e-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="6823e-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="6823e-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-377">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="6823e-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="6823e-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-379">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="6823e-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="6823e-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-381">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="6823e-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="6823e-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-383">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="6823e-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="6823e-384">ОПРЕДЕЛЕН</span><span class="sxs-lookup"><span data-stu-id="6823e-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-385">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="6823e-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="6823e-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="6823e-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-387">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="6823e-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="6823e-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="6823e-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-389">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="6823e-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="6823e-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="6823e-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-391">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="6823e-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6823e-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="6823e-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-393">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="6823e-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6823e-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="6823e-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-395">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="6823e-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="6823e-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="6823e-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-397">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="6823e-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="6823e-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="6823e-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-399">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="6823e-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="6823e-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="6823e-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-401">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="6823e-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="6823e-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="6823e-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-403">Private1</span><span class="sxs-lookup"><span data-stu-id="6823e-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="6823e-404">(5)</span><span class="sxs-lookup"><span data-stu-id="6823e-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-405">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="6823e-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="6823e-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="6823e-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-407">Повторные события</span><span class="sxs-lookup"><span data-stu-id="6823e-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="6823e-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="6823e-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-409">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="6823e-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="6823e-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-411">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="6823e-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="6823e-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="6823e-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-413">Изменить форму имя</span><span class="sxs-lookup"><span data-stu-id="6823e-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="6823e-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="6823e-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-415">Команда синхронизации</span><span class="sxs-lookup"><span data-stu-id="6823e-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="6823e-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="6823e-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-417">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="6823e-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="6823e-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="6823e-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-419">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="6823e-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="6823e-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-421">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="6823e-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="6823e-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-423">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="6823e-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="6823e-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-425">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="6823e-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="6823e-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="6823e-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-427">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="6823e-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="6823e-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-429">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="6823e-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="6823e-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="6823e-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-431">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="6823e-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="6823e-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-433">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="6823e-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="6823e-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-435">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="6823e-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="6823e-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-437">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="6823e-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="6823e-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-439">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="6823e-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="6823e-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-441">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="6823e-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="6823e-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="6823e-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-443">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="6823e-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="6823e-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="6823e-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-445">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="6823e-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="6823e-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="6823e-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-447">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="6823e-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6823e-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="6823e-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-449">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="6823e-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="6823e-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="6823e-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-451">Уникальный каталога</span><span class="sxs-lookup"><span data-stu-id="6823e-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="6823e-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="6823e-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-453">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="6823e-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="6823e-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="6823e-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-455">Уникальный схемы</span><span class="sxs-lookup"><span data-stu-id="6823e-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="6823e-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="6823e-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-457">Уникальная таблица</span><span class="sxs-lookup"><span data-stu-id="6823e-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="6823e-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="6823e-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-459">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="6823e-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="6823e-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="6823e-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-461">Обновление критериев</span><span class="sxs-lookup"><span data-stu-id="6823e-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="6823e-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="6823e-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6823e-463">Обновление повторной синхронизации</span><span class="sxs-lookup"><span data-stu-id="6823e-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="6823e-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="6823e-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6823e-465">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="6823e-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="6823e-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6823e-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

