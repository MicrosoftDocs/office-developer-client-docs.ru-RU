---
title: CreateObject Method (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ff2381626e8cf81aa95ee9d49f9396bd4b0316
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602722"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="cba01-102">CreateObject Method (RDS)</span><span class="sxs-lookup"><span data-stu-id="cba01-102">CreateObject Method (RDS)</span></span>


<span data-ttu-id="cba01-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cba01-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="cba01-104">Создает прокси-сервера для бизнес-конечного объекта и возвращает указатель на него.</span><span class="sxs-lookup"><span data-stu-id="cba01-104">Creates the proxy for the target business object and returns a pointer to it.</span></span> <span data-ttu-id="cba01-105">Прокси-сервер пакеты и выполняет маршалинг данные на стороне сервера заглушку взаимодействие с бизнес-объект для отправки запросов и данных через Интернет.</span><span class="sxs-lookup"><span data-stu-id="cba01-105">The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet.</span></span> <span data-ttu-id="cba01-106">Для объектов в процесс компонент не прокси-серверы используются, если только указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="cba01-106">For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba01-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cba01-107">Syntax</span></span>

<span data-ttu-id="cba01-108">Служба удаленных данных поддерживает следующие протоколы: HTTP, HTTPS (HTTP через протокол SSL), DCOM и в процессе.</span><span class="sxs-lookup"><span data-stu-id="cba01-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cba01-109">Протокол</span><span class="sxs-lookup"><span data-stu-id="cba01-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="cba01-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cba01-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cba01-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="cba01-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="cba01-112">Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="cba01-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cba01-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="cba01-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="cba01-114">Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="cba01-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cba01-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="cba01-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="cba01-116">Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>computername</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="cba01-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cba01-117">В работе</span><span class="sxs-lookup"><span data-stu-id="cba01-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="cba01-118">Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="cba01-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="cba01-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="cba01-119">Parameters</span></span>

  - <span data-ttu-id="cba01-120">*Объект*</span><span class="sxs-lookup"><span data-stu-id="cba01-120">*Object*</span></span>

  - <span data-ttu-id="cba01-121">Объектная переменная, которое оценивается как объект, тип которого указан *идентификатор ProgID*.</span><span class="sxs-lookup"><span data-stu-id="cba01-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="cba01-122">*Пространства данных*</span><span class="sxs-lookup"><span data-stu-id="cba01-122">*DataSpace*</span></span>

  - <span data-ttu-id="cba01-123">Объектную переменную, которая представляет [RDS. Пространства данных](dataspace-object-rds.md) используется для создания экземпляра объекта новый объект.</span><span class="sxs-lookup"><span data-stu-id="cba01-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="cba01-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="cba01-124">*ProgID*</span></span>

  - <span data-ttu-id="cba01-125">**Строковое** значение, содержащее программный идентификатор, указав на сервере бизнес-объект, который реализует приложения бизнес-правил.</span><span class="sxs-lookup"><span data-stu-id="cba01-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="cba01-126">*awebsrvr* или *имя компьютера*</span><span class="sxs-lookup"><span data-stu-id="cba01-126">*awebsrvr* or *computername*</span></span>

<span data-ttu-id="cba01-127"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="cba01-127"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="cba01-128">**Строковое** значение, представляющее URL-адрес, идентифицирующий Internet Information Services (IIS) веб-сервере, где создается экземпляр объекта business server.</span><span class="sxs-lookup"><span data-stu-id="cba01-128">A **String** value that represents a URL identifying the Internet Information Services (IIS) Web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba01-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="cba01-129">Remarks</span></span>

<a name="the-http-protocol-is-the-standard-web-protocol-https-is-a-secure-web-protocol-use-the-dcom-protocol-when-running-a-local-area-network-without-http-the-in-process-protocol-is-a-local-dynamic-link-library-dll-it-does-not-use-a-network"></a><span data-ttu-id="cba01-130">*Протокол HTTP* является протоколом Web; *HTTPS* является безопасной Интернет-протокола.</span><span class="sxs-lookup"><span data-stu-id="cba01-130">The *HTTP protocol* is the standard Web protocol; *HTTPS* is a secure Web protocol.</span></span> <span data-ttu-id="cba01-131">Используйте *протокол DCOM* при выполнении локальной сети без HTTP.</span><span class="sxs-lookup"><span data-stu-id="cba01-131">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="cba01-132">Протокол *в процесс* является локальной библиотеки динамической компоновки (DLL); сети не используется.</span><span class="sxs-lookup"><span data-stu-id="cba01-132">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>
=======
  - <span data-ttu-id="cba01-133">**Строковое** значение, представляющее URL-адрес, идентифицирующий веб-сервер Internet Information Services (IIS), где создается экземпляр объекта business server.</span><span class="sxs-lookup"><span data-stu-id="cba01-133">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba01-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="cba01-134">Remarks</span></span>

<span data-ttu-id="cba01-135">*Протокол HTTP* используется стандартный Интернет-протокола; *HTTPS* — это безопасный протокол.</span><span class="sxs-lookup"><span data-stu-id="cba01-135">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="cba01-136">Используйте *протокол DCOM* при выполнении локальной сети без HTTP.</span><span class="sxs-lookup"><span data-stu-id="cba01-136">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="cba01-137">Протокол *в процесс* является локальной библиотеки динамической компоновки (DLL); сети не используется.</span><span class="sxs-lookup"><span data-stu-id="cba01-137">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>
>>>>>>> <span data-ttu-id="cba01-138">master</span><span class="sxs-lookup"><span data-stu-id="cba01-138">master</span></span>

