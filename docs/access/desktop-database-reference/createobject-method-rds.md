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
# <a name="createobject-method-rds"></a><span data-ttu-id="d229b-102">Метод CreateObject (RDS)</span><span class="sxs-lookup"><span data-stu-id="d229b-102">CreateObject method (RDS)</span></span>

<span data-ttu-id="d229b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d229b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d229b-104">Создает прокси-сервер для целевого бизнес-объекта и возвращает ему указатель.</span><span class="sxs-lookup"><span data-stu-id="d229b-104">Creates the proxy for the target business object and returns a pointer to it.</span></span> <span data-ttu-id="d229b-105">Прокси-пакеты и маршалы данных в серверную загонку для связи с бизнес-объектом для отправки запросов и данных через Интернет.</span><span class="sxs-lookup"><span data-stu-id="d229b-105">The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet.</span></span> <span data-ttu-id="d229b-106">Для используемых в процессе объектов компонентов не используются прокси, только указка на объект предоставляется.</span><span class="sxs-lookup"><span data-stu-id="d229b-106">For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="d229b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d229b-107">Syntax</span></span>

<span data-ttu-id="d229b-108">Служба удаленных данных поддерживает следующие протоколы: HTTP, HTTPS (http over Secure Socket Layer), DCOM и in-process.</span><span class="sxs-lookup"><span data-stu-id="d229b-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d229b-109">Протокол</span><span class="sxs-lookup"><span data-stu-id="d229b-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="d229b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d229b-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d229b-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="d229b-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="d229b-112">Установите<em>объект</em>  =  <em>DataSpace</em>. CreateObject &quot; <em>(ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="d229b-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d229b-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="d229b-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="d229b-114">Установите<em>объект</em>  =  <em>DataSpace</em>. CreateObject &quot; <em>(ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="d229b-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d229b-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="d229b-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="d229b-116">Установите<em>объект</em>  =  <em>DataSpace</em>. CreateObject &quot; <em>(ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="d229b-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d229b-117">В процессе</span><span class="sxs-lookup"><span data-stu-id="d229b-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="d229b-118">Установите<em>объект</em>  =  <em>DataSpace</em>. CreateObject &quot; <em>(ProgId</em> &quot; , &quot; &quot; )</span><span class="sxs-lookup"><span data-stu-id="d229b-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="d229b-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="d229b-119">Parameters</span></span>

|<span data-ttu-id="d229b-120">Параметр</span><span class="sxs-lookup"><span data-stu-id="d229b-120">Parameter</span></span>|<span data-ttu-id="d229b-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d229b-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d229b-122">*Object*</span><span class="sxs-lookup"><span data-stu-id="d229b-122">*Object*</span></span> |<span data-ttu-id="d229b-123">Переменная объекта, которая оценивает объект, который является типом, указанным в *ProgID.*</span><span class="sxs-lookup"><span data-stu-id="d229b-123">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>|
|<span data-ttu-id="d229b-124">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="d229b-124">*DataSpace*</span></span> |<span data-ttu-id="d229b-125">Переменная объекта, представляюая [RDS. Объект DataSpace,](dataspace-object-rds.md) используемый для создания экземпляра нового объекта.</span><span class="sxs-lookup"><span data-stu-id="d229b-125">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>|
|<span data-ttu-id="d229b-126">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="d229b-126">*ProgID*</span></span> |<span data-ttu-id="d229b-127">Значение **String,** содержаное программный идентификатор, указывающий бизнес-объект на стороне сервера, реализующий бизнес-правила приложения.</span><span class="sxs-lookup"><span data-stu-id="d229b-127">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>|
|<span data-ttu-id="d229b-128">*awebsrvr или* *computername*</span><span class="sxs-lookup"><span data-stu-id="d229b-128">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="d229b-129">Значение **String,** представляю которое представляет URL-адрес, идентифицирующий веб-сервер службы IIS (IIS), на котором создается экземпляр бизнес-объекта сервера.</span><span class="sxs-lookup"><span data-stu-id="d229b-129">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d229b-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="d229b-130">Remarks</span></span>

<span data-ttu-id="d229b-131">Протокол *HTTP является* стандартным веб-протоколом; *HTTPS* — это безопасный веб-протокол.</span><span class="sxs-lookup"><span data-stu-id="d229b-131">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="d229b-132">Используйте протокол *DCOM при* работе с локальной сетью без HTTP.</span><span class="sxs-lookup"><span data-stu-id="d229b-132">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="d229b-133">Протокол *в процессе —* это локализованная библиотека динамических ссылок (DLL); он не использует сеть.</span><span class="sxs-lookup"><span data-stu-id="d229b-133">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

