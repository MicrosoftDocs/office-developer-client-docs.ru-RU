---
title: Запуск поставщика службы
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Дата последнего изменения: 7 декабря 2015 года'
ms.openlocfilehash: d14a9961002d63733423af474e147ec5001051fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586335"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="668b9-103">Запуск поставщика службы</span><span class="sxs-lookup"><span data-stu-id="668b9-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="668b9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="668b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="668b9-105">К определенному моменту после клиент запускает сеанс с MAPI, ваш поставщик услуг будет запущен.</span><span class="sxs-lookup"><span data-stu-id="668b9-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="668b9-106">Поставщики транспорта, запущены клиент создает запрос для своих служб.</span><span class="sxs-lookup"><span data-stu-id="668b9-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="668b9-107">При входе в систему клиента, запущены поставщиков хранилища адресной книги и сообщения.</span><span class="sxs-lookup"><span data-stu-id="668b9-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="668b9-108">Клиент вызывает [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) для загрузки каждого из поставщиками адресных книг, включенные в профиль и [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) для загрузки поставщика хранилища определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="668b9-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="668b9-109">Поставщиками адресных книг, которые входят в состав службы сообщений, запущены перед любым из других поставщиков в службе.</span><span class="sxs-lookup"><span data-stu-id="668b9-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="668b9-110">MAPI запускает каждого поставщика услуг в текущей конфигурации следующим образом:</span><span class="sxs-lookup"><span data-stu-id="668b9-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="668b9-111">Поиск имя DLL в профиле.</span><span class="sxs-lookup"><span data-stu-id="668b9-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="668b9-112">Вы должны зарегистрировать имя вашего поставщика библиотеки DLL в файле конфигурации Mapisvc.inf, чтобы убедиться, что он отображается в профиле.</span><span class="sxs-lookup"><span data-stu-id="668b9-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="668b9-113">Когда ваш поставщик услуг добавляется в профиль по отдельности или в составе службы сообщений, все разделы **[Поставщика услуг]** из Mapisvc.inf, которые применяются к поставщику, копируются в профиль.</span><span class="sxs-lookup"><span data-stu-id="668b9-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="668b9-114">Дополнительные сведения о структуре Mapisvc.inf можно [Файл формата MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="668b9-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="668b9-115">Вызов функции Windows API **LoadLibrary** для загрузки библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="668b9-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="668b9-116">Так как MAPI вызывает **LoadLibrary** либо каждый раз, когда используется поставщик службы DLL (независимо от того, является ли он уже загружена) или только в первый раз, ваш поставщик услуг не может делать предположения об количество раз, которые будут загружаться.</span><span class="sxs-lookup"><span data-stu-id="668b9-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="668b9-117">Для каждого вызова **метода LoadLibrary**MAPI выполняется вызов функции Windows API **FreeLibrary** при поставщика услуг, которые больше не требуется DLL-Библиотеку.</span><span class="sxs-lookup"><span data-stu-id="668b9-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="668b9-118">Вызов функции точки входа для поставщика.</span><span class="sxs-lookup"><span data-stu-id="668b9-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="668b9-119">MAPI вызывает функцию точки входа вашего поставщика, чтобы начать процесс входа в систему.</span><span class="sxs-lookup"><span data-stu-id="668b9-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="668b9-120">Точка входа функции убедитесь, что используется версия интерфейса поставщика службы (SPI), совместимый с версией MAPI.</span><span class="sxs-lookup"><span data-stu-id="668b9-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="668b9-121">Также эти функции возвращают указатели на объекты только что созданный поставщика.</span><span class="sxs-lookup"><span data-stu-id="668b9-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="668b9-122">Дополнительные сведения о создании запись точки функции для поставщика см [реализации функции выберите запись службы поставщика](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="668b9-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="668b9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="668b9-123">See also</span></span>



[<span data-ttu-id="668b9-124">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="668b9-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

