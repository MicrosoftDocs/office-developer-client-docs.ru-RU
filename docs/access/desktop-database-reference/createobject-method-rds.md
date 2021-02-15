---
title: Метод CreateObject (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295375"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="9e4cd-102">Метод CreateObject (RDS)</span><span class="sxs-lookup"><span data-stu-id="9e4cd-102">CreateObject method (RDS)</span></span>

<span data-ttu-id="9e4cd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e4cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e4cd-104">Создает прокси для целевого бизнес-объекта и возвращает на него указатель.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-104">Creates the proxy for the target business object and returns a pointer to it.</span></span> <span data-ttu-id="9e4cd-105">Прокси-сервер упаковывает и маршалит данные на серверной загоне для связи с бизнес-объектом для отправки запросов и данных через Интернет.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-105">The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet.</span></span> <span data-ttu-id="9e4cd-106">Для объектов компонентов, используемых в процессе, прокси не используются, предоставляется только указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-106">For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e4cd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e4cd-107">Syntax</span></span>

<span data-ttu-id="9e4cd-108">Удаленная служба данных поддерживает следующие протоколы: HTTP, HTTPS (http over Secure Socket Layer), DCOM и в процессе.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e4cd-109">Протокол</span><span class="sxs-lookup"><span data-stu-id="9e4cd-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="9e4cd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e4cd-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e4cd-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="9e4cd-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="9e4cd-112">Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="9e4cd-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4cd-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9e4cd-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="9e4cd-114">Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="9e4cd-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4cd-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="9e4cd-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="9e4cd-116">Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="9e4cd-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4cd-117">In-process</span><span class="sxs-lookup"><span data-stu-id="9e4cd-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="9e4cd-118">Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; &quot; )</span><span class="sxs-lookup"><span data-stu-id="9e4cd-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="9e4cd-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e4cd-119">Parameters</span></span>

|<span data-ttu-id="9e4cd-120">Параметр</span><span class="sxs-lookup"><span data-stu-id="9e4cd-120">Parameter</span></span>|<span data-ttu-id="9e4cd-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9e4cd-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9e4cd-122">*Object*</span><span class="sxs-lookup"><span data-stu-id="9e4cd-122">*Object*</span></span> |<span data-ttu-id="9e4cd-123">Объектная переменная, оцениваемая для объекта, который является типом, указанным в *ProgID.*</span><span class="sxs-lookup"><span data-stu-id="9e4cd-123">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>|
|<span data-ttu-id="9e4cd-124">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="9e4cd-124">*DataSpace*</span></span> |<span data-ttu-id="9e4cd-125">Объектная переменная, представляюная [RDS. Объект DataSpace,](dataspace-object-rds.md) используемый для создания экземпляра нового объекта.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-125">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>|
|<span data-ttu-id="9e4cd-126">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="9e4cd-126">*ProgID*</span></span> |<span data-ttu-id="9e4cd-127">**Строка,** которая содержит программный идентификатор, определяющий серверный бизнес-объект, реализующий бизнес-правила приложения.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-127">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>|
|<span data-ttu-id="9e4cd-128">*awebsrvr* или *имя компьютера*</span><span class="sxs-lookup"><span data-stu-id="9e4cd-128">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="9e4cd-129">**Строковые** значения, которые представляют URL-адрес, идентифицирующий веб-сервер служб IIS, на котором создается экземпляр бизнес-объекта сервера.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-129">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9e4cd-130">Заметки</span><span class="sxs-lookup"><span data-stu-id="9e4cd-130">Remarks</span></span>

<span data-ttu-id="9e4cd-131">Протокол *HTTP является* стандартным веб-протоколом; *HTTPS* — это безопасный веб-протокол.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-131">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="9e4cd-132">Используйте протокол *DCOM при* запуске локальной сети без протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-132">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="9e4cd-133">Этот *протокол является* локальной библиотекой динамической ссылки (DLL); Он не использует сеть.</span><span class="sxs-lookup"><span data-stu-id="9e4cd-133">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

