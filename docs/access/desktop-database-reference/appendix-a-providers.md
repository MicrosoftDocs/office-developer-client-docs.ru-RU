---
title: Приложение А. Поставщики
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4549c8817361cfb5b9fa730ee37ca6a07edc98b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297062"
---
# <a name="appendix-a-providers"></a><span data-ttu-id="a506d-102">Приложение А. Поставщики</span><span class="sxs-lookup"><span data-stu-id="a506d-102">Appendix A: Providers</span></span>


<span data-ttu-id="a506d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a506d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a506d-104">Этот раздел посвящен трем типам поставщиков: поставщикам данных, поставщикам услуг и компонентам служб.</span><span class="sxs-lookup"><span data-stu-id="a506d-104">This section addresses three kinds of providers: data providers, service providers, and service components.</span></span> <span data-ttu-id="a506d-105">Поставщики подпадают под две категории: поставщики, предоставляющие данные, и поставщики услуг.</span><span class="sxs-lookup"><span data-stu-id="a506d-105">Providers fall into two categories: those providing data and those providing services.</span></span> <span data-ttu-id="a506d-106">Поставщик *данных владеет* собственными данными и предоставляет их приложению в табличной форме.</span><span class="sxs-lookup"><span data-stu-id="a506d-106">A *data provider* owns its own data and exposes it in tabular form to your application.</span></span> <span data-ttu-id="a506d-107">Поставщик услуг инкапсулирует службу, выдав и потребляя данные, дополнив функции в приложениях ADO. </span><span class="sxs-lookup"><span data-stu-id="a506d-107">A *service provider* encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="a506d-108">Поставщик услуг также может быть далее определен как компонент *службы,* который должен работать в сочетании с другими поставщиками или компонентами службы.</span><span class="sxs-lookup"><span data-stu-id="a506d-108">A service provider may also be further defined as a *service component*, which must work in conjunction with other service providers or components.</span></span>

## <a name="data-providers"></a><span data-ttu-id="a506d-109">Поставщики данных</span><span class="sxs-lookup"><span data-stu-id="a506d-109">Data providers</span></span>

<span data-ttu-id="a506d-110">ADO — это мощный и гибкий инструмент, так как он может подключаться к любому из разных поставщиков данных и по-прежнему использовать ту же модель программирования независимо от конкретных функций конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="a506d-110">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span>

<span data-ttu-id="a506d-111">Однако, так как каждый поставщик данных уникален, способ взаимодействия приложения с ADO немного зависит от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="a506d-111">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider.</span></span> <span data-ttu-id="a506d-112">Различия обычно подпадают под одну из трех категорий:</span><span class="sxs-lookup"><span data-stu-id="a506d-112">The differences usually fall into one of three categories:</span></span>

- <span data-ttu-id="a506d-113">Параметры подключения в [свойстве ConnectionString.](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="a506d-113">Connection parameters in the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

- <span data-ttu-id="a506d-114">[Использование объекта](command-object-ado.md) command.</span><span class="sxs-lookup"><span data-stu-id="a506d-114">[Command](command-object-ado.md) object usage.</span></span>

- <span data-ttu-id="a506d-115">Поведение наборов [записей для конкретного](recordset-object-ado.md) поставщика.</span><span class="sxs-lookup"><span data-stu-id="a506d-115">Provider-specific [Recordset](recordset-object-ado.md) behavior.</span></span>

<span data-ttu-id="a506d-116">Ниже перечислены сведения о каждом поставщике данных, доступных в настоящее время корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a506d-116">Details for each of the data providers currently available from Microsoft are listed as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a506d-117">Область</span><span class="sxs-lookup"><span data-stu-id="a506d-117">Area</span></span></p></th>
<th><p><span data-ttu-id="a506d-118">Тема</span><span class="sxs-lookup"><span data-stu-id="a506d-118">Topic</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a506d-119">Базы данных ODBC</span><span class="sxs-lookup"><span data-stu-id="a506d-119">ODBC databases</span></span></p></td>
<td><p><span data-ttu-id="a506d-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span><span class="sxs-lookup"><span data-stu-id="a506d-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a506d-121">Служба индексации (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="a506d-121">Microsoft Indexing Service</span></span></p></td>
<td><p><span data-ttu-id="a506d-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span><span class="sxs-lookup"><span data-stu-id="a506d-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a506d-123">Служба Microsoft Active Directory</span><span class="sxs-lookup"><span data-stu-id="a506d-123">Microsoft Active Directory Service</span></span></p></td>
<td><p><span data-ttu-id="a506d-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span><span class="sxs-lookup"><span data-stu-id="a506d-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a506d-125">Базы данных Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="a506d-125">Microsoft Jet databases</span></span></p></td>
<td><p><span data-ttu-id="a506d-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></span><span class="sxs-lookup"><span data-stu-id="a506d-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a506d-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="a506d-127">Microsoft SQL Server</span></span></p></td>
<td><p><span data-ttu-id="a506d-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span><span class="sxs-lookup"><span data-stu-id="a506d-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a506d-129">Базы данных Oracle</span><span class="sxs-lookup"><span data-stu-id="a506d-129">Oracle databases</span></span></p></td>
<td><p><span data-ttu-id="a506d-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span><span class="sxs-lookup"><span data-stu-id="a506d-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a506d-131">Интернет-публикация</span><span class="sxs-lookup"><span data-stu-id="a506d-131">Internet Publishing</span></span></p></td>
<td><p><span data-ttu-id="a506d-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span><span class="sxs-lookup"><span data-stu-id="a506d-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a><span data-ttu-id="a506d-133">Динамические свойства для конкретного поставщика</span><span class="sxs-lookup"><span data-stu-id="a506d-133">Provider-specific dynamic properties</span></span>

<span data-ttu-id="a506d-134">Коллекции [свойств объектов](properties-collection-ado.md) [Connection,](connection-object-ado.md) [Command](command-object-ado.md)и [Recordset](recordset-object-ado.md) включают динамические свойства, специфические для поставщика.</span><span class="sxs-lookup"><span data-stu-id="a506d-134">The [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), and [Recordset](recordset-object-ado.md) objects include dynamic properties specific to the provider.</span></span> <span data-ttu-id="a506d-135">Эти свойства предоставляют сведения о функциях, характерных для поставщика, помимо встроенных свойств, поддерживаемых ADO.</span><span class="sxs-lookup"><span data-stu-id="a506d-135">These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</span></span>

<span data-ttu-id="a506d-136">После установления подключения и создания этих объектов используйте метод [Refresh](refresh-method-ado.md) в коллекции **свойств** объекта для получения свойств, характерных для конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="a506d-136">After establishing the connection and creating these objects, use the [Refresh](refresh-method-ado.md) method on the object's **Properties** collection to obtain the provider-specific properties.</span></span> <span data-ttu-id="a506d-137">Подробные сведения об этих динамических свойствах можно найти в документации поставщика и справочнике программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a506d-137">Refer to the provider documentation and the OLE DB Programmer's Reference for detailed information about these dynamic properties.</span></span>

## <a name="service-providers"></a><span data-ttu-id="a506d-138">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="a506d-138">Service providers</span></span>

<span data-ttu-id="a506d-139">Чтобы использовать поставщика услуг, необходимо предоставить ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="a506d-139">To use a service provider, you must supply a keyword.</span></span> <span data-ttu-id="a506d-140">Также следует знать о динамических свойствах, связанных с каждым поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="a506d-140">You should also be aware of the provider-specific dynamic properties associated with each service provider.</span></span> <span data-ttu-id="a506d-141">Сведения о поставщике перечислены для каждого поставщика услуг, доступных в настоящее время корпорацией Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="a506d-141">Provider-specific details are listed for each of the service providers currently available from Microsoft:</span></span>

- [<span data-ttu-id="a506d-142">Служба формирования данных Майкрософт для OLE DB</span><span class="sxs-lookup"><span data-stu-id="a506d-142">Microsoft Data Shaping Service for OLE DB</span></span>](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [<span data-ttu-id="a506d-143">Поставщик сохраняемости Microsoft OLE DB</span><span class="sxs-lookup"><span data-stu-id="a506d-143">Microsoft OLE DB Persistence Provider</span></span>](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [<span data-ttu-id="a506d-144">Microsoft OLE DB Remoting Provider</span><span class="sxs-lookup"><span data-stu-id="a506d-144">Microsoft OLE DB Remoting Provider</span></span>](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a><span data-ttu-id="a506d-145">Компоненты службы</span><span class="sxs-lookup"><span data-stu-id="a506d-145">Service components</span></span>

<span data-ttu-id="a506d-146">Компонент [службы курсора для службы OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) дополняет курсор поддержки функций поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="a506d-146">The [Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) service component supplements the cursor support functions of data providers.</span></span> <span data-ttu-id="a506d-147">Кроме того, для него требуется ключевое слово и динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="a506d-147">It also requires a keyword and has dynamic properties.</span></span>

<span data-ttu-id="a506d-148">Дополнительные сведения о поставщиках см. в документации по Microsoft OLE DB в microsoft Data Access Components SDK или в Центре разработчиков [платформы данных.](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="a506d-148">For more information about providers, see the documentation for Microsoft OLE DB in the Microsoft Data Access Components SDK or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

## <a name="provider-commands"></a><span data-ttu-id="a506d-149">Команды поставщика</span><span class="sxs-lookup"><span data-stu-id="a506d-149">Provider commands</span></span>

<span data-ttu-id="a506d-150">Если приложения позволяют пользователям вводить операторы SQL в качестве команд поставщика для каждого из перечисленных здесь поставщиков, необходимо всегда проверять входные данные пользователей и быть внимательными к возможным атакам хакеров с помощью потенциально опасных операторов SQL, например, в составе пользовательского ввода.</span><span class="sxs-lookup"><span data-stu-id="a506d-150">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statement, such as, , as part of the user input.</span></span>

