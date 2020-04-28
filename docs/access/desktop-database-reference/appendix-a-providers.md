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
# <a name="appendix-a-providers"></a><span data-ttu-id="889d6-102">Приложение А. Поставщики</span><span class="sxs-lookup"><span data-stu-id="889d6-102">Appendix A: Providers</span></span>


<span data-ttu-id="889d6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="889d6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="889d6-104">В этом разделе рассматриваются три типа поставщиков: поставщики данных, поставщики услуг и компоненты служб.</span><span class="sxs-lookup"><span data-stu-id="889d6-104">This section addresses three kinds of providers: data providers, service providers, and service components.</span></span> <span data-ttu-id="889d6-105">Поставщики делятся на две категории: они предоставляют данные и предоставляют службы.</span><span class="sxs-lookup"><span data-stu-id="889d6-105">Providers fall into two categories: those providing data and those providing services.</span></span> <span data-ttu-id="889d6-106">*Поставщик данных* владеет собственными данными и предоставляет приложению доступ к нему в табличном виде.</span><span class="sxs-lookup"><span data-stu-id="889d6-106">A *data provider* owns its own data and exposes it in tabular form to your application.</span></span> <span data-ttu-id="889d6-107">*Поставщик услуг* инкапсулирует службу, создавая и используя данные, расширяя функции в приложениях ADO.</span><span class="sxs-lookup"><span data-stu-id="889d6-107">A *service provider* encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="889d6-108">Поставщик услуг также может быть дополнительно определен как *компонент службы*, который должен работать совместно с другими поставщиками служб или компонентами.</span><span class="sxs-lookup"><span data-stu-id="889d6-108">A service provider may also be further defined as a *service component*, which must work in conjunction with other service providers or components.</span></span>

## <a name="data-providers"></a><span data-ttu-id="889d6-109">Поставщики данных</span><span class="sxs-lookup"><span data-stu-id="889d6-109">Data providers</span></span>

<span data-ttu-id="889d6-110">ADO является мощным и гибким, так как он может подключаться к любому из нескольких разных поставщиков данных и по-прежнему предоставлять одну и ту же модель программирования независимо от конкретных функций любого поставщика.</span><span class="sxs-lookup"><span data-stu-id="889d6-110">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span>

<span data-ttu-id="889d6-111">Тем не менее, так как каждый поставщик данных уникален, то, как приложение взаимодействует с ADO, немного зависит от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="889d6-111">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider.</span></span> <span data-ttu-id="889d6-112">Различия обычно попадают в одну из трех категорий:</span><span class="sxs-lookup"><span data-stu-id="889d6-112">The differences usually fall into one of three categories:</span></span>

- <span data-ttu-id="889d6-113">Параметры подключения в свойстве [ConnectionString](connectionstring-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="889d6-113">Connection parameters in the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

- <span data-ttu-id="889d6-114">Использование объекта [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="889d6-114">[Command](command-object-ado.md) object usage.</span></span>

- <span data-ttu-id="889d6-115">Поведение [набора записей](recordset-object-ado.md) , зависящее от поставщика.</span><span class="sxs-lookup"><span data-stu-id="889d6-115">Provider-specific [Recordset](recordset-object-ado.md) behavior.</span></span>

<span data-ttu-id="889d6-116">Подробные сведения о каждом из поставщиков данных, доступных в Майкрософт, перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="889d6-116">Details for each of the data providers currently available from Microsoft are listed as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="889d6-117">Область</span><span class="sxs-lookup"><span data-stu-id="889d6-117">Area</span></span></p></th>
<th><p><span data-ttu-id="889d6-118">Тема</span><span class="sxs-lookup"><span data-stu-id="889d6-118">Topic</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="889d6-119">Базы данных ODBC</span><span class="sxs-lookup"><span data-stu-id="889d6-119">ODBC databases</span></span></p></td>
<td><p><span data-ttu-id="889d6-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span><span class="sxs-lookup"><span data-stu-id="889d6-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889d6-121">Служба индексирования (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="889d6-121">Microsoft Indexing Service</span></span></p></td>
<td><p><span data-ttu-id="889d6-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span><span class="sxs-lookup"><span data-stu-id="889d6-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889d6-123">Служба Microsoft Active Directory</span><span class="sxs-lookup"><span data-stu-id="889d6-123">Microsoft Active Directory Service</span></span></p></td>
<td><p><span data-ttu-id="889d6-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span><span class="sxs-lookup"><span data-stu-id="889d6-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889d6-125">Базы данных Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="889d6-125">Microsoft Jet databases</span></span></p></td>
<td><p><span data-ttu-id="889d6-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></span><span class="sxs-lookup"><span data-stu-id="889d6-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889d6-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="889d6-127">Microsoft SQL Server</span></span></p></td>
<td><p><span data-ttu-id="889d6-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span><span class="sxs-lookup"><span data-stu-id="889d6-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889d6-129">Базы данных Oracle</span><span class="sxs-lookup"><span data-stu-id="889d6-129">Oracle databases</span></span></p></td>
<td><p><span data-ttu-id="889d6-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span><span class="sxs-lookup"><span data-stu-id="889d6-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889d6-131">Публикация в Интернете</span><span class="sxs-lookup"><span data-stu-id="889d6-131">Internet Publishing</span></span></p></td>
<td><p><span data-ttu-id="889d6-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span><span class="sxs-lookup"><span data-stu-id="889d6-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a><span data-ttu-id="889d6-133">Динамические свойства, зависящие от поставщика</span><span class="sxs-lookup"><span data-stu-id="889d6-133">Provider-specific dynamic properties</span></span>

<span data-ttu-id="889d6-134">Коллекции [свойств](properties-collection-ado.md) объекта [подключения](connection-object-ado.md), [команды](command-object-ado.md)и объекта [Recordset](recordset-object-ado.md) содержат динамические свойства, характерные для поставщика.</span><span class="sxs-lookup"><span data-stu-id="889d6-134">The [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), and [Recordset](recordset-object-ado.md) objects include dynamic properties specific to the provider.</span></span> <span data-ttu-id="889d6-135">Эти свойства предоставляют сведения о функциях, относящихся к поставщику, за пределами встроенных свойств, поддерживаемых ADO.</span><span class="sxs-lookup"><span data-stu-id="889d6-135">These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</span></span>

<span data-ttu-id="889d6-136">После установки подключения и создания этих объектов используйте метод [Refresh](refresh-method-ado.md) в коллекции **свойств** объекта, чтобы получить свойства, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="889d6-136">After establishing the connection and creating these objects, use the [Refresh](refresh-method-ado.md) method on the object's **Properties** collection to obtain the provider-specific properties.</span></span> <span data-ttu-id="889d6-137">Для получения подробных сведений об этих динамических свойствах обратитесь к документации по поставщику и Справочнику программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="889d6-137">Refer to the provider documentation and the OLE DB Programmer's Reference for detailed information about these dynamic properties.</span></span>

## <a name="service-providers"></a><span data-ttu-id="889d6-138">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="889d6-138">Service providers</span></span>

<span data-ttu-id="889d6-139">Для использования поставщика услуг необходимо указать ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="889d6-139">To use a service provider, you must supply a keyword.</span></span> <span data-ttu-id="889d6-140">Кроме того, следует помнить о динамических свойствах, связанных с поставщиками, которые связаны с каждым поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="889d6-140">You should also be aware of the provider-specific dynamic properties associated with each service provider.</span></span> <span data-ttu-id="889d6-141">Сведения, относящиеся к поставщику, указаны для каждого из поставщиков услуг, доступных в корпорации Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="889d6-141">Provider-specific details are listed for each of the service providers currently available from Microsoft:</span></span>

- [<span data-ttu-id="889d6-142">Служба формирования данных (Майкрософт) для OLE DB</span><span class="sxs-lookup"><span data-stu-id="889d6-142">Microsoft Data Shaping Service for OLE DB</span></span>](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [<span data-ttu-id="889d6-143">Поставщик службы сохранения Microsoft OLE DB</span><span class="sxs-lookup"><span data-stu-id="889d6-143">Microsoft OLE DB Persistence Provider</span></span>](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [<span data-ttu-id="889d6-144">Поставщик удаленного взаимодействия OLE DB (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="889d6-144">Microsoft OLE DB Remoting Provider</span></span>](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a><span data-ttu-id="889d6-145">Компоненты служб</span><span class="sxs-lookup"><span data-stu-id="889d6-145">Service components</span></span>

<span data-ttu-id="889d6-146">Компонент службы [курсора для службы OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) дополняют функциональные возможности поставщиков данных поддержки курсора.</span><span class="sxs-lookup"><span data-stu-id="889d6-146">The [Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) service component supplements the cursor support functions of data providers.</span></span> <span data-ttu-id="889d6-147">Кроме того, требуется ключевое слово и динамическое свойство.</span><span class="sxs-lookup"><span data-stu-id="889d6-147">It also requires a keyword and has dynamic properties.</span></span>

<span data-ttu-id="889d6-148">Для получения дополнительных сведений о поставщиках обратитесь к документации Microsoft OLE DB в пакете SDK компонентов Microsoft Data Access или посетите [Центр разработчиков платформы данных](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="889d6-148">For more information about providers, see the documentation for Microsoft OLE DB in the Microsoft Data Access Components SDK or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

## <a name="provider-commands"></a><span data-ttu-id="889d6-149">Команды поставщика</span><span class="sxs-lookup"><span data-stu-id="889d6-149">Provider commands</span></span>

<span data-ttu-id="889d6-150">Для каждого поставщика, указанного здесь, если ваши приложения позволяют пользователям вводить инструкции SQL в качестве команд поставщика, необходимо всегда проверять данные, введенные пользователем, и вигилант возможных атак хакеров, используя потенциально опасные инструкции SQL, например, как часть вводимых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="889d6-150">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statement, such as, , as part of the user input.</span></span>

