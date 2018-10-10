---
title: ADO Dynamic Property Index
TOCTitle: ADO Dynamic Property Index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58e9029e7c78a6cbde97973ee7fc482fb116c3f2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480136"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="c7ebe-102">ADO Dynamic Property Index</span><span class="sxs-lookup"><span data-stu-id="c7ebe-102">ADO Dynamic Property Index</span></span>


<span data-ttu-id="c7ebe-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7ebe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c7ebe-104">Поставщики данных, поставщиков услуг и компоненты службы можно добавить динамические свойства коллекции **свойств** объектов неоткрытый [подключения](connection-object-ado.md) и [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c7ebe-104">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="c7ebe-105">Данный поставщик также вставить дополнительные свойства при открытии эти объекты.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-105">A given provider may also insert additional properties when these objects are opened.</span></span> <span data-ttu-id="c7ebe-106">В разделе [Свойства динамического ADO](ado-dynamic-properties.md) перечислены некоторые из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-106">Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section.</span></span> <span data-ttu-id="c7ebe-107">Больше, указанных для конкретных поставщиков в разделе [Приложение а: поставщиков](appendix-a-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="c7ebe-107">More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="c7ebe-108">В таблице ниже приведен cross-index имен ADO и OLE DB для каждого стандартных OLE DB поставщика динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-108">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span> <span data-ttu-id="c7ebe-109">Ваше поставщики могут добавлять несколько свойств, чем перечисленных здесь.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-109">Your providers may add more properties than listed here.</span></span> <span data-ttu-id="c7ebe-110">Определенные сведения о динамических свойств от поставщика обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-110">For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="c7ebe-111">Справочник программиста OLE DB указано имя свойства ADO по слову «Описание».</span><span class="sxs-lookup"><span data-stu-id="c7ebe-111">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</span></span> <span data-ttu-id="c7ebe-112">Дополнительные сведения об этих стандартных свойств можно найти в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-112">You can find more information about these standard properties in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="c7ebe-113">Поиск имени свойства OLE DB в индексе или в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c7ebe-113">Search for the OLE DB property name in the Index or see the following topics:</span></span>

  - <span data-ttu-id="c7ebe-114">Приложение c. свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c7ebe-114">Appendix C: OLE DB Properties</span></span>

  - <span data-ttu-id="c7ebe-115">Поддерживаемые свойства службы курсора</span><span class="sxs-lookup"><span data-stu-id="c7ebe-115">Supported Properties of the Cursor Service</span></span>

  - <span data-ttu-id="c7ebe-116">Поддерживаемые свойства поставщика службы сохранения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-116">Supported Properties of the Persistence Provider</span></span>

  - <span data-ttu-id="c7ebe-117">Свойства Поддерживаемые OLE DB поставщика удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="c7ebe-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="c7ebe-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7ebe-118">Remarks</span></span>

<span data-ttu-id="c7ebe-119">Обратите внимание на номера, используемые в cross-index.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="c7ebe-120">(1) это свойство соответствует флаг типа Boolean, указывающее, следует ли использовать данный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-120">(1) This property is a Boolean flag indicating whether the named interface should be used.</span></span> <span data-ttu-id="c7ebe-121">Имя свойства в эквивалентный OLE DB отображается, если он существует.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-121">The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="c7ebe-122">(2) свойство «Bookmarkable» ADO создается внутренне для обратной совместимости и назначается свойству OLE DB DBPROP\_IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="c7ebe-123">Это то же свойство, которое соответствует свойству ADO IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="c7ebe-124">(3) ADO имя свойства, «Скрытые столбцы», называется иначе, чем имя свойства OLE DB описания, «Count скрытые столбцы».</span><span class="sxs-lookup"><span data-stu-id="c7ebe-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="c7ebe-125">(4) для иерархические наборы записей ADO «Максимальное число строк» свойство получает применять на все дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-125">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children.</span></span> <span data-ttu-id="c7ebe-126">В зависимости от того, в том порядке, в котором возвращенных строк может содержать все, некоторые или нет дочерних элементов для каждого родительского или потерянного дочерние элементы в наборе результатов.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-126">Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set.</span></span> <span data-ttu-id="c7ebe-127">Таким образом после изменения формы иерархические наборы записей, идентификатор для каждого дочернего должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-127">Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique.</span></span> <span data-ttu-id="c7ebe-128">В общем случае поставщика [Услуг формирования Microsoft данных для OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) не разрешает различие между свойства, которые могут наследоваться от родительского сайта и те, которые не могут быть унаследованы.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-128">In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="c7ebe-129">(5) не применяется.</span><span class="sxs-lookup"><span data-stu-id="c7ebe-129">(5) Does not apply.</span></span>

<span data-ttu-id="c7ebe-130">**Динамические свойства подключения**</span><span class="sxs-lookup"><span data-stu-id="c7ebe-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7ebe-131">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c7ebe-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c7ebe-132">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c7ebe-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-133">Активных сеансов</span><span class="sxs-lookup"><span data-stu-id="c7ebe-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-135">Прерывание Asynchable</span><span class="sxs-lookup"><span data-stu-id="c7ebe-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-137">Зафиксировать Asynchable</span><span class="sxs-lookup"><span data-stu-id="c7ebe-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-139">Уровни изоляции автоматической фиксации</span><span class="sxs-lookup"><span data-stu-id="c7ebe-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-141">Расположение каталога</span><span class="sxs-lookup"><span data-stu-id="c7ebe-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="c7ebe-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-143">Каталог терминов</span><span class="sxs-lookup"><span data-stu-id="c7ebe-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="c7ebe-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-145">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="c7ebe-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="c7ebe-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-147">Время ожидания подключения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-149">Текущий каталог</span><span class="sxs-lookup"><span data-stu-id="c7ebe-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="c7ebe-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-151">Источник данных</span><span class="sxs-lookup"><span data-stu-id="c7ebe-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-153">Имя источника данных</span><span class="sxs-lookup"><span data-stu-id="c7ebe-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="c7ebe-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-155">Модель потоков объекта источника данных</span><span class="sxs-lookup"><span data-stu-id="c7ebe-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c7ebe-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-157">Имя СУБД</span><span class="sxs-lookup"><span data-stu-id="c7ebe-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="c7ebe-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-159">Версия СУБД</span><span class="sxs-lookup"><span data-stu-id="c7ebe-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="c7ebe-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-161">Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="c7ebe-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="c7ebe-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-163">ГРУППИРОВКА по поддержке</span><span class="sxs-lookup"><span data-stu-id="c7ebe-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-165">Поддержка разнородных таблиц</span><span class="sxs-lookup"><span data-stu-id="c7ebe-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="c7ebe-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-167">Идентификатор регистра</span><span class="sxs-lookup"><span data-stu-id="c7ebe-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-169">Исходный каталог</span><span class="sxs-lookup"><span data-stu-id="c7ebe-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c7ebe-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-171">Уровни изоляции</span><span class="sxs-lookup"><span data-stu-id="c7ebe-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-173">Хранение изоляции</span><span class="sxs-lookup"><span data-stu-id="c7ebe-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="c7ebe-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-175">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="c7ebe-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="c7ebe-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-177">Location</span><span class="sxs-lookup"><span data-stu-id="c7ebe-177">Location</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="c7ebe-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-179">Максимальный размер индекса</span><span class="sxs-lookup"><span data-stu-id="c7ebe-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-181">Максимальный размер строки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-183">Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</span><span class="sxs-lookup"><span data-stu-id="c7ebe-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="c7ebe-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-185">Максимальная таблиц в Выбор</span><span class="sxs-lookup"><span data-stu-id="c7ebe-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-187">Mode</span><span class="sxs-lookup"><span data-stu-id="c7ebe-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-189">Несколько наборов параметров</span><span class="sxs-lookup"><span data-stu-id="c7ebe-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-191">Несколько результатов</span><span class="sxs-lookup"><span data-stu-id="c7ebe-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-193">Несколько объектов хранения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-195">Обновление нескольких таблицы</span><span class="sxs-lookup"><span data-stu-id="c7ebe-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-197">Порядок сортировки значений NULL</span><span class="sxs-lookup"><span data-stu-id="c7ebe-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="c7ebe-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-199">Поведение NULL объединения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c7ebe-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-201">Службы OLE DB</span><span class="sxs-lookup"><span data-stu-id="c7ebe-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-202">DBPROP_INIT_OLEDBSERVICES, УСТАНОВИТЬ</span><span class="sxs-lookup"><span data-stu-id="c7ebe-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-203">Версия OLE DB</span><span class="sxs-lookup"><span data-stu-id="c7ebe-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="c7ebe-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-205">Поддержка OLE-объектов</span><span class="sxs-lookup"><span data-stu-id="c7ebe-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-207">Поддержка открытых наборов строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-209">ORDER BY столбцы в списке Select</span><span class="sxs-lookup"><span data-stu-id="c7ebe-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-211">Выходной параметр доступности</span><span class="sxs-lookup"><span data-stu-id="c7ebe-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-213">Передайте с указанные методы</span><span class="sxs-lookup"><span data-stu-id="c7ebe-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-215">Пароль</span><span class="sxs-lookup"><span data-stu-id="c7ebe-215">Password</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="c7ebe-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-217">Сохранять сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="c7ebe-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="c7ebe-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-219">Тип сохраняемого идентификатора</span><span class="sxs-lookup"><span data-stu-id="c7ebe-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-221">Подготовка поведение аварийное завершение</span><span class="sxs-lookup"><span data-stu-id="c7ebe-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c7ebe-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-223">Подготовка поведение выделения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="c7ebe-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-225">Процедура терминов</span><span class="sxs-lookup"><span data-stu-id="c7ebe-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="c7ebe-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-227">Запрос</span><span class="sxs-lookup"><span data-stu-id="c7ebe-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-229">Понятное имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c7ebe-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="c7ebe-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-231">Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="c7ebe-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="c7ebe-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-233">Версия поставщика</span><span class="sxs-lookup"><span data-stu-id="c7ebe-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="c7ebe-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-235">Источник данных только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-237">Преобразование строк на команду</span><span class="sxs-lookup"><span data-stu-id="c7ebe-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="c7ebe-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-239">Схема терминов</span><span class="sxs-lookup"><span data-stu-id="c7ebe-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="c7ebe-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-241">Об использовании схемы</span><span class="sxs-lookup"><span data-stu-id="c7ebe-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-243">Поддержка SQL</span><span class="sxs-lookup"><span data-stu-id="c7ebe-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-245">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="c7ebe-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-247">Поддержка вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="c7ebe-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="c7ebe-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-249">В таблице терминов</span><span class="sxs-lookup"><span data-stu-id="c7ebe-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="c7ebe-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-251">Транзакций DDL</span><span class="sxs-lookup"><span data-stu-id="c7ebe-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="c7ebe-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-253">Идентификатор пользователя</span><span class="sxs-lookup"><span data-stu-id="c7ebe-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="c7ebe-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-255">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="c7ebe-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="c7ebe-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-257">Дескриптор окна</span><span class="sxs-lookup"><span data-stu-id="c7ebe-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="c7ebe-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7ebe-259">**Свойства динамической набора записей**</span><span class="sxs-lookup"><span data-stu-id="c7ebe-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="c7ebe-260">Обратите внимание, что **Динамические свойства** объекта **набора записей** выйдет из области действия (становятся недоступными) при закрытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c7ebe-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7ebe-261">Имя свойства ADO</span><span class="sxs-lookup"><span data-stu-id="c7ebe-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="c7ebe-262">Имя свойства OLE DB</span><span class="sxs-lookup"><span data-stu-id="c7ebe-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="c7ebe-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="c7ebe-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-266">(1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="c7ebe-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="c7ebe-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="c7ebe-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="c7ebe-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-274">(1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="c7ebe-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="c7ebe-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="c7ebe-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="c7ebe-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-282">(1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="c7ebe-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="c7ebe-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-286">(1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="c7ebe-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="c7ebe-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="c7ebe-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="c7ebe-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="c7ebe-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="c7ebe-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-298">(1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="c7ebe-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="c7ebe-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="c7ebe-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="c7ebe-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="c7ebe-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="c7ebe-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-311">IStream</span><span class="sxs-lookup"><span data-stu-id="c7ebe-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c7ebe-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-315">Порядок доступа</span><span class="sxs-lookup"><span data-stu-id="c7ebe-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="c7ebe-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-317">Только для добавления строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-319">Обработка асинхронных строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="c7ebe-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-321">Автоматическое обновление ссылок</span><span class="sxs-lookup"><span data-stu-id="c7ebe-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="c7ebe-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-323">Размер выборки фона</span><span class="sxs-lookup"><span data-stu-id="c7ebe-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-325">Приоритет потока фона</span><span class="sxs-lookup"><span data-stu-id="c7ebe-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-327">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="c7ebe-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-329">Блокировка объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="c7ebe-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-331">Тип закладки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="c7ebe-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-335">Упорядоченные закладки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-337">Кэш дочерних строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-339">Кэш отложенной столбцов</span><span class="sxs-lookup"><span data-stu-id="c7ebe-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="c7ebe-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-341">Изменение вставленных строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-343">Права доступа столбца</span><span class="sxs-lookup"><span data-stu-id="c7ebe-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-345">Столбец набор уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="c7ebe-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-347">Столбец для записи</span><span class="sxs-lookup"><span data-stu-id="c7ebe-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="c7ebe-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-349">Время ожидания команды</span><span class="sxs-lookup"><span data-stu-id="c7ebe-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-351">Версия модуля текущей позиции</span><span class="sxs-lookup"><span data-stu-id="c7ebe-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="c7ebe-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-353">Отложите столбца</span><span class="sxs-lookup"><span data-stu-id="c7ebe-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="c7ebe-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-355">Отложенное обновление объекта хранения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-357">Выборку</span><span class="sxs-lookup"><span data-stu-id="c7ebe-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-359">Операции фильтрации</span><span class="sxs-lookup"><span data-stu-id="c7ebe-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-361">Найдите операций</span><span class="sxs-lookup"><span data-stu-id="c7ebe-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-363">Скрытые столбцы (количество)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-365">Хранение строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-367">Немобильные строки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-369">Размер начальной выборки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-371">Литерал закладки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-373">Удостоверение литерала строки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-375">Обслуживание изменений состояния</span><span class="sxs-lookup"><span data-stu-id="c7ebe-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-377">Максимальное число открытых строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-379">Максимум ожидающие строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-381">Максимальное число строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-383">Использование памяти</span><span class="sxs-lookup"><span data-stu-id="c7ebe-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-384">ОПРЕДЕЛЕН</span><span class="sxs-lookup"><span data-stu-id="c7ebe-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-385">Степень детализации уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-387">Этапы уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="c7ebe-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-389">Объекты в транзакции</span><span class="sxs-lookup"><span data-stu-id="c7ebe-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-391">Видны прочие изменения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-393">Других пользователей вставки видимым</span><span class="sxs-lookup"><span data-stu-id="c7ebe-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-395">Видны собственные изменения</span><span class="sxs-lookup"><span data-stu-id="c7ebe-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-397">Видны собственные операции вставки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-399">Сохранять при аварийном завершении</span><span class="sxs-lookup"><span data-stu-id="c7ebe-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-401">Сохранять при фиксации</span><span class="sxs-lookup"><span data-stu-id="c7ebe-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-403">Private1</span><span class="sxs-lookup"><span data-stu-id="c7ebe-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-404">(5)</span><span class="sxs-lookup"><span data-stu-id="c7ebe-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-405">Быстрый перезапуск</span><span class="sxs-lookup"><span data-stu-id="c7ebe-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="c7ebe-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-407">Повторные события</span><span class="sxs-lookup"><span data-stu-id="c7ebe-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-409">Удаление удаленных строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="c7ebe-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-411">Сообщить о нескольких изменений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c7ebe-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-413">Изменить форму имя</span><span class="sxs-lookup"><span data-stu-id="c7ebe-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="c7ebe-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-415">Команда синхронизации</span><span class="sxs-lookup"><span data-stu-id="c7ebe-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c7ebe-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-417">Вернуть ожидающие вставки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-419">Удалить строку уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-421">Строка первого уведомления об изменении</span><span class="sxs-lookup"><span data-stu-id="c7ebe-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-423">Строка вставки уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-425">Привилегии строки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-427">Уведомления о повторной синхронизации строки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="c7ebe-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-429">Строка, потоковой модели</span><span class="sxs-lookup"><span data-stu-id="c7ebe-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="c7ebe-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-431">Уведомление об изменении отмены строки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-433">Строка отмены Delete уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-435">Вставка отмены строки уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="c7ebe-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-437">Уведомление об обновлении строки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-439">Уведомление об изменении положения строк выборки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-441">Уведомление о выпуске набора строк</span><span class="sxs-lookup"><span data-stu-id="c7ebe-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-443">Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="c7ebe-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-445">Серверный курсор</span><span class="sxs-lookup"><span data-stu-id="c7ebe-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="c7ebe-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-447">Пропустить удаленных закладки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="c7ebe-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-449">Строка строгого удостоверений</span><span class="sxs-lookup"><span data-stu-id="c7ebe-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-451">Уникальный каталога</span><span class="sxs-lookup"><span data-stu-id="c7ebe-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="c7ebe-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-453">Уникальные строки</span><span class="sxs-lookup"><span data-stu-id="c7ebe-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-455">Уникальный схемы</span><span class="sxs-lookup"><span data-stu-id="c7ebe-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="c7ebe-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-457">Уникальная таблица</span><span class="sxs-lookup"><span data-stu-id="c7ebe-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="c7ebe-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-459">Возможности обновления</span><span class="sxs-lookup"><span data-stu-id="c7ebe-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="c7ebe-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-461">Обновление критериев</span><span class="sxs-lookup"><span data-stu-id="c7ebe-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="c7ebe-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7ebe-463">Обновление повторной синхронизации</span><span class="sxs-lookup"><span data-stu-id="c7ebe-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="c7ebe-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7ebe-465">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="c7ebe-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="c7ebe-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c7ebe-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

