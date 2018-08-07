---
title: Реализация функции точки входа для поставщика службы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 632aff9c0f6fc60ee9730b5e43667b5b610ae8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809297"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="aa048-103">Реализация функции точки входа для поставщика службы</span><span class="sxs-lookup"><span data-stu-id="aa048-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="aa048-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa048-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa048-105">Каждый поставщик услуг DLL-Библиотека имеет функцию, которая вызывает MAPI, чтобы загрузить его точки входа.</span><span class="sxs-lookup"><span data-stu-id="aa048-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="aa048-106">Обратите внимание, что эта функция точки входа не то же, что [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), функции точки входа Win32 DLL.</span><span class="sxs-lookup"><span data-stu-id="aa048-106">Be aware that this entry point function is not the same as [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="aa048-107">В зависимости от типа поставщика функция точки входа вашего поставщика соответствует другой прототип.</span><span class="sxs-lookup"><span data-stu-id="aa048-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="aa048-108">MAPI определяет прототипов функций различных запись точки для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="aa048-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="aa048-109">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="aa048-109">**Provider**</span></span>|<span data-ttu-id="aa048-110">**Прототип функции точки входа**</span><span class="sxs-lookup"><span data-stu-id="aa048-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa048-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="aa048-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="aa048-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="aa048-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="aa048-113">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="aa048-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="aa048-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="aa048-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="aa048-115">Поставщиками адресных книг</span><span class="sxs-lookup"><span data-stu-id="aa048-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="aa048-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="aa048-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="aa048-117">Значительная часть функциональности в этих прототипов является общим для всех типов поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="aa048-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="aa048-118">Адресная книга, хранилища сообщений и поставщиками транспорта выполните следующие две основные задачи в их функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="aa048-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="aa048-119">Проверка версии интерфейс поставщика службы (SPI) убедитесь, что MAPI используется версия, совместимый с версией, которая использует ваш поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="aa048-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="aa048-120">Используйте параметр _lpulMAPIVer_ , который содержит версию MAPI SPI и параметр _lpulProviderVer_ , который содержит вашей версии SPI, для выполнения проверки.</span><span class="sxs-lookup"><span data-stu-id="aa048-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="aa048-121">Эти параметры являются целые числа без знака 32-разрядная версия, состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="aa048-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="aa048-122">Биты 24 до 31 представляют основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="aa048-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="aa048-123">Биты 16 до 23 представляют дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="aa048-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="aa048-124">Биты цифры от 0 до 15 представляют идентификатор обновления.</span><span class="sxs-lookup"><span data-stu-id="aa048-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="aa048-125">Несмотря на то, что основной номер версии редко изменяется, изменения номер вспомогательной версии каждый раз, когда выпущен MAPI и индекс параметров безопасности был изменен.</span><span class="sxs-lookup"><span data-stu-id="aa048-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="aa048-126">Идентификатор обновления — это внутренний Microsoft построения версии; он используется для отслеживания изменений в процессе разработки.</span><span class="sxs-lookup"><span data-stu-id="aa048-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="aa048-127">MAPI определяет константу CURRENT_SPI_VERSION, приведенной в файле заголовка Mapispi.h для указания присутствует версии SPI.</span><span class="sxs-lookup"><span data-stu-id="aa048-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="aa048-128">Если используется версия старше версии, с помощью интерфейса MAPI индекс параметров безопасности с ошибкой вашей проверки с ошибкой MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="aa048-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="aa048-129">Создайте экземпляр объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="aa048-129">Create an instance of a provider object.</span></span> <span data-ttu-id="aa048-130">Так как поставщик может работы и инициализации несколько раз, необходимо создать новый экземпляр каждый раз, когда это происходит.</span><span class="sxs-lookup"><span data-stu-id="aa048-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="aa048-131">Поставщики запускаются несколько раз, когда они отображаются в несколько профилей, используемых одновременно с одного или нескольких клиентов или они отображаются несколько раз в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="aa048-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="aa048-132">Так же, как прототип функции запись точки отличается в зависимости от типа поставщика, поэтому не тип объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="aa048-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="aa048-133">При создании поставщика адресных книг реализовать [IABProvider: IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="aa048-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="aa048-134">При создании поставщика хранилища message реализация [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="aa048-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="aa048-135">Для получения дополнительных сведений см. [Загрузка поставщики хранилища сообщений](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="aa048-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="aa048-136">При создании поставщика транспорта реализовать [IXPProvider: IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="aa048-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="aa048-137">Для получения дополнительных сведений см [инициализации поставщика транспорта](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aa048-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa048-138">См. также</span><span class="sxs-lookup"><span data-stu-id="aa048-138">See also</span></span>



[<span data-ttu-id="aa048-139">Запуск поставщика службы</span><span class="sxs-lookup"><span data-stu-id="aa048-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

