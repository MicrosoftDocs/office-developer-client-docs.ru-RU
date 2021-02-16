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
# <a name="mapi-status-objects"></a><span data-ttu-id="1189c-103">Объекты состояния MAPI</span><span class="sxs-lookup"><span data-stu-id="1189c-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="1189c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1189c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1189c-105">Объекты состояния сообщают сведения о ресурсах MAPI.</span><span class="sxs-lookup"><span data-stu-id="1189c-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="1189c-106">Например, поставщик услуг, процесс отправки и получения MAPI или адресная книга.</span><span class="sxs-lookup"><span data-stu-id="1189c-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="1189c-107">Существует объект состояния, который сообщает сведения о каждом отдельном поставщике услуг в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="1189c-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="1189c-108">MAPI отвечает за реализацию объектов состояния для подсистемы, процесса отправки и получения MAPI и адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1189c-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="1189c-109">Объект состояния подсистемы обеспечивает глобальную информацию.</span><span class="sxs-lookup"><span data-stu-id="1189c-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="1189c-110">Объект состояния для интегрированной адресной книги сообщает состояние всех поставщиков адресных книг, работающих в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="1189c-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="1189c-111">Каждый объект состояния включается в таблицу состояния , таблицу, поддерживаемую MAPI, которая предоставляет клиентам все сведения о состоянии для сеанса.</span><span class="sxs-lookup"><span data-stu-id="1189c-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="1189c-112">Дополнительные сведения см. в [таблицах состояния.](status-tables.md)</span><span class="sxs-lookup"><span data-stu-id="1189c-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="1189c-113">Клиенты могут получить доступ к определенному объекту состояния либо с помощью таблицы, либо для поставщика услуг с помощью объекта для входов.</span><span class="sxs-lookup"><span data-stu-id="1189c-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="1189c-114">Например, чтобы получить доступ к объекту состояния поставщика адресной книги, клиент может вызвать **IABLogon::OpenStatusEntry.**</span><span class="sxs-lookup"><span data-stu-id="1189c-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="1189c-115">Дополнительные сведения см. в [IABLogon::OpenStatusEntry.](iablogon-openstatusentry.md)</span><span class="sxs-lookup"><span data-stu-id="1189c-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="1189c-116">Клиенты могут использовать объекты состояния для:</span><span class="sxs-lookup"><span data-stu-id="1189c-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="1189c-117">Узнайте о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="1189c-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="1189c-118">Мониторинг поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="1189c-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="1189c-119">Управление передачей сообщений.</span><span class="sxs-lookup"><span data-stu-id="1189c-119">Control message transmission.</span></span>
    
- <span data-ttu-id="1189c-120">Просмотр или изменение конфигурации и состояния ресурса.</span><span class="sxs-lookup"><span data-stu-id="1189c-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="1189c-121">Каждый объект состояния реализует **интерфейс IMAPIStatus.**</span><span class="sxs-lookup"><span data-stu-id="1189c-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="1189c-122">Дополнительные сведения см. в подразделе [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="1189c-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="1189c-123">Однако не каждый объект состояния полностью поддерживает каждый **метод IMAPIStatus.**</span><span class="sxs-lookup"><span data-stu-id="1189c-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="1189c-124">Так как методы, поддерживаемые объектом состояния, имеются в разных вариантах, клиентам необходимо изучить определенный объект состояния, прежде чем использовать его.</span><span class="sxs-lookup"><span data-stu-id="1189c-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="1189c-125">Объекты состояния необходимы для публикации сведений об их функции в следующих трех свойствах:</span><span class="sxs-lookup"><span data-stu-id="1189c-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="1189c-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1189c-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="1189c-127">**PR_RESOURCE_TYPE** ([PidTagResourceType)](pidtagresourcetype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1189c-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="1189c-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1189c-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="1189c-129">Дополнительные сведения о реализации объекта состояния см. в [сведениях о реализации объекта status.](status-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="1189c-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="1189c-130">Дополнительные сведения об использовании объекта состояния см. в [таблицах status Table и Status Objects.](status-table-and-status-objects.md)</span><span class="sxs-lookup"><span data-stu-id="1189c-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

