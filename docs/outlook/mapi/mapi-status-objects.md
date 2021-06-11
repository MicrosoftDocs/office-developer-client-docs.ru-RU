---
title: Объекты состояния MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406747"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="bf33e-103">Объекты состояния MAPI</span><span class="sxs-lookup"><span data-stu-id="bf33e-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="bf33e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf33e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf33e-105">Объекты status сообщают сведения о ресурсах MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf33e-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="bf33e-106">Например, поставщик услуг, процесс отправки и получения MAPI или адресная книга.</span><span class="sxs-lookup"><span data-stu-id="bf33e-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="bf33e-107">В текущем профиле имеется объект состояния, поставляющий сведения о каждом отдельном поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="bf33e-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="bf33e-108">MAPI отвечает за реализацию объектов состояния для подсистемы, процесса отправки и получения MAPI и адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bf33e-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="bf33e-109">Объект состояния подсистемы поставляет глобальную информацию.</span><span class="sxs-lookup"><span data-stu-id="bf33e-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="bf33e-110">Объект состояния интегрированной адресной книги обеспечивает состояние всех действующих поставщиков адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bf33e-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="bf33e-111">Каждый объект состояния включен в таблицу состояния, таблицу, поддерживаемую MAPI, которая предоставляет клиентам всю информацию о состоянии для сеанса.</span><span class="sxs-lookup"><span data-stu-id="bf33e-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="bf33e-112">Дополнительные сведения см. в [таблице Status Tables.](status-tables.md)</span><span class="sxs-lookup"><span data-stu-id="bf33e-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="bf33e-113">Клиенты могут получить доступ к определенному объекту состояния либо через таблицу, либо для поставщика услуг через его объект logon.</span><span class="sxs-lookup"><span data-stu-id="bf33e-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="bf33e-114">Например, чтобы получить доступ к объекту состояния поставщика адресной книги, клиент может вызвать **IABLogon::OpenStatusEntry.**</span><span class="sxs-lookup"><span data-stu-id="bf33e-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="bf33e-115">Дополнительные сведения см. [в iABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="bf33e-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="bf33e-116">Клиенты могут использовать объекты состояния для:</span><span class="sxs-lookup"><span data-stu-id="bf33e-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="bf33e-117">Узнайте о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="bf33e-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="bf33e-118">Мониторинг поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="bf33e-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="bf33e-119">Контроль передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="bf33e-119">Control message transmission.</span></span>
    
- <span data-ttu-id="bf33e-120">Просмотр или изменение конфигурации и состояния ресурса.</span><span class="sxs-lookup"><span data-stu-id="bf33e-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="bf33e-121">Каждый объект состояния реализует **интерфейс IMAPIStatus.**</span><span class="sxs-lookup"><span data-stu-id="bf33e-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="bf33e-122">Дополнительные сведения см. [в iMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="bf33e-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="bf33e-123">Однако не каждый объект состояния полностью поддерживает **каждый метод IMAPIStatus.**</span><span class="sxs-lookup"><span data-stu-id="bf33e-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="bf33e-124">Поскольку существуют различия в методах, поддерживаемых объектом состояния, клиентам необходимо узнать об определенном объекте состояния, прежде чем использовать его.</span><span class="sxs-lookup"><span data-stu-id="bf33e-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="bf33e-125">Объекты status должны публиковать сведения о своих свойствах в следующих трех свойствах:</span><span class="sxs-lookup"><span data-stu-id="bf33e-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="bf33e-126">**PR_RESOURCE_METHODS** [(PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bf33e-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="bf33e-127">**PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bf33e-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="bf33e-128">**PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bf33e-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="bf33e-129">Дополнительные сведения о реализации объекта состояния см. в дополнительных [сведениях о реализации объектов status.](status-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="bf33e-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="bf33e-130">Дополнительные сведения об использовании объекта состояния см. в таблице [status Table и Status Objects.](status-table-and-status-objects.md)</span><span class="sxs-lookup"><span data-stu-id="bf33e-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

