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
ms.openlocfilehash: 69a4d25fc6a7abec68c94cc947e5944322d230a6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594952"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="2d071-103">Объекты состояния MAPI</span><span class="sxs-lookup"><span data-stu-id="2d071-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="2d071-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d071-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d071-105">Объекты состояния о сведения обо всех ресурсах MAPI.</span><span class="sxs-lookup"><span data-stu-id="2d071-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="2d071-106">Например поставщика услуг, процесс отправки и получения MAPI или в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="2d071-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="2d071-107">Имеется объект состояния, предоставление сведений о каждой отдельной службы поставщика текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="2d071-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="2d071-108">MAPI несет ответственность за внедрение объектов состояния для подсистемы, процесс отправки и получения MAPI и адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2d071-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="2d071-109">Объект состояния подсистемы предоставляет глобальные данные.</span><span class="sxs-lookup"><span data-stu-id="2d071-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="2d071-110">Объект состояния для встроенной адресной книги предоставляет состояние всех поставщиками адресной книги в настоящее время работы.</span><span class="sxs-lookup"><span data-stu-id="2d071-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="2d071-111">Каждый объект состояния включен в таблице состояния, таблицы, задаваемые с помощью интерфейса MAPI, который предоставляет клиентам все сведения о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="2d071-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="2d071-112">Для получения дополнительных сведений см [Состояние](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2d071-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="2d071-113">Клиенты могут доступ к объекту определенное состояние, либо из таблицы или для поставщика услуг, через возвращается объект входа в систему.</span><span class="sxs-lookup"><span data-stu-id="2d071-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="2d071-114">Например для доступа к объекту состояние поставщика адресных книг, клиент может вызвать **IABLogon::OpenStatusEntry**.</span><span class="sxs-lookup"><span data-stu-id="2d071-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="2d071-115">Для получения дополнительных сведений см [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="2d071-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="2d071-116">Клиенты могут использовать состояние объектов:</span><span class="sxs-lookup"><span data-stu-id="2d071-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="2d071-117">Сведения о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="2d071-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="2d071-118">Мониторинг поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2d071-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="2d071-119">Контроль передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="2d071-119">Control message transmission.</span></span>
    
- <span data-ttu-id="2d071-120">Просмотр или изменение конфигурации и состоянии ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d071-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="2d071-121">Каждый объект состояния реализует интерфейс **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="2d071-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="2d071-122">Дополнительные сведения можно [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="2d071-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="2d071-123">Тем не менее не каждый объект состояния полностью поддерживает все методы **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="2d071-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="2d071-124">Поскольку вариантов в методах, поддерживаемых приложением объект состояния, клиентам требуется сведения об объекте определенное состояние перед их можно использовать.</span><span class="sxs-lookup"><span data-stu-id="2d071-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="2d071-125">Состояние объектов необходимо опубликовать сведения о компонентах для их в следующие три свойства:</span><span class="sxs-lookup"><span data-stu-id="2d071-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="2d071-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d071-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="2d071-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d071-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="2d071-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d071-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="2d071-129">Дополнительные сведения о реализации объекта состояния [Реализация объекта состояния](status-object-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="2d071-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="2d071-130">Дополнительные сведения об использовании состояние объекта можно [таблице состояния и состояния объектов](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2d071-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

