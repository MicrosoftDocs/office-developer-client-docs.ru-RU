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
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="9a4e0-102">Поставщик Microsoft OLE DB для службы Microsoft Active Directory</span><span class="sxs-lookup"><span data-stu-id="9a4e0-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="9a4e0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a4e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a4e0-104">Поставщик служб Microsoft Active Directory Service Interfaces (ADSI) позволяет ADO подключаться к неоднородным службам каталогов с помощью ADSI.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-104">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI.</span></span> <span data-ttu-id="9a4e0-105">Это предоставляет приложениям ADO доступ только для чтения к службам каталогов Microsoft Windows NT 4.0 и Microsoft Windows 2000, а также к любым службам каталогов, совместимым с LDAP и Novell Directory Services.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-105">This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services.</span></span> <span data-ttu-id="9a4e0-106">Сам ADSI основан на модели поставщика, поэтому если новый поставщик дает доступ к другому каталогу, приложение ADO сможет получить к нему доступ без проблем.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-106">ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly.</span></span> <span data-ttu-id="9a4e0-107">Поставщик ADSI является бесплатным и включен юникодом.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-107">The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="9a4e0-108">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="9a4e0-108">Connection String Parameters</span></span>

<span data-ttu-id="9a4e0-109">Чтобы подключиться к этому поставщику, установите **аргумент поставщика** свойства [ConnectionString:](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="9a4e0-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="9a4e0-110">Чтение свойства [Provider](provider-property-ado.md) также вернет эту строку.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="9a4e0-111">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="9a4e0-111">Typical Connection String</span></span>

<span data-ttu-id="9a4e0-112">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="9a4e0-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="9a4e0-113">Строка состоит из этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="9a4e0-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a4e0-114">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="9a4e0-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="9a4e0-115">Description</span><span class="sxs-lookup"><span data-stu-id="9a4e0-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-116"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="9a4e0-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-117">Указывает поставщика OLE DB для службы Microsoft Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-118"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="9a4e0-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-119">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-119">Specifies the user name.</span></span> <span data-ttu-id="9a4e0-120">Если это ключевое слово пропущено, используется текущий логотип.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-120">If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="9a4e0-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-122">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-122">Specifies the user password.</span></span> <span data-ttu-id="9a4e0-123">Если это ключевое слово пропущено, используется текущий логотип.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-123">If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a4e0-124">**Командный текст**</span><span class="sxs-lookup"><span data-stu-id="9a4e0-124">**Command Text**</span></span>

<span data-ttu-id="9a4e0-125">Текстовая строка из четырех команд распознается поставщиком в следующем синтаксисе:</span><span class="sxs-lookup"><span data-stu-id="9a4e0-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a4e0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9a4e0-126">Value</span></span></p></th>
<th><p><span data-ttu-id="9a4e0-127">Описание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-128"><em>Root</em></span><span class="sxs-lookup"><span data-stu-id="9a4e0-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-129">Указывает объект <strong>ADsPath,</strong> с которого следует начать поиск (то есть корень поиска).</span><span class="sxs-lookup"><span data-stu-id="9a4e0-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-130"><em>Filter</em></span><span class="sxs-lookup"><span data-stu-id="9a4e0-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-131">Указывает фильтр поиска в формате RFC 1960.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-132"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="9a4e0-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-133">Указывает список атрибутов, возвращаемого с запятой.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-134"><em>Scope</em></span><span class="sxs-lookup"><span data-stu-id="9a4e0-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-135">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-135">Optional.</span></span> <span data-ttu-id="9a4e0-136"><strong>Строка,</strong> которая указывает область поиска.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="9a4e0-137">Может быть одним из следующих: Base — поиск только базового объекта (корень поиска).</span><span class="sxs-lookup"><span data-stu-id="9a4e0-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="9a4e0-138">OneLevel — поиск только одного уровня.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="9a4e0-139">Subtree — поиск всего подтрия.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a4e0-140">Пример.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="9a4e0-141">Поставщик также поддерживает SQL SELECT для командного текста.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-141">The provider also supports SQL SELECT for command text.</span></span> <span data-ttu-id="9a4e0-142">Пример.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-142">For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="9a4e0-143">Поставщик не принимает сохраненные вызовы процедур или простые имена таблиц (например, свойство [CommandType](commandtype-property-ado.md) всегда **будет adCmdText).**</span><span class="sxs-lookup"><span data-stu-id="9a4e0-143">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span> <span data-ttu-id="9a4e0-144">Дополнительные описания текстовых элементов команд см. в документации по интерфейсам службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-144">See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="9a4e0-145">Поведение наборов записей</span><span class="sxs-lookup"><span data-stu-id="9a4e0-145">Recordset Behavior</span></span>

<span data-ttu-id="9a4e0-146">В следующих таблицах перечислить функции, доступные на [объекте Recordset,](recordset-object-ado.md) открытом с помощью этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="9a4e0-147">Доступен только тип статического курсора **(adOpenStatic).**</span><span class="sxs-lookup"><span data-stu-id="9a4e0-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="9a4e0-148">Дополнительные сведения о поведении **Recordset** для конфигурации поставщика запустите метод [Supports](supports-method-ado.md) и введите коллекцию [Свойств](properties-collection-ado.md) в **наборе Recordset,** чтобы определить, присутствуют ли динамические свойства конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="9a4e0-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="9a4e0-149">Доступность стандартных свойств ADO **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="9a4e0-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a4e0-150">Свойство</span><span class="sxs-lookup"><span data-stu-id="9a4e0-150">Property</span></span></p></th>
<th><p><span data-ttu-id="9a4e0-151">Доступность</span><span class="sxs-lookup"><span data-stu-id="9a4e0-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-153">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-155">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-157">read-only</span><span class="sxs-lookup"><span data-stu-id="9a4e0-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-159">read-only</span><span class="sxs-lookup"><span data-stu-id="9a4e0-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-160"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-161">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-163">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-165">всегда <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="9a4e0-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-166"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-167">всегда <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="9a4e0-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-169">всегда <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="9a4e0-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-170"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-171">read-only</span><span class="sxs-lookup"><span data-stu-id="9a4e0-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-172"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-173">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-174"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-175">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-177">недоступен</span><span class="sxs-lookup"><span data-stu-id="9a4e0-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-179">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-181">read-only</span><span class="sxs-lookup"><span data-stu-id="9a4e0-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-183">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-185">read-only</span><span class="sxs-lookup"><span data-stu-id="9a4e0-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-186"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-187">чтение и написание</span><span class="sxs-lookup"><span data-stu-id="9a4e0-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-188"><a href="state-property-ado.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-189">read-only</span><span class="sxs-lookup"><span data-stu-id="9a4e0-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-190"><a href="status-property-ado-recordset.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-191">read-only</span><span class="sxs-lookup"><span data-stu-id="9a4e0-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a4e0-192">Доступность стандартных методов ADO **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="9a4e0-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a4e0-193">Метод</span><span class="sxs-lookup"><span data-stu-id="9a4e0-193">Method</span></span></p></th>
<th><p><span data-ttu-id="9a4e0-194">Доступно?</span><span class="sxs-lookup"><span data-stu-id="9a4e0-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-196">Нет</span><span class="sxs-lookup"><span data-stu-id="9a4e0-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-197"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-198">Нет</span><span class="sxs-lookup"><span data-stu-id="9a4e0-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-200">Нет</span><span class="sxs-lookup"><span data-stu-id="9a4e0-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-202">Нет</span><span class="sxs-lookup"><span data-stu-id="9a4e0-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-203"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-204">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-205"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-206">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-207"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-208">Нет</span><span class="sxs-lookup"><span data-stu-id="9a4e0-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-209"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-210">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-211"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-212">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-214">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-216">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-218">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-220">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-222">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-223"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-224">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-225"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-226">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-227"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-228">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-229"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-230">Да</span><span class="sxs-lookup"><span data-stu-id="9a4e0-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a4e0-231"><a href="update-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-232">Нет</span><span class="sxs-lookup"><span data-stu-id="9a4e0-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a4e0-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="9a4e0-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9a4e0-234">Нет</span><span class="sxs-lookup"><span data-stu-id="9a4e0-234">No</span></span></p></td>
</tr>
</tbody>
</table>

