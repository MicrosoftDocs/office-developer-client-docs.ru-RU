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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288920"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="a79f1-102">Поставщик Microsoft OLE DB для службы индексирования (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="a79f1-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="a79f1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a79f1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a79f1-104">Поставщик microsoft OLE DB для службы индексации Майкрософт предоставляет программный доступ только для чтения к файловой системе и веб-данным, индексациям с помощью службы индексации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a79f1-104">The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="a79f1-105">Приложения ADO могут SQL запросы для получения сведений о свойстве контента и файлов.</span><span class="sxs-lookup"><span data-stu-id="a79f1-105">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>

<span data-ttu-id="a79f1-106">Поставщик имеет свободный поток и включен юникод.</span><span class="sxs-lookup"><span data-stu-id="a79f1-106">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="a79f1-107">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="a79f1-107">Connection String Parameters</span></span>

<span data-ttu-id="a79f1-108">Чтобы подключиться к этому поставщику, установите **аргумент Provider=** для свойства [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="a79f1-108">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="a79f1-109">Чтение свойства [Provider](provider-property-ado.md) также вернет эту строку.</span><span class="sxs-lookup"><span data-stu-id="a79f1-109">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="a79f1-110">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="a79f1-110">Typical Connection String</span></span>

<span data-ttu-id="a79f1-111">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="a79f1-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="a79f1-112">Строка состоит из этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="a79f1-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a79f1-113">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="a79f1-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="a79f1-114">Description</span><span class="sxs-lookup"><span data-stu-id="a79f1-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-115"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="a79f1-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="a79f1-116">Указывает поставщика OLE DB для службы индексации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a79f1-116">Specifies the OLE DB Provider for Microsoft Indexing Service.</span></span> <span data-ttu-id="a79f1-117">Обычно это единственное ключевое слово, указанное в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="a79f1-117">Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-118"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="a79f1-118"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="a79f1-119">Указывает имя каталога службы индексации.</span><span class="sxs-lookup"><span data-stu-id="a79f1-119">Specifies the Indexing Service catalog name.</span></span> <span data-ttu-id="a79f1-120">Если это ключевое слово не указано, используется каталог системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a79f1-120">If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-121"><strong>Идентификатор locale</strong></span><span class="sxs-lookup"><span data-stu-id="a79f1-121"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="a79f1-122">Указывает уникальный 32-битный номер (например, 1033), который указывает предпочтения, связанные с языком пользователя.</span><span class="sxs-lookup"><span data-stu-id="a79f1-122">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language.</span></span> <span data-ttu-id="a79f1-123">Эти параметры указывают форматирование дат и времени, сортировку элементов в алфавитном порядке, сравнение строк и так далее.</span><span class="sxs-lookup"><span data-stu-id="a79f1-123">These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span> <span data-ttu-id="a79f1-124">Если это ключевое слово не указано, используется идентификатор локального значения системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a79f1-124">If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="a79f1-125">Командный текст</span><span class="sxs-lookup"><span data-stu-id="a79f1-125">Command Text</span></span>

<span data-ttu-id="a79f1-126">Синтаксис SQL службы индексации состоит из расширений для утверждения SELECT SQL-92  и его положений FROM **и** **WHERE.**</span><span class="sxs-lookup"><span data-stu-id="a79f1-126">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses.</span></span> <span data-ttu-id="a79f1-127">Результаты запроса возвращаются с помощью строк OLE DB, которые могут потребляться ADO и манипулировать как [объекты Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="a79f1-127">The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="a79f1-128">Вы можете искать точные слова или фразы или использовать подкарды для поиска шаблонов или стеблей слов.</span><span class="sxs-lookup"><span data-stu-id="a79f1-128">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words.</span></span> <span data-ttu-id="a79f1-129">Логика поиска может основываться на решениях boolean, взвешеных терминах или близости к другим словам.</span><span class="sxs-lookup"><span data-stu-id="a79f1-129">The search logic can be based on Boolean decisions, weighted terms, or proximity to other words.</span></span> <span data-ttu-id="a79f1-130">Вы также можете искать по "свободному тексту", который находит совпадения на основе значения, а не точных слов.</span><span class="sxs-lookup"><span data-stu-id="a79f1-130">You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="a79f1-131">Поставщик не принимает сохраненные вызовы процедур или простые имена таблиц (например, свойство [CommandType](commandtype-property-ado.md) всегда **будет adCmdText).**</span><span class="sxs-lookup"><span data-stu-id="a79f1-131">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="a79f1-132">Поведение наборов записей</span><span class="sxs-lookup"><span data-stu-id="a79f1-132">Recordset Behavior</span></span>

<span data-ttu-id="a79f1-133">В следующих таблицах перечислить функции, доступные с **объектом Recordset,** открытым с помощью этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="a79f1-133">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="a79f1-134">Доступен только тип статического курсора **(adOpenStatic).**</span><span class="sxs-lookup"><span data-stu-id="a79f1-134">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="a79f1-135">Дополнительные сведения о поведении **Recordset** для конфигурации поставщика запустите метод [Supports](supports-method-ado.md) и введите коллекцию [Свойств](properties-collection-ado.md) в **наборе Recordset,** чтобы определить, присутствуют ли динамические свойства конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="a79f1-135">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="a79f1-136">Доступность стандартных свойств ADO **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="a79f1-136">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a79f1-137">Свойство</span><span class="sxs-lookup"><span data-stu-id="a79f1-137">Property</span></span></p></th>
<th><p><span data-ttu-id="a79f1-138">Доступность</span><span class="sxs-lookup"><span data-stu-id="a79f1-138">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-140">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-140">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-142">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-142">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-144">read-only</span><span class="sxs-lookup"><span data-stu-id="a79f1-144">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-145"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-145"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-146">read-only</span><span class="sxs-lookup"><span data-stu-id="a79f1-146">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-147"><a href="bookmark-property-ado.md">Закладка</a>\*</span><span class="sxs-lookup"><span data-stu-id="a79f1-147"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="a79f1-148">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-148">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-149"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-149"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-150">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-150">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-152">всегда <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="a79f1-152">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-153"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-153"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-154">всегда <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="a79f1-154">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-155"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-155"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-156">всегда <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="a79f1-156">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-157"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-157"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-158">read-only</span><span class="sxs-lookup"><span data-stu-id="a79f1-158">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-159"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-159"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-160">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-160">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-161"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-161"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-162">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-162">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-164">недоступен</span><span class="sxs-lookup"><span data-stu-id="a79f1-164">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-166">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-166">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-167"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-167"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-168">read-only</span><span class="sxs-lookup"><span data-stu-id="a79f1-168">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-169"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-169"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-170">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-170">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-171"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-171"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-172">read-only</span><span class="sxs-lookup"><span data-stu-id="a79f1-172">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-173"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-173"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-174">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="a79f1-174">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-175"><a href="state-property-ado.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-175"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-176">read-only</span><span class="sxs-lookup"><span data-stu-id="a79f1-176">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-177"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-177"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-178">read-only</span><span class="sxs-lookup"><span data-stu-id="a79f1-178">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a79f1-179">\*Закладки должны быть включены в поставщике, чтобы эта функция существовала в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="a79f1-179">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="a79f1-180">Доступность стандартных методов ADO **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="a79f1-180">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a79f1-181">Метод</span><span class="sxs-lookup"><span data-stu-id="a79f1-181">Method</span></span></p></th>
<th><p><span data-ttu-id="a79f1-182">Доступно?</span><span class="sxs-lookup"><span data-stu-id="a79f1-182">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-183"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-183"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-184">Нет</span><span class="sxs-lookup"><span data-stu-id="a79f1-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-185"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-185"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-186">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-188">Нет</span><span class="sxs-lookup"><span data-stu-id="a79f1-188">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-190">Нет</span><span class="sxs-lookup"><span data-stu-id="a79f1-190">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-191"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-191"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-192">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-192">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-193"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-193"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-194">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-194">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-195"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-195"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-196">Нет</span><span class="sxs-lookup"><span data-stu-id="a79f1-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-197"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-197"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-198">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-199"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-199"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-200">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-200">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-202">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-202">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-204">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-205"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-205"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-206">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-207"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-207"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-208">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-208">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-209"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-209"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-210">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-211"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-211"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-212">Да</span><span class="sxs-lookup"><span data-stu-id="a79f1-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a79f1-213"><a href="update-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-213"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-214">Нет</span><span class="sxs-lookup"><span data-stu-id="a79f1-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a79f1-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="a79f1-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a79f1-216">Нет</span><span class="sxs-lookup"><span data-stu-id="a79f1-216">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a79f1-217">См. также</span><span class="sxs-lookup"><span data-stu-id="a79f1-217">See also</span></span>

<span data-ttu-id="a79f1-218">Подробные сведения о реализации и функциональные сведения о поставщике microsoft OLE DB для службы индексации Майкрософт обратитесь в справочную службу программиста Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a79f1-218">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

