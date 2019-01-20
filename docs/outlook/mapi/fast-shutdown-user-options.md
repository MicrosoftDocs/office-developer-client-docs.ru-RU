---
title: Пользовательские параметры быстрого завершения работы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Дата последнего изменения: 26 июня 2012 года'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716371"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="b46f1-103">Пользовательские параметры быстрого завершения работы</span><span class="sxs-lookup"><span data-stu-id="b46f1-103">Fast shutdown user options</span></span>

<span data-ttu-id="b46f1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b46f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b46f1-105">В этой статье описаны три параметра реестра Windows, доступные начиная с Microsoft Outlook 2010, включая Microsoft Outlook 2013, для быстрого завершения работы клиентов MAPI пользователя.</span><span class="sxs-lookup"><span data-stu-id="b46f1-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="b46f1-106">Администраторы могут использовать эти параметры реестра, чтобы указать предпочитаемое поведение при завершении работы клиента в зависимости от поддержки поставщиками MAPI быстрого завершения работы клиента.</span><span class="sxs-lookup"><span data-stu-id="b46f1-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="b46f1-107">Параметр администратора, в свою очередь, определяет реакцию подсистемы MAPI на вызов клиентом MAPI метода [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) с учетом наличия поддержки быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="b46f1-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="b46f1-108">Хотя параметр реестра отражает предпочтения администратора на уровне пользователя по быстрому завершению работы для всех клиентов MAPI, разработчик клиента MAPI может решить, поддерживает ли клиент быстрое завершение работы независимо от других клиентов MAPI и параметра реестра администратора.</span><span class="sxs-lookup"><span data-stu-id="b46f1-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="b46f1-109">Тем не менее, для успешности быстрого завершения работы у пользователя должен быть настроен необходимый параметр реестра, клиент MAPI должен начать быстрое завершение работы с помощью интерфейса [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md), а поставщики MAPI, работающие с клиентом, должны реализовать интерфейс [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) для поддержки быстрого завершения работы клиента.</span><span class="sxs-lookup"><span data-stu-id="b46f1-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="b46f1-110">В приведенном ниже списке описаны три варианта на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="b46f1-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="b46f1-111">Вариант 1. Подсистема MAPI позволяет быстро завершить работу, если поставщики MAPI не отказались от этого явным образом</span><span class="sxs-lookup"><span data-stu-id="b46f1-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="b46f1-112">Начиная с Outlook 2010, это поведение по умолчанию, если Outlook является клиентом MAPI. Это необязательно является поведением по умолчанию в других клиентах MAPI.</span><span class="sxs-lookup"><span data-stu-id="b46f1-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="b46f1-113">Чтобы явным образом указать этот вариант для Outlook, администраторы могут настроить указанный ниже раздел реестра и значение.</span><span class="sxs-lookup"><span data-stu-id="b46f1-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="b46f1-114">Раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="b46f1-114"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="b46f1-115">Значение:</span><span class="sxs-lookup"><span data-stu-id="b46f1-115">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="b46f1-116">Когда клиент MAPI запускает быстрое завершение работы и вызывает метод **IMAPIClientShutdown::QueryFastShutdown** для запроса поддержки быстрого завершения работы, подсистема MAPI в ответ на запрос возвращает значение S\_OK, если никакой поставщик MAPI с активным сеансом MAPI у клиента MAPI явным образом не отказался от поддержки быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="b46f1-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="b46f1-117">Поставщик MAPI отказывается от быстрого завершения работы путем возвращения ошибки при реализации метода [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) (MAPI\_E\_NO\_SUPPORT).</span><span class="sxs-lookup"><span data-stu-id="b46f1-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="b46f1-118">Если один или несколько поставщиков MAPI возвращают ошибку в методе **IMAPIProviderShutdown::QueryFastShutdown**, подсистема MAPI возвращает значение MAPI_\E_\NO\_SUPPORT в метод **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="b46f1-119">Если поставщик MAPI не оказался от применения, подсистема MAPI возвращает значение S\_OK, даже если один или несколько поставщиков не реализовали интерфейс **IMAPIProviderShutdown : IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="b46f1-120">Вариант 2. Подсистема MAPI позволяет быстро завершить работу, если все поставщики MAPI согласились на это явным образом</span><span class="sxs-lookup"><span data-stu-id="b46f1-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="b46f1-121">Администраторы должны явным образом настроить указанный ниже раздел реестра и значение, чтобы указать предпочтение для быстрого завершения работы клиента.</span><span class="sxs-lookup"><span data-stu-id="b46f1-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="b46f1-122">Раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="b46f1-122"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="b46f1-123">Значение:</span><span class="sxs-lookup"><span data-stu-id="b46f1-123">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="b46f1-124">Когда клиент MAPI запускает быстрое завершение работы и вызывает метод **IMAPIClientShutdown::QueryFastShutdown** для запроса поддержки быстрого завершения работы, подсистема MAPI в ответ на запрос возвращает значение S\_OK, если все поставщики MAPI с активными сеансами с клиентами MAPI поддерживают быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="b46f1-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="b46f1-125">Поставщик MAPI демонстрирует свою поддержку путем возвращения кода отсутствия ошибки при реализации метода **IMAPIProviderShutdown::QueryFastShutdown** (S\_ОК).</span><span class="sxs-lookup"><span data-stu-id="b46f1-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="b46f1-126">Если один или несколько таких поставщиков MAPI возвращают значение MAPI\_E\_NO\_SUPPORT или не реализуют метод **IMAPIProviderShutdown::QueryFastShutdown**, подсистема MAPI возвращает код ошибки в метод **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="b46f1-127">Вариант 3. Администратор отключает поддержку быстрого завершения работы клиента</span><span class="sxs-lookup"><span data-stu-id="b46f1-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="b46f1-128">Администраторы должны явным образом настроить указанный ниже раздел реестра и значение, чтобы отключить поддержку быстрого завершения работы клиента.</span><span class="sxs-lookup"><span data-stu-id="b46f1-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="b46f1-129">Раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="b46f1-129"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="b46f1-130">Значение:</span><span class="sxs-lookup"><span data-stu-id="b46f1-130">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="b46f1-131">Когда клиент MAPI запускает быстрое завершение работы и вызывает метод **IMAPIClientShutdown::QueryFastShutdown** для запроса поддержки быстрого завершения работы, подсистема MAPI в ответ на запрос возвращает значение MAPI_E_NO_SUPPORT независимо от поддержки каким-либо поставщиком MAPI быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="b46f1-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="b46f1-132">При этом параметре реестра подсистема MAPI никогда не вызывает метод **IMAPIProviderShutdown::QueryFastShutdown** или [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) поставщиков.</span><span class="sxs-lookup"><span data-stu-id="b46f1-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b46f1-133">См. также</span><span class="sxs-lookup"><span data-stu-id="b46f1-133">See also</span></span>

- [<span data-ttu-id="b46f1-134">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="b46f1-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="b46f1-135">Обзор быстрого завершения работы</span><span class="sxs-lookup"><span data-stu-id="b46f1-135">Fast shutdown overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="b46f1-136">Рекомендации по быстрому завершению работы</span><span class="sxs-lookup"><span data-stu-id="b46f1-136">Best practices for fast shutdown</span></span>](best-practices-for-fast-shutdown.md)

