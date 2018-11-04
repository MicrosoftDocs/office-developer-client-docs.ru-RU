---
title: Метод CreateObject (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f622ee94fa6e37c2f618b038aea746791e58e9b8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950085"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="5176b-102">Метод CreateObject (RDS)</span><span class="sxs-lookup"><span data-stu-id="5176b-102">CreateObject method (RDS)</span></span>

<span data-ttu-id="5176b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5176b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5176b-104">Создает прокси-сервера для бизнес-конечного объекта и возвращает указатель на него.</span><span class="sxs-lookup"><span data-stu-id="5176b-104">Creates the proxy for the target business object and returns a pointer to it.</span></span> <span data-ttu-id="5176b-105">Прокси-сервер пакеты и выполняет маршалинг данные на стороне сервера заглушку взаимодействие с бизнес-объект для отправки запросов и данных через Интернет.</span><span class="sxs-lookup"><span data-stu-id="5176b-105">The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet.</span></span> <span data-ttu-id="5176b-106">Для объектов в процесс компонент не прокси-серверы используются, если только указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="5176b-106">For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="5176b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5176b-107">Syntax</span></span>

<span data-ttu-id="5176b-108">Служба удаленных данных поддерживает следующие протоколы: HTTP, HTTPS (HTTP через протокол SSL), DCOM и в процессе.</span><span class="sxs-lookup"><span data-stu-id="5176b-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5176b-109">Протокол</span><span class="sxs-lookup"><span data-stu-id="5176b-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="5176b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5176b-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5176b-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="5176b-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="5176b-112">Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="5176b-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5176b-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="5176b-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="5176b-114">Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="5176b-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5176b-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="5176b-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="5176b-116">Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>computername</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="5176b-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5176b-117">В работе</span><span class="sxs-lookup"><span data-stu-id="5176b-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="5176b-118">Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="5176b-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="5176b-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="5176b-119">Parameters</span></span>

|<span data-ttu-id="5176b-120">Параметр</span><span class="sxs-lookup"><span data-stu-id="5176b-120">Parameter</span></span>|<span data-ttu-id="5176b-121">Описание</span><span class="sxs-lookup"><span data-stu-id="5176b-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5176b-122">*Объект*</span><span class="sxs-lookup"><span data-stu-id="5176b-122">*Object*</span></span> |<span data-ttu-id="5176b-123">Объектная переменная, которое оценивается как объект, тип которого указан *идентификатор ProgID*.</span><span class="sxs-lookup"><span data-stu-id="5176b-123">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>|
|<span data-ttu-id="5176b-124">*Пространства данных*</span><span class="sxs-lookup"><span data-stu-id="5176b-124">*DataSpace*</span></span> |<span data-ttu-id="5176b-125">Объектную переменную, которая представляет [RDS. Пространства данных](dataspace-object-rds.md) используется для создания экземпляра объекта новый объект.</span><span class="sxs-lookup"><span data-stu-id="5176b-125">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>|
|<span data-ttu-id="5176b-126">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="5176b-126">*ProgID*</span></span> |<span data-ttu-id="5176b-127">**Строковое** значение, содержащее программный идентификатор, указав на сервере бизнес-объект, который реализует приложения бизнес-правил.</span><span class="sxs-lookup"><span data-stu-id="5176b-127">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>|
|<span data-ttu-id="5176b-128">*awebsrvr* или *имя компьютера*</span><span class="sxs-lookup"><span data-stu-id="5176b-128">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="5176b-129">**Строковое** значение, представляющее URL-адрес, идентифицирующий веб-сервер Internet Information Services (IIS), где создается экземпляр объекта business server.</span><span class="sxs-lookup"><span data-stu-id="5176b-129">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5176b-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="5176b-130">Remarks</span></span>

<span data-ttu-id="5176b-131">*Протокол HTTP* используется стандартный Интернет-протокола; *HTTPS* — это безопасный протокол.</span><span class="sxs-lookup"><span data-stu-id="5176b-131">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="5176b-132">Используйте *протокол DCOM* при выполнении локальной сети без HTTP.</span><span class="sxs-lookup"><span data-stu-id="5176b-132">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="5176b-133">Протокол *в процесс* является локальной библиотеки динамической компоновки (DLL); сети не используется.</span><span class="sxs-lookup"><span data-stu-id="5176b-133">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

