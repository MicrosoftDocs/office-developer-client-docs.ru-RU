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
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="a2373-103">Реализация функции точки входа поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="a2373-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="a2373-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2373-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2373-105">Каждая DLL-запись поставщика услуг имеет функцию точки входа, которую MAPI вызывает для ее загрузки.</span><span class="sxs-lookup"><span data-stu-id="a2373-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="a2373-106">Следует помнить, что эта функция точки входа не такая, как [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), функция точки входа Win32 DLL.</span><span class="sxs-lookup"><span data-stu-id="a2373-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="a2373-107">В зависимости от типа поставщика функция точки входа поставщика соответствует другому прототипу.</span><span class="sxs-lookup"><span data-stu-id="a2373-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="a2373-108">MAPI определяет различные прототипы функции точки входа для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="a2373-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="a2373-109">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="a2373-109">**Provider**</span></span>|<span data-ttu-id="a2373-110">**Прототип функции точки входа**</span><span class="sxs-lookup"><span data-stu-id="a2373-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2373-111">Поставщики store сообщений</span><span class="sxs-lookup"><span data-stu-id="a2373-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="a2373-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="a2373-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="a2373-113">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="a2373-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="a2373-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="a2373-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="a2373-115">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="a2373-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="a2373-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="a2373-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="a2373-117">Большая часть функциональных возможностей этих прототипов является одинаковой для всех типов поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="a2373-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="a2373-118">Адресная книга, хранилище сообщений и поставщики транспорта выполняют следующие две основные задачи в своих функциях точки входа:</span><span class="sxs-lookup"><span data-stu-id="a2373-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="a2373-119">Проверьте версию интерфейса поставщика услуг (SPI), чтобы убедиться, что MAPI использует версию, совместимую с версией, используемой поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="a2373-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="a2373-120">Для выполнения проверки используйте параметр  _lpulMAPIVer,_ который содержит версию MAPI SPI, и  _параметр lpulProviderVer,_ содержащий версию SPI.</span><span class="sxs-lookup"><span data-stu-id="a2373-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="a2373-121">Эти параметры являются 32-битами без подписи, состоящими из трех частей:</span><span class="sxs-lookup"><span data-stu-id="a2373-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="a2373-122">Биты от 24 до 31 представляют основной версии.</span><span class="sxs-lookup"><span data-stu-id="a2373-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="a2373-123">Биты от 16 до 23 представляют второстепенную версию.</span><span class="sxs-lookup"><span data-stu-id="a2373-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="a2373-124">Биты от 0 до 15 представляют идентификатор обновления.</span><span class="sxs-lookup"><span data-stu-id="a2373-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="a2373-125">Несмотря на то что основной номер версии редко изменяется, номер второстепенной версии изменяется при выпусках MAPI и изменения SPI.</span><span class="sxs-lookup"><span data-stu-id="a2373-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="a2373-126">Идентификатор обновления — это версия внутренней сборки Майкрософт; он используется для отслеживания изменений в процессе разработки.</span><span class="sxs-lookup"><span data-stu-id="a2373-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="a2373-127">MAPI определяет константы CURRENT_SPI_VERSION, задокументированные в файле заголовщика Mapispi.h, чтобы указать конечную версию SPI.</span><span class="sxs-lookup"><span data-stu-id="a2373-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="a2373-128">Не удается проверить ошибку MAPI_E_VERSION если вы используете версию SPI, которая является более новой, чем версия, используемая MAPI.</span><span class="sxs-lookup"><span data-stu-id="a2373-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="a2373-129">Создание экземпляра объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="a2373-129">Create an instance of a provider object.</span></span> <span data-ttu-id="a2373-130">Так как поставщик может быть запущен и инициализирован несколько раз, каждый раз при этом следует создавать новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a2373-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="a2373-131">Поставщики запущены несколько раз, когда они отображаются в нескольких профилях, которые одновременно используются одним или несколькими клиентами, или если они отображаются несколько раз в одном профиле.</span><span class="sxs-lookup"><span data-stu-id="a2373-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="a2373-132">Так же, как прототип функции точки входа отличается в зависимости от типа поставщика, так же как и тип объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="a2373-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="a2373-133">Если вы пишете поставщика адресной книги, реализуем [IABProvider : IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a2373-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="a2373-134">Если вы пишете поставщика store сообщений, реализуют [IMSProvider : IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a2373-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="a2373-135">Дополнительные сведения см. в [подзагосе "Загрузка поставщиков store сообщений".](loading-message-store-providers.md)</span><span class="sxs-lookup"><span data-stu-id="a2373-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="a2373-136">Если вы пишете поставщика транспорта, реализуют [IXPProvider : IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a2373-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="a2373-137">Дополнительные сведения см. в [инициализации поставщика транспорта.](initializing-the-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="a2373-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2373-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a2373-138">See also</span></span>



[<span data-ttu-id="a2373-139">Запуск поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="a2373-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

