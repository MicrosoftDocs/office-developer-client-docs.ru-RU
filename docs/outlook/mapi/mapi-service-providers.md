---
title: Поставщики услуг MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409540"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="aa1e7-103">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="aa1e7-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="aa1e7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa1e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa1e7-105">Существует три распространенных типа поставщиков услуг:</span><span class="sxs-lookup"><span data-stu-id="aa1e7-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="aa1e7-106">Поставщики адресных книг.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-106">Address book providers.</span></span>
    
- <span data-ttu-id="aa1e7-107">Поставщики store сообщений.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-107">Message store providers.</span></span>
    
- <span data-ttu-id="aa1e7-108">Поставщики транспорта.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-108">Transport providers.</span></span>
    
<span data-ttu-id="aa1e7-109">Поставщики адресной книги и магазина сообщений имеют множество сходств.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="aa1e7-110">Они регистрируют уникальный идентификатор с помощью MAPI, который они используют для создания идентификаторов записей для своих объектов.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="aa1e7-111">Они предоставляют иерархию объектов и свойств, к которые клиенты могут получать доступ и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="aa1e7-112">Для своих объектов-контейнеров они поддерживают таблицу иерархии и таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="aa1e7-113">Они поддерживают уведомления о событиях в этих таблицах и при желании на отдельных объектах, чтобы клиенты могли получать уведомления об изменениях, происходящих во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="aa1e7-114">Когда операции становятся длительными, они могут отображать индикатор хода выполнения, чтобы сообщить пользователю о состоянии операции.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="aa1e7-115">Клиенты могут взаимодействовать с поставщиками адресной книги и магазина сообщений либо косвенно через MAPI, используя [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) и [IMAPISession : интерфейсы IUnknown](imapisessioniunknown.md) или напрямую с помощью одного из интерфейсов поставщика услуг, который приводится в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="aa1e7-116">**Интерфейсы поставщиков адресных книг**</span><span class="sxs-lookup"><span data-stu-id="aa1e7-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="aa1e7-117">**Интерфейсы поставщиков store сообщений**</span><span class="sxs-lookup"><span data-stu-id="aa1e7-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa1e7-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="aa1e7-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="aa1e7-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aa1e7-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="aa1e7-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="aa1e7-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="aa1e7-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="aa1e7-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="aa1e7-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aa1e7-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="aa1e7-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aa1e7-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="aa1e7-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aa1e7-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="aa1e7-125">Поставщики транспорта отличаются от поставщиков адресной книги и хранения сообщений способом взаимодействия с MAPI и клиентами.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="aa1e7-126">Поставщики транспорта обычно ждут, пока MAPI запросит у них информацию, а не инициируют связь.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="aa1e7-127">В отличие от других поставщиков, поставщики транспорта не поддерживают различные объекты и таблицы, к которые часто имеют доступ клиенты.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="aa1e7-128">Однако они поддерживают объект состояния, как и все поставщики услуг, и публикуют его свойства в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="aa1e7-129">В то время как поставщики адресной книги и хранения сообщений вызывают метод [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации уникальных идентификаторов для создания идентификаторов записей, поставщики транспорта звонят [методу IXPLogon::AddressTypes](ixplogon-addresstypes.md) для регистрации уникальных идентификаторов, а также типов адресов для оказания ответственности за доставку определенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="aa1e7-130">Поставщик услуг должен иметь три файла заголовок: один файл общедоступных и два внутренних.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="aa1e7-131">Используйте файл открытого загона для настройки, а также для документации свойств и их значений.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="aa1e7-132">Включить в один из внутренних файлов заголовок все необходимые общедоступные заголовки MAPI; Этот файл заголовок должен быть включен во все исходные файлы поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="aa1e7-133">Используйте другой внутренний файл для определения идентификаторов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="aa1e7-134">Адресная книга, хранилище сообщений и поставщики транспорта выполняют следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="aa1e7-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="aa1e7-135">Указать функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="aa1e7-136">Предоставить поставщик и объект для логотипа для обработки инициализации и инициализации.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="aa1e7-137">Если поставщик принадлежит к службе сообщений, указать функцию точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="aa1e7-138">Поддержка конфигурации путем реализации таблицы свойств.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="aa1e7-139">Реализация объекта состояния и поддержка таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="aa1e7-140">Обработка отключения.</span><span class="sxs-lookup"><span data-stu-id="aa1e7-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa1e7-141">См. также</span><span class="sxs-lookup"><span data-stu-id="aa1e7-141">See also</span></span>



[<span data-ttu-id="aa1e7-142">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="aa1e7-142">MAPI Concepts</span></span>](mapi-concepts.md)

