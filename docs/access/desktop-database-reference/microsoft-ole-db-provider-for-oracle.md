---
title: Поставщик Microsoft OLE DB для Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9b506f40039ff91a6b1985606322fd86a9e7c0e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722503"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="731d9-102">Поставщик Microsoft OLE DB для Oracle</span><span class="sxs-lookup"><span data-stu-id="731d9-102">Microsoft OLE DB Provider for Oracle</span></span>

<span data-ttu-id="731d9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="731d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="731d9-104">Поставщик Microsoft OLE DB для Oracle позволяет ADO для доступа к базам данных Oracle.</span><span class="sxs-lookup"><span data-stu-id="731d9-104">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="731d9-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="731d9-105">Connection String Parameters</span></span>

<span data-ttu-id="731d9-106">Для подключения к данным поставщиком, задайте для свойства [ConnectionString](connectionstring-property-ado.md) для аргумента *поставщика* :</span><span class="sxs-lookup"><span data-stu-id="731d9-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAORA 
```

<span data-ttu-id="731d9-107">Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.</span><span class="sxs-lookup"><span data-stu-id="731d9-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

<span data-ttu-id="731d9-108">Запрос соединения с набором ключей или динамический курсор при выполнении в базе данных Oracle, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="731d9-108">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs.</span></span> <span data-ttu-id="731d9-109">Oracle поддерживает только статический курсор только для чтения.</span><span class="sxs-lookup"><span data-stu-id="731d9-109">Oracle only supports a static read-only cursor.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="731d9-110">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="731d9-110">Typical Connection String</span></span>

<span data-ttu-id="731d9-111">— Это строка соединения для данного поставщика:</span><span class="sxs-lookup"><span data-stu-id="731d9-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

<span data-ttu-id="731d9-112">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="731d9-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="731d9-113">Keyword</span><span class="sxs-lookup"><span data-stu-id="731d9-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="731d9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="731d9-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="731d9-115"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-116">Задает поставщика OLE DB для Oracle.</span><span class="sxs-lookup"><span data-stu-id="731d9-116">Specifies the OLE DB Provider for Oracle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="731d9-117"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-117"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="731d9-118">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="731d9-119"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-120">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="731d9-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="731d9-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-122">Задает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="731d9-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="731d9-123">Параметры подключения от поставщика</span><span class="sxs-lookup"><span data-stu-id="731d9-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="731d9-124">Поставщик поддерживает несколько параметров подключения для конкретного поставщика дополнение к тем определяется ADO.</span><span class="sxs-lookup"><span data-stu-id="731d9-124">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="731d9-125">Как с помощью свойства подключения ADO, эти свойства от поставщика может быть задано посредством коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или как часть **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="731d9-125">As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or as part of the **ConnectionString**.</span></span>

<span data-ttu-id="731d9-126">Эти параметры подробно описаны в Справочник программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="731d9-126">These parameters are fully described in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="731d9-127">( [Индекс динамические свойства ADO](ado-dynamic-property-index.md) предоставляет перекрестная ссылка между имена этих параметров и соответствующих свойств OLE DB).</span><span class="sxs-lookup"><span data-stu-id="731d9-127">(The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="731d9-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="731d9-128">Parameter</span></span></p></th>
<th><p><span data-ttu-id="731d9-129">Описание</span><span class="sxs-lookup"><span data-stu-id="731d9-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="731d9-130"><strong>Дескриптор окна</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-130"><strong>Window Handle</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-131">Указывает дескриптор окна для использования запроса для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="731d9-131">Indicates the window handle to use to prompt for additional information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="731d9-132"><strong>Идентификатор языка</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-132"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-133">Указывает уникальный 32-разрядная версия номер (например, 1033), который указывает параметры, связанные с языком пользователя.</span><span class="sxs-lookup"><span data-stu-id="731d9-133">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language.</span></span> <span data-ttu-id="731d9-134">Эти параметры указывают способ форматирования даты и времени, элементы сортируются в алфавитном порядке, строк сравниваются и т. д.</span><span class="sxs-lookup"><span data-stu-id="731d9-134">These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="731d9-135"><strong>Службы OLE DB</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-135"><strong>OLE DB Services</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-136">Указывает битовую маску, которая определяет службы OLE DB для включения или отключения.</span><span class="sxs-lookup"><span data-stu-id="731d9-136">Indicates a bitmask that specifies OLE DB services to enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="731d9-137"><strong>Prompt</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-137"><strong>Prompt</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-138">Указывает, следует ли запрашивать у пользователя при установке подключения.</span><span class="sxs-lookup"><span data-stu-id="731d9-138">Indicates whether to prompt the user while a connection is being established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="731d9-139"><strong>Расширенные свойства</strong></span><span class="sxs-lookup"><span data-stu-id="731d9-139"><strong>Extended Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="731d9-140">Строка, содержащая сведения о подключении к от поставщика, расширенная.</span><span class="sxs-lookup"><span data-stu-id="731d9-140">A string containing provider-specific, extended connection information.</span></span> <span data-ttu-id="731d9-141">Это свойство используется только для подключения к конкретному поставщику данных, которые не удается описано через механизм свойства.</span><span class="sxs-lookup"><span data-stu-id="731d9-141">Use this property only for provider-specific connection information that cannot be described through the property mechanism.</span></span></p></td>
</tr>
</tbody>
</table>

