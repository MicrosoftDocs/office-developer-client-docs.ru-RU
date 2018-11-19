---
title: Приложение А. Поставщики
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45416c68d52a2ba20ba9adfa19a6ebd89d1e0240
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026206"
---
# <a name="appendix-a-providers"></a><span data-ttu-id="1cf73-102">Приложение А. Поставщики</span><span class="sxs-lookup"><span data-stu-id="1cf73-102">Appendix A: Providers</span></span>


<span data-ttu-id="1cf73-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cf73-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1cf73-104">В данном разделе описываются три вида поставщиков: поставщики данных, поставщиков услуг и компоненты службы.</span><span class="sxs-lookup"><span data-stu-id="1cf73-104">This section addresses three kinds of providers: data providers, service providers, and service components.</span></span> <span data-ttu-id="1cf73-105">Поставщики могут быть разделены на две категории: те, предоставляя данные и те, обеспечивающих работу служб.</span><span class="sxs-lookup"><span data-stu-id="1cf73-105">Providers fall into two categories: those providing data and those providing services.</span></span> <span data-ttu-id="1cf73-106">*Поставщик данных* несет ответственность за свои собственные данные и предоставляет доступ к нему в виде таблицы в приложение.</span><span class="sxs-lookup"><span data-stu-id="1cf73-106">A *data provider* owns its own data and exposes it in tabular form to your application.</span></span> <span data-ttu-id="1cf73-107">*Поставщик услуг* инкапсулирует службы путем создания и использования данных, дополнения функции в приложениях ADO.</span><span class="sxs-lookup"><span data-stu-id="1cf73-107">A *service provider* encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="1cf73-108">Поставщик службы может также быть разбить как *компонент службы*, которым необходимо работать совместно с другими поставщиками услуг или компоненты.</span><span class="sxs-lookup"><span data-stu-id="1cf73-108">A service provider may also be further defined as a *service component*, which must work in conjunction with other service providers or components.</span></span>

## <a name="data-providers"></a><span data-ttu-id="1cf73-109">Поставщики данных</span><span class="sxs-lookup"><span data-stu-id="1cf73-109">Data providers</span></span>

<span data-ttu-id="1cf73-110">ADO мощные и гибкие, так как он может подключиться к любой из нескольких разных поставщиков данных и по-прежнему предоставляют доступ к той же модели программирования, вне зависимости от конкретных компонентов любого заданного поставщика.</span><span class="sxs-lookup"><span data-stu-id="1cf73-110">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span>

<span data-ttu-id="1cf73-111">Тем не менее так как каждый поставщик данных является уникальным, как приложение взаимодействует с ADO будет отличаться поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="1cf73-111">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider.</span></span> <span data-ttu-id="1cf73-112">Различия обычно делятся на три категории.</span><span class="sxs-lookup"><span data-stu-id="1cf73-112">The differences usually fall into one of three categories:</span></span>

- <span data-ttu-id="1cf73-113">Параметры подключения в свойстве [ConnectionString](connectionstring-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf73-113">Connection parameters in the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

- <span data-ttu-id="1cf73-114">Использование объекта [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf73-114">[Command](command-object-ado.md) object usage.</span></span>

- <span data-ttu-id="1cf73-115">Поставщик поведение [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf73-115">Provider-specific [Recordset](recordset-object-ado.md) behavior.</span></span>

<span data-ttu-id="1cf73-116">Подробные сведения для каждого из поставщиков данных, доступные в настоящее время корпорацией Майкрософт перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="1cf73-116">Details for each of the data providers currently available from Microsoft are listed as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cf73-117">Область</span><span class="sxs-lookup"><span data-stu-id="1cf73-117">Area</span></span></p></th>
<th><p><span data-ttu-id="1cf73-118">Статья</span><span class="sxs-lookup"><span data-stu-id="1cf73-118">Topic</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cf73-119">Базы данных ODBC</span><span class="sxs-lookup"><span data-stu-id="1cf73-119">ODBC databases</span></span></p></td>
<td><p><span data-ttu-id="1cf73-120"><a href="microsoft-ole-db-provider-for-odbc.md">Поставщик Microsoft OLE DB для ODBC</a></span><span class="sxs-lookup"><span data-stu-id="1cf73-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cf73-121">Служба индексирования</span><span class="sxs-lookup"><span data-stu-id="1cf73-121">Microsoft Indexing Service</span></span></p></td>
<td><p><span data-ttu-id="1cf73-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Поставщик Microsoft OLE DB для службы индексирования (Майкрософт)</a></span><span class="sxs-lookup"><span data-stu-id="1cf73-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cf73-123">Службы Microsoft Active Directory</span><span class="sxs-lookup"><span data-stu-id="1cf73-123">Microsoft Active Directory Service</span></span></p></td>
<td><p><span data-ttu-id="1cf73-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Поставщик Microsoft OLE DB для службы Microsoft Active Directory</a></span><span class="sxs-lookup"><span data-stu-id="1cf73-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cf73-125">Базы данных Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="1cf73-125">Microsoft Jet databases</span></span></p></td>
<td><p><span data-ttu-id="1cf73-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Поставщик Microsoft OLE DB для Microsoft Jet</a></span><span class="sxs-lookup"><span data-stu-id="1cf73-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cf73-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="1cf73-127">Microsoft SQL Server</span></span></p></td>
<td><p><span data-ttu-id="1cf73-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Поставщик Microsoft OLE DB для SQL Server</a></span><span class="sxs-lookup"><span data-stu-id="1cf73-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cf73-129">Базы данных Oracle</span><span class="sxs-lookup"><span data-stu-id="1cf73-129">Oracle databases</span></span></p></td>
<td><p><span data-ttu-id="1cf73-130"><a href="microsoft-ole-db-provider-for-oracle.md">Поставщик Microsoft OLE DB для Oracle</a></span><span class="sxs-lookup"><span data-stu-id="1cf73-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cf73-131">Публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="1cf73-131">Internet Publishing</span></span></p></td>
<td><p><span data-ttu-id="1cf73-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации в Интернете</a></span><span class="sxs-lookup"><span data-stu-id="1cf73-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a><span data-ttu-id="1cf73-133">Динамические свойства от поставщика</span><span class="sxs-lookup"><span data-stu-id="1cf73-133">Provider-specific dynamic properties</span></span>

<span data-ttu-id="1cf73-134">Коллекции [свойств](properties-collection-ado.md) объектов [подключения](connection-object-ado.md), [команды](command-object-ado.md)и [набора записей](recordset-object-ado.md) включают динамических свойств, относящихся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="1cf73-134">The [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), and [Recordset](recordset-object-ado.md) objects include dynamic properties specific to the provider.</span></span> <span data-ttu-id="1cf73-135">Эти свойства предоставляют информацию о функциональные возможности к поставщику за пределы встроенных свойств, которые поддерживает ADO.</span><span class="sxs-lookup"><span data-stu-id="1cf73-135">These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</span></span>

<span data-ttu-id="1cf73-136">После подключения к и создания этих объектов, используйте метод [Refresh](refresh-method-ado.md) в коллекции **свойств** объекта для получения свойства от поставщика.</span><span class="sxs-lookup"><span data-stu-id="1cf73-136">After establishing the connection and creating these objects, use the [Refresh](refresh-method-ado.md) method on the object's **Properties** collection to obtain the provider-specific properties.</span></span> <span data-ttu-id="1cf73-137">Обратитесь к документации поставщика и Справочник программиста OLE DB для получения дополнительных сведений об этих динамических свойств.</span><span class="sxs-lookup"><span data-stu-id="1cf73-137">Refer to the provider documentation and the OLE DB Programmer's Reference for detailed information about these dynamic properties.</span></span>

## <a name="service-providers"></a><span data-ttu-id="1cf73-138">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="1cf73-138">Service providers</span></span>

<span data-ttu-id="1cf73-139">Чтобы использовать поставщика услуг, необходимо указать ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="1cf73-139">To use a service provider, you must supply a keyword.</span></span> <span data-ttu-id="1cf73-140">Кроме того, необходимо принять во внимание от поставщика динамические свойства, связанные с каждой поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="1cf73-140">You should also be aware of the provider-specific dynamic properties associated with each service provider.</span></span> <span data-ttu-id="1cf73-141">Сведения от поставщика, приведены для каждого из поставщиков услуг, доступные в настоящее время корпорации Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="1cf73-141">Provider-specific details are listed for each of the service providers currently available from Microsoft:</span></span>

- [<span data-ttu-id="1cf73-142">Microsoft службы формирования данных для OLE DB</span><span class="sxs-lookup"><span data-stu-id="1cf73-142">Microsoft Data Shaping Service for OLE DB</span></span>](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [<span data-ttu-id="1cf73-143">Сохраняемость поставщик Microsoft OLE DB</span><span class="sxs-lookup"><span data-stu-id="1cf73-143">Microsoft OLE DB Persistence Provider</span></span>](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [<span data-ttu-id="1cf73-144">Поставщик Microsoft OLE DB удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="1cf73-144">Microsoft OLE DB Remoting Provider</span></span>](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a><span data-ttu-id="1cf73-145">Компоненты службы</span><span class="sxs-lookup"><span data-stu-id="1cf73-145">Service components</span></span>

<span data-ttu-id="1cf73-146">Компонент службы [Служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) дополняет функции поддержки курсора поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="1cf73-146">The [Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) service component supplements the cursor support functions of data providers.</span></span> <span data-ttu-id="1cf73-147">Он также требует использования ключевого слова и имеет динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="1cf73-147">It also requires a keyword and has dynamic properties.</span></span>

<span data-ttu-id="1cf73-148">Дополнительные сведения о поставщиках обратитесь к документации по Microsoft OLE DB в пакете SDK компонентов доступа к данным Microsoft или посетите [Центр разработчиков данных платформы](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="1cf73-148">For more information about providers, see the documentation for Microsoft OLE DB in the Microsoft Data Access Components SDK or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

## <a name="provider-commands"></a><span data-ttu-id="1cf73-149">Команды поставщика</span><span class="sxs-lookup"><span data-stu-id="1cf73-149">Provider commands</span></span>

<span data-ttu-id="1cf73-150">Для каждого поставщика в списке, если ваши приложения позволяют пользователям вводить инструкции SQL как команды поставщика, необходимо всегда вводимых пользователем и быть бдительность возможные злоумышленник атак с помощью потенциально опасных инструкции SQL, например, как часть Ввод данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="1cf73-150">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statement, such as, , as part of the user input.</span></span>

