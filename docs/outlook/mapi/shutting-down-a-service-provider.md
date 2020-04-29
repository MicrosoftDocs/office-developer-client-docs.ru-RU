---
title: Завершение работы поставщика услуг
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
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="a2f26-103">Завершение работы поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="a2f26-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="a2f26-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2f26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2f26-105">Когда клиент вызывает метод [IMAPISession:: logoff](imapisession-logoff.md) для завершения сеанса и завершения работы всех активных поставщиков услуг, MAPI в свою очередь вызывает следующие методы:</span><span class="sxs-lookup"><span data-stu-id="a2f26-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="a2f26-106">[Иаблогон:: выход из системы](iablogon-logoff.md) для поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="a2f26-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="a2f26-107">[Имслогон:: выход из системы](imslogon-logoff.md) для поставщиков хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="a2f26-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="a2f26-108">[Иксплогон:: транспортлогофф](ixplogon-transportlogoff.md) для поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="a2f26-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="a2f26-109">Эти методы имеют похожие реализации.</span><span class="sxs-lookup"><span data-stu-id="a2f26-109">These methods have similar implementations.</span></span> <span data-ttu-id="a2f26-110">Ниже перечислены основные задачи, выполняемые методом выхода.</span><span class="sxs-lookup"><span data-stu-id="a2f26-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="a2f26-111">Освобождение всех открытых объектов, в том числе подобъектов и объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="a2f26-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="a2f26-112">Вызов метода [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объекта support для уменьшения счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="a2f26-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="a2f26-113">Удаление всех зарегистрированных структур [мапиуид](mapiuid.md) поставщика.</span><span class="sxs-lookup"><span data-stu-id="a2f26-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="a2f26-114">Удаление строки поставщика в таблице Status.</span><span class="sxs-lookup"><span data-stu-id="a2f26-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="a2f26-115">Выполнение любых задач, связанных с удалением ресурсов, таких как следующие:</span><span class="sxs-lookup"><span data-stu-id="a2f26-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="a2f26-116">Завершение подключения к удаленному серверу.</span><span class="sxs-lookup"><span data-stu-id="a2f26-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="a2f26-117">Уменьшение числа ссылок на объект logon.</span><span class="sxs-lookup"><span data-stu-id="a2f26-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="a2f26-118">Удаление объекта logon из списка объектов входа, которые хранятся у поставщика.</span><span class="sxs-lookup"><span data-stu-id="a2f26-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="a2f26-119">В режиме отладки выдача трассировок для обнаружения объектов с утечкой памяти.</span><span class="sxs-lookup"><span data-stu-id="a2f26-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="a2f26-120">При возвращении метода выхода из системы MAPI вызывает следующие вызовы:</span><span class="sxs-lookup"><span data-stu-id="a2f26-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="a2f26-121">Метод **IUnknown:: Release** объекта logon.</span><span class="sxs-lookup"><span data-stu-id="a2f26-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="a2f26-122">Метод **завершения работы** объекта Provider для выполнения окончательных задач очистки.</span><span class="sxs-lookup"><span data-stu-id="a2f26-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="a2f26-123">В зависимости от типа поставщика вызывается один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="a2f26-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="a2f26-124">[Иабпровидер:: завершение работы](iabprovider-shutdown.md) для поставщиков адресных книг</span><span class="sxs-lookup"><span data-stu-id="a2f26-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="a2f26-125">[Функцииimsprovider:: Shutdown](imsprovider-shutdown.md) для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="a2f26-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="a2f26-126">[Иксппровидер:: Shutdown](ixpprovider-shutdown.md) для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="a2f26-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="a2f26-127">Метод **IUnknown:: Release** объекта provider.</span><span class="sxs-lookup"><span data-stu-id="a2f26-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="a2f26-128">Если ваш поставщик является хранилищем сообщений, клиентский вызов [IMsgStore:: сторелогофф](imsgstore-storelogoff.md) также начнет процесс завершения работы.</span><span class="sxs-lookup"><span data-stu-id="a2f26-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="a2f26-129">**Сторелогофф** закрывает один конкретный поставщик хранилища сообщений и не оказывает никакого действия для сеанса.</span><span class="sxs-lookup"><span data-stu-id="a2f26-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="a2f26-130">С этим методом можно завершить работу только из поставщика хранилища сообщений; нет явного способа завершить работу определенной адресной книги или поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="a2f26-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="a2f26-131">Сведения о том, как реагировать на вызов **сторелогофф** , приведены в разделе [Завершение работы поставщика хранилища сообщений](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a2f26-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="a2f26-132">Библиотека DLL поставщика будет выгружена, когда MAPI вызывает функцию API Win32 **FreeLibrary**, вызов, выполненный после последнего активного клиента, называется [мапиунинитиализе](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="a2f26-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="a2f26-133">По истечение этого времени ваш поставщик услуг завершит работу.</span><span class="sxs-lookup"><span data-stu-id="a2f26-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2f26-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a2f26-134">See also</span></span>



[<span data-ttu-id="a2f26-135">Поставщики службы MAPI</span><span class="sxs-lookup"><span data-stu-id="a2f26-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

