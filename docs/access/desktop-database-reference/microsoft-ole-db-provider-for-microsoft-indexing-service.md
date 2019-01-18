---
title: Поставщик Microsoft OLE DB для службы индексирования (Майкрософт)
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba27bfdf6cc1317b441e626c61784e2c50b589f1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716610"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="3cff9-102">Поставщик Microsoft OLE DB для службы индексирования (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="3cff9-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="3cff9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cff9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cff9-104">Поставщик Microsoft OLE DB для служб индексирования Microsoft позволяет получать доступ только для чтения к файловой системы и веб-данных, службой индексирования Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3cff9-104">The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="3cff9-105">ADO приложений можно выполнять запросы SQL для извлечения сведений содержимое и файлы.</span><span class="sxs-lookup"><span data-stu-id="3cff9-105">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>

<span data-ttu-id="3cff9-106">Поставщик свободных потоков и Юникод.</span><span class="sxs-lookup"><span data-stu-id="3cff9-106">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="3cff9-107">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="3cff9-107">Connection String Parameters</span></span>

<span data-ttu-id="3cff9-108">Для подключения к данным поставщиком, задайте **поставщика =** аргумент свойства [ConnectionString](connectionstring-property-ado.md) для:</span><span class="sxs-lookup"><span data-stu-id="3cff9-108">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="3cff9-109">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="3cff9-109">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="3cff9-110">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="3cff9-110">Typical Connection String</span></span>

<span data-ttu-id="3cff9-111">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="3cff9-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="3cff9-112">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="3cff9-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cff9-113">Keyword</span><span class="sxs-lookup"><span data-stu-id="3cff9-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="3cff9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3cff9-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-115"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="3cff9-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="3cff9-116">Задает поставщика OLE DB для службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="3cff9-116">Specifies the OLE DB Provider for Microsoft Indexing Service.</span></span> <span data-ttu-id="3cff9-117">Обычно это единственный ключевого слова, указанного в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="3cff9-117">Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-118"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="3cff9-118"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="3cff9-119">Задает имя каталога службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="3cff9-119">Specifies the Indexing Service catalog name.</span></span> <span data-ttu-id="3cff9-120">Если это ключевое слово не указан, используется каталог системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3cff9-120">If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-121"><strong>Идентификатор языка</strong></span><span class="sxs-lookup"><span data-stu-id="3cff9-121"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="3cff9-122">Число уникальных 32-разрядная версия (например, 1033), который указывает параметры, связанные с языком пользователя.</span><span class="sxs-lookup"><span data-stu-id="3cff9-122">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language.</span></span> <span data-ttu-id="3cff9-123">Эти параметры указывают способ форматирования даты и времени, элементы сортируются в алфавитном порядке, строк сравниваются и т. д.</span><span class="sxs-lookup"><span data-stu-id="3cff9-123">These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span> <span data-ttu-id="3cff9-124">Если это ключевое слово не указан, используется идентификатор языкового стандарта системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3cff9-124">If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="3cff9-125">Текст команды</span><span class="sxs-lookup"><span data-stu-id="3cff9-125">Command Text</span></span>

<span data-ttu-id="3cff9-126">Синтаксис запроса SQL службы индексирования состоит из расширения инструкции SQL-92 **ВЫБЕРИТЕ** и его **ОТПРАВИТЕЛЯ** и **ГДЕ** предложений.</span><span class="sxs-lookup"><span data-stu-id="3cff9-126">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses.</span></span> <span data-ttu-id="3cff9-127">Результаты запроса возвращаются через строк OLE DB, который может использоваться с ADO и управлять как объекты [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3cff9-127">The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="3cff9-128">Поиск точного слова или фразы или использовать подстановочные знаки для поиска шаблонов или основам слов.</span><span class="sxs-lookup"><span data-stu-id="3cff9-128">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words.</span></span> <span data-ttu-id="3cff9-129">Логика поиска может быть основана на логическое решения, Средневзвешенное термины или всего к другим слова.</span><span class="sxs-lookup"><span data-stu-id="3cff9-129">The search logic can be based on Boolean decisions, weighted terms, or proximity to other words.</span></span> <span data-ttu-id="3cff9-130">Также можно выполнить поиск по «бесплатную текст», который находит совпадений на основе значения, а не точное слова.</span><span class="sxs-lookup"><span data-stu-id="3cff9-130">You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="3cff9-131">Поставщик не принимает вызовы хранимых процедур или простой таблице имен (например, для свойства [CommandType](commandtype-property-ado.md) всегда будет **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="3cff9-131">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="3cff9-132">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="3cff9-132">Recordset Behavior</span></span>

<span data-ttu-id="3cff9-133">В следующей таблице перечислены функции, доступные с объектом **набора записей** , открытых с этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3cff9-133">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="3cff9-134">Доступен только тип статический курсор (**adOpenStatic**).</span><span class="sxs-lookup"><span data-stu-id="3cff9-134">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="3cff9-135">Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции [свойств](properties-collection-ado.md) **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="3cff9-135">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="3cff9-136">Доступность стандартными свойствами ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="3cff9-136">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cff9-137">Свойство</span><span class="sxs-lookup"><span data-stu-id="3cff9-137">Property</span></span></p></th>
<th><p><span data-ttu-id="3cff9-138">Availability</span><span class="sxs-lookup"><span data-stu-id="3cff9-138">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-140">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-140">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-142">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-142">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-144">только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cff9-144">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-145"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-145"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-146">только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cff9-146">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-147"><a href="bookmark-property-ado.md">Закладка</a>\*</span><span class="sxs-lookup"><span data-stu-id="3cff9-147"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="3cff9-148">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-148">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-149"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-149"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-150">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-150">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-152">всегда <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="3cff9-152">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-153"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-153"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-154">всегда <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="3cff9-154">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-155"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-155"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-156">всегда <strong>как таковые</strong></span><span class="sxs-lookup"><span data-stu-id="3cff9-156">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-157"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-157"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-158">только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cff9-158">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-159"><a href="filter-property-ado.md">Фильтр</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-159"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-160">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-160">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-161"><a href="locktype-property-ado.md">LockType для</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-161"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-162">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-162">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-164">Недоступен</span><span class="sxs-lookup"><span data-stu-id="3cff9-164">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-166">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-166">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-167"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-167"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-168">только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cff9-168">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-169"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-169"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-170">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-170">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-171"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-171"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-172">только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cff9-172">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-173"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-173"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-174">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3cff9-174">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-175"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-175"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-176">только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cff9-176">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-177"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-177"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-178">только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cff9-178">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3cff9-179">\*Закладки должна быть включена в поставщика в порядке для этой функции существует во **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="3cff9-179">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="3cff9-180">Доступность стандартных способов ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="3cff9-180">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cff9-181">Method</span><span class="sxs-lookup"><span data-stu-id="3cff9-181">Method</span></span></p></th>
<th><p><span data-ttu-id="3cff9-182">Доступные?</span><span class="sxs-lookup"><span data-stu-id="3cff9-182">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-183"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-183"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-184">Нет</span><span class="sxs-lookup"><span data-stu-id="3cff9-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-185"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-185"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-186">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-188">Нет</span><span class="sxs-lookup"><span data-stu-id="3cff9-188">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-190">Нет</span><span class="sxs-lookup"><span data-stu-id="3cff9-190">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-191"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-191"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-192">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-192">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-193"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-193"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-194">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-194">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-195"><a href="delete-method-ado-recordset.md">удаление</a>;</span><span class="sxs-lookup"><span data-stu-id="3cff9-195"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-196">Нет</span><span class="sxs-lookup"><span data-stu-id="3cff9-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-197"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-197"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-198">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-199"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-199"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-200">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-200">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-202">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-202">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-204">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-205"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-205"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-206">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-207"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-207"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-208">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-208">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-209"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-209"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-210">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-211"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-211"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-212">Да</span><span class="sxs-lookup"><span data-stu-id="3cff9-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cff9-213"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="3cff9-213"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-214">Нет</span><span class="sxs-lookup"><span data-stu-id="3cff9-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cff9-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="3cff9-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="3cff9-216">Нет</span><span class="sxs-lookup"><span data-stu-id="3cff9-216">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3cff9-217">См. также</span><span class="sxs-lookup"><span data-stu-id="3cff9-217">See also</span></span>

<span data-ttu-id="3cff9-218">Сведения о реализации и функциональным сведения о поставщик Microsoft OLE DB для служб индексирования Microsoft обратитесь к Microsoft OLE DB Справочник программиста.</span><span class="sxs-lookup"><span data-stu-id="3cff9-218">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

