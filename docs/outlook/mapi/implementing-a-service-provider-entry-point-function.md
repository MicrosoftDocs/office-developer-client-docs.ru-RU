---
title: Реализация функции точки входа поставщика услуг
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332993"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="d950d-103">Реализация функции точки входа поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="d950d-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="d950d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d950d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d950d-105">Каждый поставщик услуг DLL имеет функцию точки входа, которую MAPI вызывает для ее загрузки.</span><span class="sxs-lookup"><span data-stu-id="d950d-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="d950d-106">Следует помнить, что эта функция точки входа не такая, как [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), функция точки входа в Win32 DLL.</span><span class="sxs-lookup"><span data-stu-id="d950d-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="d950d-107">В зависимости от типа поставщика функция точки входа поставщика соответствует другому прототипу.</span><span class="sxs-lookup"><span data-stu-id="d950d-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="d950d-108">MAPI определяет различные прототипы функций точки входа для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="d950d-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="d950d-109">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="d950d-109">**Provider**</span></span>|<span data-ttu-id="d950d-110">**Прототип функции точки входа**</span><span class="sxs-lookup"><span data-stu-id="d950d-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d950d-111">Поставщики магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="d950d-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="d950d-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="d950d-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="d950d-113">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="d950d-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="d950d-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="d950d-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="d950d-115">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="d950d-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="d950d-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="d950d-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="d950d-117">Большая часть функций в этих прототипах одинаково для всех типов поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="d950d-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="d950d-118">Адресная книга, хранилище сообщений и поставщики транспорта выполняют следующие две основные задачи в своих функциях точки входа:</span><span class="sxs-lookup"><span data-stu-id="d950d-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="d950d-119">Проверьте версию интерфейса поставщика услуг (SPI), чтобы убедиться, что MAPI использует версию, совместимую с версией, которую использует поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="d950d-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="d950d-120">Для выполнения проверки используйте параметр  _lpulMAPIVer,_ содержащий версию MAPI SPI, и  _параметр lpulProviderVer,_ содержащий версию SPI.</span><span class="sxs-lookup"><span data-stu-id="d950d-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="d950d-121">Эти параметры — это 32-битные неподписаные integers, состоящие из трех частей:</span><span class="sxs-lookup"><span data-stu-id="d950d-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="d950d-122">Биты от 24 до 31 представляют главную версию.</span><span class="sxs-lookup"><span data-stu-id="d950d-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="d950d-123">Биты от 16 до 23 представляют незначительную версию.</span><span class="sxs-lookup"><span data-stu-id="d950d-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="d950d-124">Биты от 0 до 15 представляют идентификатор обновления.</span><span class="sxs-lookup"><span data-stu-id="d950d-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="d950d-125">Несмотря на то, что основной номер версии редко изменяется, незначительный номер версии изменяется при выпусках MAPI и изменения SPI.</span><span class="sxs-lookup"><span data-stu-id="d950d-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="d950d-126">Идентификатор обновления — это внутренняя версия сборки Майкрософт; он используется для отслеживания изменений в процессе разработки.</span><span class="sxs-lookup"><span data-stu-id="d950d-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="d950d-127">MAPI определяет постоянную CURRENT_SPI_VERSION, задокументированную в файле заголовки Mapispi.h, чтобы указать конечную версию SPI.</span><span class="sxs-lookup"><span data-stu-id="d950d-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="d950d-128">Сбой проверки с ошибкой MAPI_E_VERSION, если вы используете версию SPI, которая является более новой, чем версия, которую использует MAPI.</span><span class="sxs-lookup"><span data-stu-id="d950d-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="d950d-129">Создание экземпляра объекта-поставщика.</span><span class="sxs-lookup"><span data-stu-id="d950d-129">Create an instance of a provider object.</span></span> <span data-ttu-id="d950d-130">Так как поставщик может быть запущен и инициализирован несколько раз, необходимо создавать новый экземпляр каждый раз, когда это происходит.</span><span class="sxs-lookup"><span data-stu-id="d950d-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="d950d-131">Поставщики запущены несколько раз, когда они отображаются в нескольких профилях, которые используются одновременно одним или несколькими клиентами, или когда они отображаются несколько раз в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="d950d-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="d950d-132">Точно так же, как прототип функции точки входа отличается в зависимости от типа поставщика, так и тип объекта-поставщика.</span><span class="sxs-lookup"><span data-stu-id="d950d-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="d950d-133">Если вы пишете поставщика адресных книг, реализуем [IABProvider : IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d950d-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="d950d-134">Если вы пишете поставщика магазина сообщений, реализуют [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d950d-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="d950d-135">Дополнительные сведения см. в [перенагрузке поставщиков магазинов сообщений.](loading-message-store-providers.md)</span><span class="sxs-lookup"><span data-stu-id="d950d-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="d950d-136">Если вы пишете поставщика транспорта, реализуют [IXPProvider : IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d950d-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="d950d-137">Дополнительные сведения см. в [инициализации поставщика транспорта.](initializing-the-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="d950d-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d950d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="d950d-138">See also</span></span>



[<span data-ttu-id="d950d-139">Запуск поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="d950d-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

