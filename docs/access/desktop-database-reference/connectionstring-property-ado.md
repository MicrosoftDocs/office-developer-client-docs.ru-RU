---
title: Свойство ConnectionString (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3612652f3473c0794dbfe9be60f84ea2e3fee252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712731"
---
# <a name="connectionstring-property-ado"></a><span data-ttu-id="8e9f9-102">Свойство ConnectionString (ADO)</span><span class="sxs-lookup"><span data-stu-id="8e9f9-102">ConnectionString property (ADO)</span></span>


<span data-ttu-id="8e9f9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e9f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e9f9-104">Указывает сведения, используемые для установления подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-104">Indicates the information used to establish a connection to a data source.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8e9f9-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8e9f9-105">Settings and return values</span></span>

<span data-ttu-id="8e9f9-106">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e9f9-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="8e9f9-107">Remarks</span></span>

<span data-ttu-id="8e9f9-108">Свойство **ConnectionString** укажите источник данных, передав строку подробные подключения, содержащую последовательность операторов *= значение* *аргумента* , разделенные точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-108">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="8e9f9-109">ADO поддерживает пять аргументов для свойства **ConnectionString** ; любые другие аргументы передачи непосредственно к поставщику без какой-либо обработки с ADO.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-109">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO.</span></span> <span data-ttu-id="8e9f9-110">Поддерживает ADO аргументы, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-110">The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e9f9-111">Аргумент</span><span class="sxs-lookup"><span data-stu-id="8e9f9-111">Argument</span></span></p></th>
<th><p><span data-ttu-id="8e9f9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8e9f9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e9f9-113"><em>Поставщик =</em></span><span class="sxs-lookup"><span data-stu-id="8e9f9-113"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="8e9f9-114">Задает имя поставщика, который используется для подключения.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-114">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e9f9-115"><em>Имя файла =</em></span><span class="sxs-lookup"><span data-stu-id="8e9f9-115"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="8e9f9-116">Указывает имя файла от поставщика (например, объект источника постоянных данных), содержащий сведения о подключении к предварительно.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-116">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e9f9-117"><em>Удаленный поставщик =</em></span><span class="sxs-lookup"><span data-stu-id="8e9f9-117"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="8e9f9-118">Задает имя поставщика для использования при открытии подключения со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-118">Specifies the name of a provider to use when opening a client-side connection.</span></span> <span data-ttu-id="8e9f9-119">(Служба удаленных данных только.)</span><span class="sxs-lookup"><span data-stu-id="8e9f9-119">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e9f9-120"><em>Удаленный сервер =</em></span><span class="sxs-lookup"><span data-stu-id="8e9f9-120"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="8e9f9-121">Задает имя пути сервера, который будет использоваться при открытии подключения со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-121">Specifies the path name of the server to use when opening a client-side connection.</span></span> <span data-ttu-id="8e9f9-122">(Служба удаленных данных только.)</span><span class="sxs-lookup"><span data-stu-id="8e9f9-122">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e9f9-123"><em>URL-АДРЕС =</em></span><span class="sxs-lookup"><span data-stu-id="8e9f9-123"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="8e9f9-124">Указывает строку подключения, как абсолютный URL-адрес, идентифицирующий ресурс, такой как файл или папку.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-124">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8e9f9-125">После того как использовать свойство **ConnectionString** и откройте объект [подключения](connection-object-ado.md) поставщик может изменить содержимое свойства, например путем сопоставления имен аргументов определенные ADO с их эквивалентами поставщика.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-125">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="8e9f9-126">Свойство **ConnectionString** автоматически наследует значение, используемое для аргумента *ConnectionString* метод [Open](open-method-ado-connection.md) , можно переопределить свойство **ConnectionString** текущей во время вызова метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="8e9f9-126">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="8e9f9-127">Так как *Имя файла* для аргумента вызывает ADO для загрузки соответствующим поставщиком, нельзя передавать аргументы *поставщика* и *Имени файла* .</span><span class="sxs-lookup"><span data-stu-id="8e9f9-127">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="8e9f9-128">Свойство **ConnectionString** — чтение и запись при подключении закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-128">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="8e9f9-129">Дубликаты аргумент **создаваемая** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-129">Duplicates of an argument in the **ConnectionString** property are ignored.</span></span> <span data-ttu-id="8e9f9-130">Последний экземпляр любого аргумента используется.</span><span class="sxs-lookup"><span data-stu-id="8e9f9-130">The last instance of any argument is used.</span></span>

<span data-ttu-id="8e9f9-131">**Службы удаленных данных об использовании** При использовании на объект **подключения** со стороны клиента со значением свойства **ConnectionString** может включать только параметры *Удаленного поставщика* и *Удаленного сервера* .</span><span class="sxs-lookup"><span data-stu-id="8e9f9-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

