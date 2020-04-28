---
title: Поставщик Microsoft OLE DB для службы Microsoft Active Directory
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23e1cab32fee6103a046219a7cda8c90f02d9f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288941"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="48bdd-102">Поставщик Microsoft OLE DB для службы Microsoft Active Directory</span><span class="sxs-lookup"><span data-stu-id="48bdd-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="48bdd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48bdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48bdd-104">Поставщик интерфейсов служб Microsoft Active Directory (ADSI) позволяет ADO подключаться к гетерогенным службам каталогов через ADSI.</span><span class="sxs-lookup"><span data-stu-id="48bdd-104">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI.</span></span> <span data-ttu-id="48bdd-105">Это предоставляет приложениям ADO доступ только для чтения к службам каталогов Microsoft Windows NT 4,0 и Microsoft Windows 2000 в дополнение к любым LDAP-совместимым службам каталогов и службам Novell Directory.</span><span class="sxs-lookup"><span data-stu-id="48bdd-105">This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services.</span></span> <span data-ttu-id="48bdd-106">Интерфейсы ADSI основываются на модели поставщика, поэтому если у вас есть новый поставщик, предоставляющий доступ к другому каталогу, приложение ADO сможет легко получить доступ к нему.</span><span class="sxs-lookup"><span data-stu-id="48bdd-106">ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly.</span></span> <span data-ttu-id="48bdd-107">Поставщик ADSI является бесплатным и поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="48bdd-107">The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="48bdd-108">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="48bdd-108">Connection String Parameters</span></span>

<span data-ttu-id="48bdd-109">Чтобы подключиться к поставщику, присвойте аргументу **provider** свойства [ConnectionString](connectionstring-property-ado.md) значение:</span><span class="sxs-lookup"><span data-stu-id="48bdd-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="48bdd-110">Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.</span><span class="sxs-lookup"><span data-stu-id="48bdd-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="48bdd-111">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="48bdd-111">Typical Connection String</span></span>

<span data-ttu-id="48bdd-112">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="48bdd-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="48bdd-113">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="48bdd-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48bdd-114">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="48bdd-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="48bdd-115">Описание</span><span class="sxs-lookup"><span data-stu-id="48bdd-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-116"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="48bdd-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="48bdd-117">Задает поставщика OLE DB для службы Microsoft Active Directory.</span><span class="sxs-lookup"><span data-stu-id="48bdd-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-118"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="48bdd-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="48bdd-119">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="48bdd-119">Specifies the user name.</span></span> <span data-ttu-id="48bdd-120">Если это ключевое слово не задано, используется текущий вход.</span><span class="sxs-lookup"><span data-stu-id="48bdd-120">If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="48bdd-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="48bdd-122">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="48bdd-122">Specifies the user password.</span></span> <span data-ttu-id="48bdd-123">Если это ключевое слово не задано, используется текущий вход.</span><span class="sxs-lookup"><span data-stu-id="48bdd-123">If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="48bdd-124">**Текст команды**</span><span class="sxs-lookup"><span data-stu-id="48bdd-124">**Command Text**</span></span>

<span data-ttu-id="48bdd-125">Поставщик в следующем синтаксисе распознает строку текста команды из четырех частей:</span><span class="sxs-lookup"><span data-stu-id="48bdd-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48bdd-126">Значение</span><span class="sxs-lookup"><span data-stu-id="48bdd-126">Value</span></span></p></th>
<th><p><span data-ttu-id="48bdd-127">Описание</span><span class="sxs-lookup"><span data-stu-id="48bdd-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-128"><em>Root</em></span><span class="sxs-lookup"><span data-stu-id="48bdd-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="48bdd-129">Указывает объект <strong>ADsPath</strong> , с которого начинается поиск (то есть, корневой каталог поиска).</span><span class="sxs-lookup"><span data-stu-id="48bdd-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-130"><em>Filter</em></span><span class="sxs-lookup"><span data-stu-id="48bdd-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="48bdd-131">Указывает фильтр поиска в формате RFC 1960.</span><span class="sxs-lookup"><span data-stu-id="48bdd-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-132"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="48bdd-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="48bdd-133">Указывает список возвращаемых атрибутов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="48bdd-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-134"><em>Область</em></span><span class="sxs-lookup"><span data-stu-id="48bdd-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="48bdd-135">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="48bdd-135">Optional.</span></span> <span data-ttu-id="48bdd-136"><strong>Строка</strong> , определяющая область поиска.</span><span class="sxs-lookup"><span data-stu-id="48bdd-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="48bdd-137">Может быть одним из следующих: Base — Поиск только базового объекта (корня поиска).</span><span class="sxs-lookup"><span data-stu-id="48bdd-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="48bdd-138">Онелевел — Поиск только одного уровня.</span><span class="sxs-lookup"><span data-stu-id="48bdd-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="48bdd-139">Поддерево — Поиск во всем поддереве.</span><span class="sxs-lookup"><span data-stu-id="48bdd-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="48bdd-140">Например:</span><span class="sxs-lookup"><span data-stu-id="48bdd-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="48bdd-141">Поставщик также поддерживает SQL SELECT для текста команды.</span><span class="sxs-lookup"><span data-stu-id="48bdd-141">The provider also supports SQL SELECT for command text.</span></span> <span data-ttu-id="48bdd-142">Например:</span><span class="sxs-lookup"><span data-stu-id="48bdd-142">For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="48bdd-143">Поставщик не принимает вызовы хранимых процедур или простые имена таблиц (например, свойство [CommandType](commandtype-property-ado.md) всегда будет **адкмдтекст**).</span><span class="sxs-lookup"><span data-stu-id="48bdd-143">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span> <span data-ttu-id="48bdd-144">Более полное описание элементов текста команды можно найти в документации по интерфейсам службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="48bdd-144">See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="48bdd-145">Поведение набора записей</span><span class="sxs-lookup"><span data-stu-id="48bdd-145">Recordset Behavior</span></span>

<span data-ttu-id="48bdd-146">В следующих таблицах перечислены функции, доступные для объекта [Recordset](recordset-object-ado.md) , открытого с помощью этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="48bdd-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="48bdd-147">Доступен только статический тип курсора (**адопенстатик**).</span><span class="sxs-lookup"><span data-stu-id="48bdd-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="48bdd-148">Для получения более подробных сведений о поведении **набора записей** для конфигурации поставщика [запустите метод](supports-method-ado.md) Supports и перечислите коллекцию [свойств](properties-collection-ado.md) объекта **Recordset** , чтобы определить, присутствуют ли динамические свойства, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="48bdd-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="48bdd-149">Доступность стандартных свойств **записей** ADO:</span><span class="sxs-lookup"><span data-stu-id="48bdd-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48bdd-150">Свойство</span><span class="sxs-lookup"><span data-stu-id="48bdd-150">Property</span></span></p></th>
<th><p><span data-ttu-id="48bdd-151">Доступность</span><span class="sxs-lookup"><span data-stu-id="48bdd-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-153">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-155">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-157">только для чтения</span><span class="sxs-lookup"><span data-stu-id="48bdd-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-159">только для чтения</span><span class="sxs-lookup"><span data-stu-id="48bdd-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-160"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-161">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-163">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-165">всегда <strong>адусесервер</strong></span><span class="sxs-lookup"><span data-stu-id="48bdd-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-166"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-167">всегда <strong>адопенстатик</strong></span><span class="sxs-lookup"><span data-stu-id="48bdd-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-169">всегда <strong>адедитноне</strong></span><span class="sxs-lookup"><span data-stu-id="48bdd-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-170"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-171">только для чтения</span><span class="sxs-lookup"><span data-stu-id="48bdd-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-172"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-173">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-174"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-175">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-177">недоступен</span><span class="sxs-lookup"><span data-stu-id="48bdd-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-179">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-181">только для чтения</span><span class="sxs-lookup"><span data-stu-id="48bdd-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-183">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-185">только для чтения</span><span class="sxs-lookup"><span data-stu-id="48bdd-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-186"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-187">чтение и запись</span><span class="sxs-lookup"><span data-stu-id="48bdd-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-188"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-189">только для чтения</span><span class="sxs-lookup"><span data-stu-id="48bdd-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-190"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-191">только для чтения</span><span class="sxs-lookup"><span data-stu-id="48bdd-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="48bdd-192">Доступность стандартных методов **набора записей** ADO:</span><span class="sxs-lookup"><span data-stu-id="48bdd-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48bdd-193">Method</span><span class="sxs-lookup"><span data-stu-id="48bdd-193">Method</span></span></p></th>
<th><p><span data-ttu-id="48bdd-194">Доступность?</span><span class="sxs-lookup"><span data-stu-id="48bdd-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-196">Нет</span><span class="sxs-lookup"><span data-stu-id="48bdd-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-197"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-198">Нет</span><span class="sxs-lookup"><span data-stu-id="48bdd-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-200">Нет</span><span class="sxs-lookup"><span data-stu-id="48bdd-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-202">Нет</span><span class="sxs-lookup"><span data-stu-id="48bdd-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-203"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-204">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-205"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-206">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-207"><a href="delete-method-ado-recordset.md">удаление</a>;</span><span class="sxs-lookup"><span data-stu-id="48bdd-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-208">Нет</span><span class="sxs-lookup"><span data-stu-id="48bdd-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-209"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-210">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-211"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-212">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-214">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-216">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-218">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-220">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-222">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-223"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-224">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-225"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-226">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-227"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-228">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-229"><a href="supports-method-ado.md">Имеется</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-230">Да</span><span class="sxs-lookup"><span data-stu-id="48bdd-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48bdd-231"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="48bdd-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-232">Нет</span><span class="sxs-lookup"><span data-stu-id="48bdd-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48bdd-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="48bdd-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="48bdd-234">Нет</span><span class="sxs-lookup"><span data-stu-id="48bdd-234">No</span></span></p></td>
</tr>
</tbody>
</table>

