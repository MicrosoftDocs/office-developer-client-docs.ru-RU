---
title: Отключение поставщика услуг
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339209"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="a0423-103">Отключение поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="a0423-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="a0423-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0423-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0423-105">Когда клиент вызывает [метод IMAPISession::Logoff,](imapisession-logoff.md) чтобы закончить сеанс и закрыть все активные поставщики услуг, MAPI в свою очередь вызывает следующие методы:</span><span class="sxs-lookup"><span data-stu-id="a0423-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="a0423-106">[IABLogon::Logoff](iablogon-logoff.md) для поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="a0423-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="a0423-107">[IMSLogon::Logoff](imslogon-logoff.md) для поставщиков магазинов сообщений.</span><span class="sxs-lookup"><span data-stu-id="a0423-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="a0423-108">[IXPLogon::TransportLogoff для](ixplogon-transportlogoff.md) поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="a0423-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="a0423-109">Эти методы имеют аналогичные реализации.</span><span class="sxs-lookup"><span data-stu-id="a0423-109">These methods have similar implementations.</span></span> <span data-ttu-id="a0423-110">Основные задачи, выполняемые методом журнала:</span><span class="sxs-lookup"><span data-stu-id="a0423-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="a0423-111">Освобождение всех открытых объектов, включая подобекты и объекты состояния.</span><span class="sxs-lookup"><span data-stu-id="a0423-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="a0423-112">Вызов метода [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объекта поддержки для усугубления его отсчета ссылок.</span><span class="sxs-lookup"><span data-stu-id="a0423-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="a0423-113">Удаление всех зарегистрированных структур [MAPIUID](mapiuid.md) поставщика.</span><span class="sxs-lookup"><span data-stu-id="a0423-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="a0423-114">Удаление строки поставщика в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="a0423-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="a0423-115">Выполнение любых задач, которые связаны с очисткой ресурсов, например следующие:</span><span class="sxs-lookup"><span data-stu-id="a0423-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="a0423-116">Прекращение подключения к удаленному серверу.</span><span class="sxs-lookup"><span data-stu-id="a0423-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="a0423-117">Decrementing the reference count on the logon object.</span><span class="sxs-lookup"><span data-stu-id="a0423-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="a0423-118">Удаление объекта logon из списка объектов logon, которые хранит поставщик.</span><span class="sxs-lookup"><span data-stu-id="a0423-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="a0423-119">В режиме отлаживания выдают следы, чтобы найти объекты с утечкой памяти.</span><span class="sxs-lookup"><span data-stu-id="a0423-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="a0423-120">Когда метод входа возвращается, MAPI вызывает следующее:</span><span class="sxs-lookup"><span data-stu-id="a0423-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="a0423-121">Метод **IUnknown::Release** объекта вашего логона.</span><span class="sxs-lookup"><span data-stu-id="a0423-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="a0423-122">Метод отключения объекта поставщика **для** выполнения любых задач окончательной очистки.</span><span class="sxs-lookup"><span data-stu-id="a0423-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="a0423-123">В зависимости от типа поставщика один из следующих методов называется:</span><span class="sxs-lookup"><span data-stu-id="a0423-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="a0423-124">[IABProvider::Shutdown](iabprovider-shutdown.md) для поставщиков адресных книг</span><span class="sxs-lookup"><span data-stu-id="a0423-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="a0423-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) для поставщиков магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="a0423-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="a0423-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="a0423-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="a0423-127">Метод **IUnknown::Release** объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="a0423-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="a0423-128">Если поставщик является хранилищем сообщений, клиентский вызов [в IMsgStore::StoreLogoff](imsgstore-storelogoff.md) также инициирует процесс остановки.</span><span class="sxs-lookup"><span data-stu-id="a0423-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="a0423-129">**StoreLogoff** закрывает одного конкретного поставщика магазина сообщений и не влияет на сеанс.</span><span class="sxs-lookup"><span data-stu-id="a0423-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="a0423-130">Только поставщик магазина сообщений может быть закрыт с помощью этого метода; нет явного способа отключения конкретной адресной книги или поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="a0423-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="a0423-131">Сведения о том, как реагировать на вызов **StoreLogoff,** см. в сообщении [Shutting Down a Message Store Provider.](shutting-down-a-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="a0423-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="a0423-132">DLL поставщика будет выгружена, когда MAPI вызывает функцию API **Win32 FreeLibrary**, вызов, который сделан после того, как последний активный клиент вызывает [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="a0423-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="a0423-133">К этому времени поставщик услуг завершит работу.</span><span class="sxs-lookup"><span data-stu-id="a0423-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0423-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a0423-134">See also</span></span>



[<span data-ttu-id="a0423-135">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="a0423-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

