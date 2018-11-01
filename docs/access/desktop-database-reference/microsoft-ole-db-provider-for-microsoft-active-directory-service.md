---
title: Поставщик Microsoft OLE DB для службы Microsoft Active Directory
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1555883ef8305225d6ddd1969d98de082288a6b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887539"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="53a6b-102">Поставщик Microsoft OLE DB для службы Microsoft Active Directory</span><span class="sxs-lookup"><span data-stu-id="53a6b-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="53a6b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53a6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53a6b-104">Поставщик Microsoft служб Active Directory интерфейсы (ADSI) позволяет ADO для подключения к службам каталогов разнородных через ADSI.</span><span class="sxs-lookup"><span data-stu-id="53a6b-104">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI.</span></span> <span data-ttu-id="53a6b-105">Это позволяет приложений ADO доступ только для чтения к Microsoft Windows NT 4.0 и Microsoft Windows 2000 службы каталогов, в дополнение к любой LDAP-совместимый службы каталогов и Novell Directory Services.</span><span class="sxs-lookup"><span data-stu-id="53a6b-105">This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services.</span></span> <span data-ttu-id="53a6b-106">ADSI самого основана на модели поставщика, поэтому в случае нового поставщика, предоставляющая доступ к другой каталог приложений ADO смогут бесперебойно получать доступ к нему.</span><span class="sxs-lookup"><span data-stu-id="53a6b-106">ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly.</span></span> <span data-ttu-id="53a6b-107">Поставщик ADSI свободных потоков и Юникод.</span><span class="sxs-lookup"><span data-stu-id="53a6b-107">The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="53a6b-108">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="53a6b-108">Connection String Parameters</span></span>

<span data-ttu-id="53a6b-109">Для подключения к данным поставщиком, задайте для свойства [ConnectionString](connectionstring-property-ado.md) для аргумента **поставщика** :</span><span class="sxs-lookup"><span data-stu-id="53a6b-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="53a6b-110">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="53a6b-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="53a6b-111">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="53a6b-111">Typical Connection String</span></span>

<span data-ttu-id="53a6b-112">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="53a6b-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="53a6b-113">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="53a6b-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53a6b-114">Keyword</span><span class="sxs-lookup"><span data-stu-id="53a6b-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="53a6b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="53a6b-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-116"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="53a6b-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="53a6b-117">Задает поставщика OLE DB для служб Microsoft Active Directory.</span><span class="sxs-lookup"><span data-stu-id="53a6b-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-118"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="53a6b-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="53a6b-119">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="53a6b-119">Specifies the user name.</span></span> <span data-ttu-id="53a6b-120">Если это ключевое слово задан, используется данный момент в систему.</span><span class="sxs-lookup"><span data-stu-id="53a6b-120">If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="53a6b-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="53a6b-122">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="53a6b-122">Specifies the user password.</span></span> <span data-ttu-id="53a6b-123">Если это ключевое слово задан, используется данный момент в систему.</span><span class="sxs-lookup"><span data-stu-id="53a6b-123">If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="53a6b-124">**Текст команды**</span><span class="sxs-lookup"><span data-stu-id="53a6b-124">**Command Text**</span></span>

<span data-ttu-id="53a6b-125">Текстовая строка из четырех частей команду распознается поставщика в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="53a6b-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53a6b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="53a6b-126">Value</span></span></p></th>
<th><p><span data-ttu-id="53a6b-127">Описание</span><span class="sxs-lookup"><span data-stu-id="53a6b-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-128"><em>Root</em></span><span class="sxs-lookup"><span data-stu-id="53a6b-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="53a6b-129">Указывает объект <strong>путь</strong> , с которого следует начинать поиск (то есть, корень поиска).</span><span class="sxs-lookup"><span data-stu-id="53a6b-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-130"><em>Filter</em></span><span class="sxs-lookup"><span data-stu-id="53a6b-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="53a6b-131">Указывает фильтр поиска в формате RFC 1960.</span><span class="sxs-lookup"><span data-stu-id="53a6b-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-132"><em>Атрибуты</em></span><span class="sxs-lookup"><span data-stu-id="53a6b-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="53a6b-133">Указывает, разделенный запятыми список атрибутов должно быть возвращено.</span><span class="sxs-lookup"><span data-stu-id="53a6b-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-134"><em>Область</em></span><span class="sxs-lookup"><span data-stu-id="53a6b-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="53a6b-135">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="53a6b-135">Optional.</span></span> <span data-ttu-id="53a6b-136"><strong>Строка</strong> , которая определяет область поиска.</span><span class="sxs-lookup"><span data-stu-id="53a6b-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="53a6b-137">Может иметь одно из следующих значений: базовый — поиск только базового объекта (корень поиска).</span><span class="sxs-lookup"><span data-stu-id="53a6b-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="53a6b-138">OneLevel — Поиск только один уровень.</span><span class="sxs-lookup"><span data-stu-id="53a6b-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="53a6b-139">Поддерево — Поиск поддерево.</span><span class="sxs-lookup"><span data-stu-id="53a6b-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="53a6b-140">Пример:</span><span class="sxs-lookup"><span data-stu-id="53a6b-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="53a6b-141">Поставщик также поддерживает SQL SELECT текст команды.</span><span class="sxs-lookup"><span data-stu-id="53a6b-141">The provider also supports SQL SELECT for command text.</span></span> <span data-ttu-id="53a6b-142">Пример:</span><span class="sxs-lookup"><span data-stu-id="53a6b-142">For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="53a6b-143">Поставщик не принимает вызовы хранимых процедур или простой таблице имен (например, для свойства [CommandType](commandtype-property-ado.md) всегда будет **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="53a6b-143">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span> <span data-ttu-id="53a6b-144">Обратитесь к документации интерфейсы службы Active Directory для более полное описание элементов текста команды.</span><span class="sxs-lookup"><span data-stu-id="53a6b-144">See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="53a6b-145">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="53a6b-145">Recordset Behavior</span></span>

<span data-ttu-id="53a6b-146">В следующей таблице перечислены функции, доступные для объекта [набора записей](recordset-object-ado.md) , открытых с этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="53a6b-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="53a6b-147">Доступен только тип статический курсор (**adOpenStatic**).</span><span class="sxs-lookup"><span data-stu-id="53a6b-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="53a6b-148">Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции [свойств](properties-collection-ado.md) **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="53a6b-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="53a6b-149">Доступность стандартными свойствами ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="53a6b-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53a6b-150">Свойство</span><span class="sxs-lookup"><span data-stu-id="53a6b-150">Property</span></span></p></th>
<th><p><span data-ttu-id="53a6b-151">Availability</span><span class="sxs-lookup"><span data-stu-id="53a6b-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-153">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-155">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-157">только для чтения</span><span class="sxs-lookup"><span data-stu-id="53a6b-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-159">только для чтения</span><span class="sxs-lookup"><span data-stu-id="53a6b-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-160"><a href="bookmark-property-ado.md">Закладка</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-161">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-163">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-165">всегда <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="53a6b-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-166"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-167">всегда <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="53a6b-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-169">всегда <strong>как таковые</strong></span><span class="sxs-lookup"><span data-stu-id="53a6b-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-170"><a href="bof-eof-properties-ado.md">ФУНКЦИЯ EOF</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-171">только для чтения</span><span class="sxs-lookup"><span data-stu-id="53a6b-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-172"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-173">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-174"><a href="locktype-property-ado.md">LockType для</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-175">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-177">Недоступен</span><span class="sxs-lookup"><span data-stu-id="53a6b-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-179">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-181">только для чтения</span><span class="sxs-lookup"><span data-stu-id="53a6b-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-183">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-185">только для чтения</span><span class="sxs-lookup"><span data-stu-id="53a6b-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-186"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-187">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="53a6b-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-188"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-189">только для чтения</span><span class="sxs-lookup"><span data-stu-id="53a6b-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-190"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-191">только для чтения</span><span class="sxs-lookup"><span data-stu-id="53a6b-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="53a6b-192">Доступность стандартных способов ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="53a6b-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53a6b-193">Метод</span><span class="sxs-lookup"><span data-stu-id="53a6b-193">Method</span></span></p></th>
<th><p><span data-ttu-id="53a6b-194">Доступные?</span><span class="sxs-lookup"><span data-stu-id="53a6b-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-196">Нет</span><span class="sxs-lookup"><span data-stu-id="53a6b-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-197"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-198">Нет</span><span class="sxs-lookup"><span data-stu-id="53a6b-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-200">Нет</span><span class="sxs-lookup"><span data-stu-id="53a6b-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-202">Нет</span><span class="sxs-lookup"><span data-stu-id="53a6b-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-203"><a href="clone-method-ado.md">Копия</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-204">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-205"><a href="close-method-ado.md">Закрыть</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-206">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-207"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-208">Нет</span><span class="sxs-lookup"><span data-stu-id="53a6b-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-209"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-210">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-211"><a href="move-method-ado.md">Перемещение</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-212">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-214">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-216">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-218">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-220">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-222">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-223"><a href="open-method-ado-recordset.md">Открытие</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-224">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-225"><a href="requery-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-226">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-227"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-228">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-229"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-230">Да</span><span class="sxs-lookup"><span data-stu-id="53a6b-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a6b-231"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="53a6b-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-232">Нет</span><span class="sxs-lookup"><span data-stu-id="53a6b-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a6b-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="53a6b-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="53a6b-234">Нет</span><span class="sxs-lookup"><span data-stu-id="53a6b-234">No</span></span></p></td>
</tr>
</tbody>
</table>

