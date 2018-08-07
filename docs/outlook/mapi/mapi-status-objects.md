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
ms.openlocfilehash: f5b48f8cd4ef6ff41733ec9a18d1ab682f5e6bcb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809848"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="2153b-103">Объекты состояния MAPI</span><span class="sxs-lookup"><span data-stu-id="2153b-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="2153b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2153b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2153b-105">Объекты состояния о сведения обо всех ресурсах MAPI.</span><span class="sxs-lookup"><span data-stu-id="2153b-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="2153b-106">Например поставщика услуг, процесс отправки и получения MAPI или в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="2153b-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="2153b-107">Имеется объект состояния, предоставление сведений о каждой отдельной службы поставщика текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="2153b-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="2153b-108">MAPI несет ответственность за внедрение объектов состояния для подсистемы, процесс отправки и получения MAPI и адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2153b-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="2153b-109">Объект состояния подсистемы предоставляет глобальные данные.</span><span class="sxs-lookup"><span data-stu-id="2153b-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="2153b-110">Объект состояния для встроенной адресной книги предоставляет состояние всех поставщиками адресной книги в настоящее время работы.</span><span class="sxs-lookup"><span data-stu-id="2153b-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="2153b-111">Каждый объект состояния включен в таблице состояния, таблицы, задаваемые с помощью интерфейса MAPI, который предоставляет клиентам все сведения о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="2153b-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="2153b-112">Для получения дополнительных сведений см [Состояние](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2153b-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="2153b-113">Клиенты могут доступ к объекту определенное состояние, либо из таблицы или для поставщика услуг, через возвращается объект входа в систему.</span><span class="sxs-lookup"><span data-stu-id="2153b-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="2153b-114">Например для доступа к объекту состояние поставщика адресных книг, клиент может вызвать **IABLogon::OpenStatusEntry**.</span><span class="sxs-lookup"><span data-stu-id="2153b-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="2153b-115">Для получения дополнительных сведений см [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="2153b-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="2153b-116">Клиенты могут использовать состояние объектов:</span><span class="sxs-lookup"><span data-stu-id="2153b-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="2153b-117">Сведения о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="2153b-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="2153b-118">Мониторинг поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2153b-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="2153b-119">Контроль передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="2153b-119">Control message transmission.</span></span>
    
- <span data-ttu-id="2153b-120">Просмотр или изменение конфигурации и состоянии ресурса.</span><span class="sxs-lookup"><span data-stu-id="2153b-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="2153b-121">Каждый объект состояния реализует интерфейс **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="2153b-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="2153b-122">Дополнительные сведения можно [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="2153b-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="2153b-123">Тем не менее не каждый объект состояния полностью поддерживает все методы **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="2153b-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="2153b-124">Поскольку вариантов в методах, поддерживаемых приложением объект состояния, клиентам требуется сведения об объекте определенное состояние перед их можно использовать.</span><span class="sxs-lookup"><span data-stu-id="2153b-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="2153b-125">Состояние объектов необходимо опубликовать сведения о компонентах для их в следующие три свойства:</span><span class="sxs-lookup"><span data-stu-id="2153b-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="2153b-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2153b-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="2153b-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2153b-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="2153b-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2153b-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="2153b-129">Дополнительные сведения о реализации объекта состояния [Реализация объекта состояния](status-object-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="2153b-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="2153b-130">Дополнительные сведения об использовании состояние объекта можно [таблице состояния и состояния объектов](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2153b-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

