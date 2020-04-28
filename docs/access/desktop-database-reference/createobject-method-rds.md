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
# <a name="createobject-method-rds"></a><span data-ttu-id="876ce-102">Метод CreateObject (RDS)</span><span class="sxs-lookup"><span data-stu-id="876ce-102">CreateObject method (RDS)</span></span>

<span data-ttu-id="876ce-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="876ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="876ce-104">Создает прокси-сервер для целевого бизнес-объекта и возвращает указатель на него.</span><span class="sxs-lookup"><span data-stu-id="876ce-104">Creates the proxy for the target business object and returns a pointer to it.</span></span> <span data-ttu-id="876ce-105">Пакеты прокси-сервера и маршалирует данные в заглушку на стороне сервера для связи с бизнес-объектами для отправки запросов и данных через Интернет.</span><span class="sxs-lookup"><span data-stu-id="876ce-105">The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet.</span></span> <span data-ttu-id="876ce-106">Для объектов внутрипроцессного компонента не используются прокси-серверы, предоставляется только указатель на этот объект.</span><span class="sxs-lookup"><span data-stu-id="876ce-106">For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="876ce-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="876ce-107">Syntax</span></span>

<span data-ttu-id="876ce-108">Удаленная служба данных поддерживает следующие протоколы: HTTP, HTTPS (HTTP over SSL Layer), DCOM и внутрипроцессный.</span><span class="sxs-lookup"><span data-stu-id="876ce-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="876ce-109">Протокол</span><span class="sxs-lookup"><span data-stu-id="876ce-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="876ce-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="876ce-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="876ce-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="876ce-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="876ce-112">Задайте<em>объектное</em> = <em>пространство</em>. CreateObject (&quot;<em>ProgID</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</span><span class="sxs-lookup"><span data-stu-id="876ce-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="876ce-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="876ce-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="876ce-114">Задайте<em>объектное</em> = <em>пространство</em>. CreateObject (&quot;<em>ProgID</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</span><span class="sxs-lookup"><span data-stu-id="876ce-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="876ce-115">ТРАФИК</span><span class="sxs-lookup"><span data-stu-id="876ce-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="876ce-116">Задайте<em>объектное</em> = <em>пространство</em>. CreateObject (&quot;<em>ProgID</em>&quot;, &quot; <em>ComputerName</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="876ce-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="876ce-117">Внутрипроцессный</span><span class="sxs-lookup"><span data-stu-id="876ce-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="876ce-118">Задайте<em>объектное</em> = <em>пространство</em>. CreateObject (&quot;<em>ProgID</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="876ce-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="876ce-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="876ce-119">Parameters</span></span>

|<span data-ttu-id="876ce-120">Параметр</span><span class="sxs-lookup"><span data-stu-id="876ce-120">Parameter</span></span>|<span data-ttu-id="876ce-121">Описание</span><span class="sxs-lookup"><span data-stu-id="876ce-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="876ce-122">*Object*</span><span class="sxs-lookup"><span data-stu-id="876ce-122">*Object*</span></span> |<span data-ttu-id="876ce-123">Объектная переменная, которая оценивается как объект, который является типом, указанным в параметре *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="876ce-123">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>|
|<span data-ttu-id="876ce-124">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="876ce-124">*DataSpace*</span></span> |<span data-ttu-id="876ce-125">Объектная переменная, представляющая [RDS. Объект Space](dataspace-object-rds.md) , используемый для создания экземпляра нового объекта.</span><span class="sxs-lookup"><span data-stu-id="876ce-125">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>|
|<span data-ttu-id="876ce-126">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="876ce-126">*ProgID*</span></span> |<span data-ttu-id="876ce-127">**Строковое** значение, содержащее программный идентификатор, указывающий на серверный бизнес-объект, который реализует бизнес-правила приложения.</span><span class="sxs-lookup"><span data-stu-id="876ce-127">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>|
|<span data-ttu-id="876ce-128">*авебсрвр* или *ComputerName*</span><span class="sxs-lookup"><span data-stu-id="876ce-128">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="876ce-129">**Строковое** значение, представляющее URL-адрес, определяющий веб-сервер служб IIS, на котором создается экземпляр бизнес-объекта сервера.</span><span class="sxs-lookup"><span data-stu-id="876ce-129">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="876ce-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="876ce-130">Remarks</span></span>

<span data-ttu-id="876ce-131">*Http-протокол* является стандартным веб-протоколом; *HTTPS* — это безопасный веб-протокол.</span><span class="sxs-lookup"><span data-stu-id="876ce-131">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="876ce-132">Используйте *протокол DCOM* при работе с локальной сетью без протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="876ce-132">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="876ce-133">*Внутрипроцессный* протокол — это локальная библиотека динамической КОМПОНОВКИ (DLL); она не использует сеть.</span><span class="sxs-lookup"><span data-stu-id="876ce-133">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

