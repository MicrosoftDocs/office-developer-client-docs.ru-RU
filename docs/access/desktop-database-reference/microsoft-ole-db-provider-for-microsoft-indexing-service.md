---
title: Microsoft OLE DB Provider for Microsoft Indexing Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e41633ddb2730af66ddeee400ad035d5a17ed90d
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607055"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="f31f7-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span><span class="sxs-lookup"><span data-stu-id="f31f7-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="f31f7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f31f7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f31f7-104"><<<<<<< HEAD поставщик Microsoft OLE DB для службы индексирования Майкрософт предоставляет программный доступ только для чтения к файловой системе и данных веб-службой индексирования Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f31f7-104"><<<<<<< HEAD The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and Web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="f31f7-105">ADO приложений можно выполнять запросы SQL для извлечения сведений содержимое и файлы.</span><span class="sxs-lookup"><span data-stu-id="f31f7-105">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>
<span data-ttu-id="f31f7-106">=== Microsoft поставщика OLE DB для служб индексирования Microsoft позволяет получать доступ только для чтения к файловой системы и веб-данных, службой индексирования Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f31f7-106">======= The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="f31f7-107">ADO приложений можно выполнять запросы SQL для извлечения сведений содержимое и файлы.</span><span class="sxs-lookup"><span data-stu-id="f31f7-107">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>
>>>>>>> <span data-ttu-id="f31f7-108">master</span><span class="sxs-lookup"><span data-stu-id="f31f7-108">master</span></span>

<span data-ttu-id="f31f7-109">Поставщик свободных потоков и Юникод.</span><span class="sxs-lookup"><span data-stu-id="f31f7-109">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="f31f7-110">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="f31f7-110">Connection String Parameters</span></span>

<span data-ttu-id="f31f7-111">Для подключения к данным поставщиком, задайте **поставщика =** аргумент свойства [ConnectionString](connectionstring-property-ado.md) для:</span><span class="sxs-lookup"><span data-stu-id="f31f7-111">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="f31f7-112">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="f31f7-112">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="f31f7-113">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="f31f7-113">Typical Connection String</span></span>

<span data-ttu-id="f31f7-114">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="f31f7-114">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="f31f7-115">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="f31f7-115">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f31f7-116">Keyword</span><span class="sxs-lookup"><span data-stu-id="f31f7-116">Keyword</span></span></p></th>
<th><p><span data-ttu-id="f31f7-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f31f7-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-118"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="f31f7-118"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="f31f7-119">Задает поставщика OLE DB для службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="f31f7-119">Specifies the OLE DB Provider for Microsoft Indexing Service.</span></span> <span data-ttu-id="f31f7-120">Обычно это единственный ключевого слова, указанного в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="f31f7-120">Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-121"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="f31f7-121"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="f31f7-122">Задает имя каталога службы индексирования.</span><span class="sxs-lookup"><span data-stu-id="f31f7-122">Specifies the Indexing Service catalog name.</span></span> <span data-ttu-id="f31f7-123">Если это ключевое слово не указан, используется каталог системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f31f7-123">If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-124"><strong>Идентификатор языка</strong></span><span class="sxs-lookup"><span data-stu-id="f31f7-124"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="f31f7-125">Число уникальных 32-разрядная версия (например, 1033), который указывает параметры, связанные с языком пользователя.</span><span class="sxs-lookup"><span data-stu-id="f31f7-125">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language.</span></span> <span data-ttu-id="f31f7-126">Эти параметры указывают способ форматирования даты и времени, элементы сортируются в алфавитном порядке, строк сравниваются и т. д.</span><span class="sxs-lookup"><span data-stu-id="f31f7-126">These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span> <span data-ttu-id="f31f7-127">Если это ключевое слово не указан, используется идентификатор языкового стандарта системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f31f7-127">If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="f31f7-128">Текст команды</span><span class="sxs-lookup"><span data-stu-id="f31f7-128">Command Text</span></span>

<span data-ttu-id="f31f7-129">Синтаксис запроса SQL службы индексирования состоит из расширения инструкции SQL-92 **ВЫБЕРИТЕ** и его **ОТПРАВИТЕЛЯ** и **ГДЕ** предложений.</span><span class="sxs-lookup"><span data-stu-id="f31f7-129">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses.</span></span> <span data-ttu-id="f31f7-130">Результаты запроса возвращаются через строк OLE DB, который может использоваться с ADO и управлять как объекты [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f31f7-130">The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="f31f7-131">Поиск точного слова или фразы или использовать подстановочные знаки для поиска шаблонов или основам слов.</span><span class="sxs-lookup"><span data-stu-id="f31f7-131">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words.</span></span> <span data-ttu-id="f31f7-132">Логика поиска может быть основана на логическое решения, Средневзвешенное термины или всего к другим слова.</span><span class="sxs-lookup"><span data-stu-id="f31f7-132">The search logic can be based on Boolean decisions, weighted terms, or proximity to other words.</span></span> <span data-ttu-id="f31f7-133">Также можно выполнить поиск по «бесплатную текст», который находит совпадений на основе значения, а не точное слова.</span><span class="sxs-lookup"><span data-stu-id="f31f7-133">You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="f31f7-134">Поставщик не принимает вызовы хранимых процедур или простой таблице имен (например, для свойства [CommandType](commandtype-property-ado.md) всегда будет **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="f31f7-134">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="f31f7-135">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="f31f7-135">Recordset Behavior</span></span>

<span data-ttu-id="f31f7-136">В следующей таблице перечислены функции, доступные с объектом **набора записей** , открытых с этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f31f7-136">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="f31f7-137">Доступен только тип статический курсор (**adOpenStatic**).</span><span class="sxs-lookup"><span data-stu-id="f31f7-137">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="f31f7-138">Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции [свойств](properties-collection-ado.md) **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="f31f7-138">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="f31f7-139">Доступность стандартными свойствами ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="f31f7-139">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f31f7-140">Свойство</span><span class="sxs-lookup"><span data-stu-id="f31f7-140">Property</span></span></p></th>
<th><p><span data-ttu-id="f31f7-141">Availability</span><span class="sxs-lookup"><span data-stu-id="f31f7-141">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-142"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-142"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-143">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-143">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-144"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-144"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-145">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-145">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-146"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-146"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-147">только для чтения</span><span class="sxs-lookup"><span data-stu-id="f31f7-147">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-148"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-148"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-149">только для чтения</span><span class="sxs-lookup"><span data-stu-id="f31f7-149">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-150"><a href="bookmark-property-ado.md">Закладка</a>\*</span><span class="sxs-lookup"><span data-stu-id="f31f7-150"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="f31f7-151">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-151">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-152"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-152"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-153">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-153">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-154"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-154"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-155">всегда <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="f31f7-155">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-156"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-156"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-157">всегда <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="f31f7-157">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-158"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-158"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-159">всегда <strong>как таковые</strong></span><span class="sxs-lookup"><span data-stu-id="f31f7-159">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-160"><a href="bof-eof-properties-ado.md">ФУНКЦИЯ EOF</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-160"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-161">только для чтения</span><span class="sxs-lookup"><span data-stu-id="f31f7-161">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-162"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-162"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-163">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-163">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-164"><a href="locktype-property-ado.md">LockType для</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-164"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-165">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-165">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-166"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-166"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-167">Недоступен</span><span class="sxs-lookup"><span data-stu-id="f31f7-167">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-168"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-168"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-169">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-169">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-170"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-170"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-171">только для чтения</span><span class="sxs-lookup"><span data-stu-id="f31f7-171">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-172"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-172"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-173">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-173">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-174"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-174"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-175">только для чтения</span><span class="sxs-lookup"><span data-stu-id="f31f7-175">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-176"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-176"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-177">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f31f7-177">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-178"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-178"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-179">только для чтения</span><span class="sxs-lookup"><span data-stu-id="f31f7-179">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-180"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-180"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-181">только для чтения</span><span class="sxs-lookup"><span data-stu-id="f31f7-181">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f31f7-182">\*Закладки должна быть включена в поставщика в порядке для этой функции существует во **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="f31f7-182">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="f31f7-183">Доступность стандартных способов ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="f31f7-183">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f31f7-184">Метод</span><span class="sxs-lookup"><span data-stu-id="f31f7-184">Method</span></span></p></th>
<th><p><span data-ttu-id="f31f7-185">Доступные?</span><span class="sxs-lookup"><span data-stu-id="f31f7-185">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-186"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-186"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-187">Нет</span><span class="sxs-lookup"><span data-stu-id="f31f7-187">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-188"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-188"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-189">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-189">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-190"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-190"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-191">Нет</span><span class="sxs-lookup"><span data-stu-id="f31f7-191">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-192"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-192"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-193">Нет</span><span class="sxs-lookup"><span data-stu-id="f31f7-193">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-194"><a href="clone-method-ado.md">Копия</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-194"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-195">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-195">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-196"><a href="close-method-ado.md">Закрыть</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-196"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-197">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-197">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-198"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-198"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-199">Нет</span><span class="sxs-lookup"><span data-stu-id="f31f7-199">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-200"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-200"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-201">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-201">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-202"><a href="move-method-ado.md">Перемещение</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-202"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-203">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-204"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-204"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-205">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-206"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-206"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-207">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-207">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-208"><a href="open-method-ado-recordset.md">Открытие</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-208"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-209">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-209">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-210"><a href="requery-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-210"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-211">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-211">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-212"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-212"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-213">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-213">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-214"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-214"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-215">Да</span><span class="sxs-lookup"><span data-stu-id="f31f7-215">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31f7-216"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="f31f7-216"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-217">Нет</span><span class="sxs-lookup"><span data-stu-id="f31f7-217">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31f7-218"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="f31f7-218"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="f31f7-219">Нет</span><span class="sxs-lookup"><span data-stu-id="f31f7-219">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f31f7-220">См. также</span><span class="sxs-lookup"><span data-stu-id="f31f7-220">See also</span></span>

<span data-ttu-id="f31f7-221">Сведения о реализации и функциональным сведения о поставщик Microsoft OLE DB для служб индексирования Microsoft обратитесь к Microsoft OLE DB Справочник программиста.</span><span class="sxs-lookup"><span data-stu-id="f31f7-221">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

