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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288934"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="55b70-102">Поставщик Microsoft OLE DB для Oracle</span><span class="sxs-lookup"><span data-stu-id="55b70-102">Microsoft OLE DB Provider for Oracle</span></span>

<span data-ttu-id="55b70-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55b70-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55b70-104">Поставщик Microsoft OLE DB для Oracle позволяет ADO получать доступ к базам данных Oracle.</span><span class="sxs-lookup"><span data-stu-id="55b70-104">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="55b70-105">Параметры строки подключения</span><span class="sxs-lookup"><span data-stu-id="55b70-105">Connection String Parameters</span></span>

<span data-ttu-id="55b70-106">Чтобы подключиться к поставщику, присвойте аргументу *provider* свойства [ConnectionString](connectionstring-property-ado.md) значение:</span><span class="sxs-lookup"><span data-stu-id="55b70-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAORA 
```

<span data-ttu-id="55b70-107">Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.</span><span class="sxs-lookup"><span data-stu-id="55b70-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

<span data-ttu-id="55b70-108">Если в базе данных Oracle выполняется запрос на присоединение с набором ключей или динамическим курсором, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="55b70-108">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs.</span></span> <span data-ttu-id="55b70-109">Oracle поддерживает только статический курсор только для чтения.</span><span class="sxs-lookup"><span data-stu-id="55b70-109">Oracle only supports a static read-only cursor.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="55b70-110">Типичная строка подключения</span><span class="sxs-lookup"><span data-stu-id="55b70-110">Typical Connection String</span></span>

<span data-ttu-id="55b70-111">Типичная строка подключения для этого поставщика:</span><span class="sxs-lookup"><span data-stu-id="55b70-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

<span data-ttu-id="55b70-112">Строка состоит из следующих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="55b70-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55b70-113">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="55b70-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="55b70-114">Описание</span><span class="sxs-lookup"><span data-stu-id="55b70-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55b70-115"><strong>Поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-116">Задает поставщика OLE DB для Oracle.</span><span class="sxs-lookup"><span data-stu-id="55b70-116">Specifies the OLE DB Provider for Oracle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55b70-117"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-117"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-118">Задает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="55b70-118">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55b70-119"><strong>Идентификатор пользователя</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-120">Задает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="55b70-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55b70-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-122">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="55b70-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="55b70-123">Параметры подключения, зависящие от поставщика</span><span class="sxs-lookup"><span data-stu-id="55b70-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="55b70-124">Поставщик поддерживает несколько параметров подключения, относящихся к поставщику, помимо тех, которые определены в ADO.</span><span class="sxs-lookup"><span data-stu-id="55b70-124">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</span></span> <span data-ttu-id="55b70-125">Как и в случае со свойствами подключения ADO, эти свойства, зависящие от поставщика, можно задать с помощью коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или в качестве части **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="55b70-125">As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or as part of the **ConnectionString**.</span></span>

<span data-ttu-id="55b70-126">Эти параметры полностью описаны в справочнике программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="55b70-126">These parameters are fully described in the OLE DB Programmer's Reference.</span></span> <span data-ttu-id="55b70-127">( [Индекс динамического свойства ADO](ado-dynamic-property-index.md) предоставляет перекрестные ссылки между именами этих параметров и СООТВЕТСТВУЮЩИМИ свойствами OLE DB.)</span><span class="sxs-lookup"><span data-stu-id="55b70-127">(The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55b70-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="55b70-128">Parameter</span></span></p></th>
<th><p><span data-ttu-id="55b70-129">Описание</span><span class="sxs-lookup"><span data-stu-id="55b70-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55b70-130"><strong>Дескриптор окна</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-130"><strong>Window Handle</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-131">Указывает дескриптор окна, используемый для вывода дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="55b70-131">Indicates the window handle to use to prompt for additional information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55b70-132"><strong>Идентификатор языкового стандарта</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-132"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-133">Указывает уникальное 32-разрядное число (например, 1033), которое определяет параметры, связанные с языком пользователя.</span><span class="sxs-lookup"><span data-stu-id="55b70-133">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language.</span></span> <span data-ttu-id="55b70-134">Эти установки указывают, как форматируется Дата и время, сортируются элементы в алфавитном порядке, сравниваются строки и т. д.</span><span class="sxs-lookup"><span data-stu-id="55b70-134">These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55b70-135"><strong>Службы OLE DB</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-135"><strong>OLE DB Services</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-136">Указывает битовую маску, указывающую, какие службы OLE DB необходимо включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="55b70-136">Indicates a bitmask that specifies OLE DB services to enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55b70-137"><strong>Prompt</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-137"><strong>Prompt</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-138">Указывает, следует ли запрашивать пользователя во время установки подключения.</span><span class="sxs-lookup"><span data-stu-id="55b70-138">Indicates whether to prompt the user while a connection is being established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55b70-139"><strong>Расширенные свойства</strong></span><span class="sxs-lookup"><span data-stu-id="55b70-139"><strong>Extended Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="55b70-140">Строка, содержащая сведения о расширенном подключении, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="55b70-140">A string containing provider-specific, extended connection information.</span></span> <span data-ttu-id="55b70-141">Это свойство используется только для сведений о соединении с конкретным поставщиком, которые невозможно описать с помощью механизма свойств.</span><span class="sxs-lookup"><span data-stu-id="55b70-141">Use this property only for provider-specific connection information that cannot be described through the property mechanism.</span></span></p></td>
</tr>
</tbody>
</table>

