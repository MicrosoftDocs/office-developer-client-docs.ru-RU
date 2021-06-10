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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295711"
---
# <a name="connectionstring-property-ado"></a><span data-ttu-id="cfadd-102">Свойство ConnectionString (ADO)</span><span class="sxs-lookup"><span data-stu-id="cfadd-102">ConnectionString property (ADO)</span></span>


<span data-ttu-id="cfadd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfadd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfadd-104">Указывает сведения, используемые для установления подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="cfadd-104">Indicates the information used to establish a connection to a data source.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cfadd-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="cfadd-105">Settings and return values</span></span>

<span data-ttu-id="cfadd-106">Задает или возвращает значение **String.**</span><span class="sxs-lookup"><span data-stu-id="cfadd-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfadd-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="cfadd-107">Remarks</span></span>

<span data-ttu-id="cfadd-108">Используйте **свойство ConnectionString,** чтобы указать источник данных, передав подробную строку подключения, содержащую серию аргументов  *=* утверждения значений, разделенных зайколонами.</span><span class="sxs-lookup"><span data-stu-id="cfadd-108">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="cfadd-109">ADO поддерживает пять аргументов для свойства **ConnectionString;** любые другие аргументы передаются непосредственно поставщику без обработки ADO.</span><span class="sxs-lookup"><span data-stu-id="cfadd-109">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO.</span></span> <span data-ttu-id="cfadd-110">Аргументы, поддерживаемые ADO, следуют следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cfadd-110">The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfadd-111">Аргументация</span><span class="sxs-lookup"><span data-stu-id="cfadd-111">Argument</span></span></p></th>
<th><p><span data-ttu-id="cfadd-112">Description</span><span class="sxs-lookup"><span data-stu-id="cfadd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfadd-113"><em>Provider=</em></span><span class="sxs-lookup"><span data-stu-id="cfadd-113"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="cfadd-114">Задает имя поставщика, чтобы использовать для подключения.</span><span class="sxs-lookup"><span data-stu-id="cfadd-114">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfadd-115"><em>Имя файла=</em></span><span class="sxs-lookup"><span data-stu-id="cfadd-115"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="cfadd-116">Указывает имя файла, соответствующего поставщику (например, исходный объект сохраненных данных), содержащий предварительно заданные сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="cfadd-116">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfadd-117"><em>Удаленный поставщик=</em></span><span class="sxs-lookup"><span data-stu-id="cfadd-117"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="cfadd-118">Указывает имя поставщика, используемого при открытии клиентского подключения.</span><span class="sxs-lookup"><span data-stu-id="cfadd-118">Specifies the name of a provider to use when opening a client-side connection.</span></span> <span data-ttu-id="cfadd-119">(Только служба удаленных данных.)</span><span class="sxs-lookup"><span data-stu-id="cfadd-119">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfadd-120"><em>Удаленный сервер=</em></span><span class="sxs-lookup"><span data-stu-id="cfadd-120"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="cfadd-121">Указывает имя пути сервера, используемого при открытии клиентского подключения.</span><span class="sxs-lookup"><span data-stu-id="cfadd-121">Specifies the path name of the server to use when opening a client-side connection.</span></span> <span data-ttu-id="cfadd-122">(Только служба удаленных данных.)</span><span class="sxs-lookup"><span data-stu-id="cfadd-122">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfadd-123"><em>URL=</em></span><span class="sxs-lookup"><span data-stu-id="cfadd-123"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="cfadd-124">Указывает строку подключения как абсолютный URL-адрес, определяющий ресурс, например файл или папку.</span><span class="sxs-lookup"><span data-stu-id="cfadd-124">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cfadd-125">После задания свойства **ConnectionString** и открытия объекта [Подключения](connection-object-ado.md) поставщик может изменить содержимое свойства, например, с помощью сопоставления имен аргументов, определенных ADO, с эквивалентами поставщика.</span><span class="sxs-lookup"><span data-stu-id="cfadd-125">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="cfadd-126">Свойство **ConnectionString** автоматически наследует значение, используемого для аргумента *ConnectionString* метода Open, поэтому можно переопрепредить текущее свойство **ConnectionString** во время вызова метода **Open.** [](open-method-ado-connection.md)</span><span class="sxs-lookup"><span data-stu-id="cfadd-126">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="cfadd-127">Так как *аргумент Имя файла* вызывает загрузку ADO связанного поставщика, вы не можете передать аргументы *поставщика* и *имени* файлов.</span><span class="sxs-lookup"><span data-stu-id="cfadd-127">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="cfadd-128">Свойство **ConnectionString** считыв или записывалось при закрытии подключения и только для чтения, когда оно открыто.</span><span class="sxs-lookup"><span data-stu-id="cfadd-128">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="cfadd-129">Дубликаты аргумента в **свойстве ConnectionString** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="cfadd-129">Duplicates of an argument in the **ConnectionString** property are ignored.</span></span> <span data-ttu-id="cfadd-130">Используется последний экземпляр любого аргумента.</span><span class="sxs-lookup"><span data-stu-id="cfadd-130">The last instance of any argument is used.</span></span>

<span data-ttu-id="cfadd-131">**Удаленное использование службы данных** При этом свойство **ConnectionString** может включать только параметры  удаленного поставщика и  *удаленного* сервера.</span><span class="sxs-lookup"><span data-stu-id="cfadd-131">**Remote Data Service Usage** When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

