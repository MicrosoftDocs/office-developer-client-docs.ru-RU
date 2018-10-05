---
title: Завершение работы поставщика службы
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395177"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="53027-103">Завершение работы поставщика службы</span><span class="sxs-lookup"><span data-stu-id="53027-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="53027-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53027-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53027-105">Когда клиент вызывает метод [IMAPISession::Logoff](imapisession-logoff.md) , чтобы завершить сеанс и завершите работу всех поставщиков услуг активный, MAPI в свою очередь вызывает следующие методы:</span><span class="sxs-lookup"><span data-stu-id="53027-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="53027-106">[IABLogon::Logoff](iablogon-logoff.md) поставщиками адресной книги.</span><span class="sxs-lookup"><span data-stu-id="53027-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="53027-107">[IMSLogon::Logoff](imslogon-logoff.md) поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="53027-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="53027-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="53027-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="53027-109">Эти методы иметь аналогичные реализации.</span><span class="sxs-lookup"><span data-stu-id="53027-109">These methods have similar implementations.</span></span> <span data-ttu-id="53027-110">Основные задачи, которые выполняет выход из системы, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="53027-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="53027-111">Освобождение всех открытых объектов, включая вложенных объектов и объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="53027-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="53027-112">Вызов метода [функции IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объект поддержки для уменьшения счетчик ссылок на него.</span><span class="sxs-lookup"><span data-stu-id="53027-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="53027-113">Удаление всех зарегистрированных [MAPIUID](mapiuid.md) структуры ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="53027-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="53027-114">Удаление ваш поставщик строки в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="53027-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="53027-115">Выполнять все задачи, связанные с очистки ресурсов, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="53027-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="53027-116">Завершение подключения к удаленному серверу.</span><span class="sxs-lookup"><span data-stu-id="53027-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="53027-117">Уменьшение справочные материалы по счетчик на объект вход в систему.</span><span class="sxs-lookup"><span data-stu-id="53027-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="53027-118">Удаление из списка объектов входа в систему, ваш поставщик хранит объект вход в систему.</span><span class="sxs-lookup"><span data-stu-id="53027-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="53027-119">В режиме отладки выдачи трассировку для поиска объектов, которые утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="53027-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="53027-120">При возвращении метод выхода из системы, MAPI вызывает следующее:</span><span class="sxs-lookup"><span data-stu-id="53027-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="53027-121">Метод **функции IUnknown::Release** объекта входа в систему.</span><span class="sxs-lookup"><span data-stu-id="53027-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="53027-122">Метод **Shutdown** объект поставщика для выполнения задач, окончательную.</span><span class="sxs-lookup"><span data-stu-id="53027-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="53027-123">В зависимости от типа поставщика называется один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="53027-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="53027-124">[IABProvider::Shutdown](iabprovider-shutdown.md) для поставщиками адресных книг</span><span class="sxs-lookup"><span data-stu-id="53027-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="53027-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) для поставщиков хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="53027-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="53027-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) для поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="53027-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="53027-127">Метод **функции IUnknown::Release** объект поставщика.</span><span class="sxs-lookup"><span data-stu-id="53027-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="53027-128">Если ваш поставщик хранилища сообщений, вызов клиентом [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) также начнет процесс завершения работы.</span><span class="sxs-lookup"><span data-stu-id="53027-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="53027-129">**StoreLogoff** завершает работу одного поставщика хранилища конкретное сообщение и не оказывает влияния на сеанс.</span><span class="sxs-lookup"><span data-stu-id="53027-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="53027-130">Только поставщика хранилища сообщений можно завершить работу с помощью этого метода; нет возможности явные остановки конкретной адресной книги или транспорта поставщика.</span><span class="sxs-lookup"><span data-stu-id="53027-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="53027-131">Дополнительные сведения о реагировании **StoreLogoff** звонков, см [Завершает работу сообщение поставщика хранилища](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="53027-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="53027-132">Ваш поставщик DLL будет выгружен, когда MAPI вызывает функцию Win32 API **FreeLibrary**вызов, внесенных после последнего активного клиента называется [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="53027-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="53027-133">В данный момент ваш поставщик услуг будет завершена завершает работу.</span><span class="sxs-lookup"><span data-stu-id="53027-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53027-134">См. также</span><span class="sxs-lookup"><span data-stu-id="53027-134">See also</span></span>



[<span data-ttu-id="53027-135">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="53027-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

