---
title: Быстрое завершение работы пользовательских параметров
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Последнее изменение: 26 июня 2012 г.'
ms.openlocfilehash: bd541ed09bc661f3697408d3f475928b9ef0bcc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585194"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="9828e-103">Быстрое завершение работы пользовательских параметров</span><span class="sxs-lookup"><span data-stu-id="9828e-103">Fast shutdown user options</span></span>

<span data-ttu-id="9828e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9828e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9828e-105">В этом разделе описываются три параметров реестра Windows, которые доступны, начиная с Microsoft Outlook 2010 и теперь включая Microsoft Outlook 2013 для быстрое завершение работы клиентов MAPI пользователя.</span><span class="sxs-lookup"><span data-stu-id="9828e-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="9828e-106">Администраторы могут использовать эти параметры реестра для указания режима завершения работы предпочитаемого клиентского в зависимости от те поставщики MAPI поддержка быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="9828e-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="9828e-107">Установка администратора, в свою очередь, определяет реакцию подсистемы MAPI на клиента MAPI вызов [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) с точки зрения поддержки доступно быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="9828e-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="9828e-108">Несмотря на то, что параметр реестра отражает предпочтений администратора на уровне пользователя, для быстрого завершения работы для всех клиентов MAPI, разработчик клиента MAPI можно определить, поддерживает ли клиент быстрое завершение работы независимо от других клиентов MAPI и параметр реестра администратора.</span><span class="sxs-lookup"><span data-stu-id="9828e-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="9828e-109">Тем не менее, для быстрого завершения работы вступили в силу успешно, пользователь должен иметь значение реестра, необходимых, клиент MAPI должен инициировать быстрое завершение работы с помощью [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) интерфейса и поставщики MAPI, которые работают с Клиент должен реализовывать [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) интерфейс для поддержки быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="9828e-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="9828e-110">В следующем списке описываются три варианта уровня пользователя.</span><span class="sxs-lookup"><span data-stu-id="9828e-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="9828e-111">Вариант 1: Подсистемы MAPI позволяет быстрое завершение работы, если не поставщики MAPI явным образом отключить</span><span class="sxs-lookup"><span data-stu-id="9828e-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="9828e-112">Начиная с Outlook 2010, это поведение по умолчанию при Outlook — это клиент MAPI; она не обязательно поведение по умолчанию для других клиентов MAPI.</span><span class="sxs-lookup"><span data-stu-id="9828e-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="9828e-113">Чтобы явно задать этот параметр для Outlook, Администраторы имеют возможность задать следующий раздел реестра и значение.</span><span class="sxs-lookup"><span data-stu-id="9828e-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="9828e-114">Раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="9828e-114">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="9828e-115">Значение:</span><span class="sxs-lookup"><span data-stu-id="9828e-115">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="9828e-116">Если клиент MAPI инициирует быстрое завершение работы и вызывает **IMAPIClientShutdown::QueryFastShutdown** для запроса для поддержки быстрое завершение работы, подсистемы MAPI отвечает на запрос, возвращая S\_OK в течение без поставщика MAPI, имеющей active MAPI сеанс с помощью клиентского интерфейса MAPI выбрал явно не поддерживается быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="9828e-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="9828e-117">Отключает поставщика MAPI из него быстрое завершение работы с помощью метода [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) возвращает ошибку (MAPI\_E\_NO\_поддержки).</span><span class="sxs-lookup"><span data-stu-id="9828e-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="9828e-118">Если один или несколько поставщики MAPI возвращает ошибку в **IMAPIProviderShutdown::QueryFastShutdown**, подсистемы MAPI возвращает MAPI_\E_\NO\_поддержки **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="9828e-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="9828e-119">Если не отключает поставщика MAPI, возвращает подсистемы MAPI S\_OK, даже в том случае, если один или несколько поставщиков не реализованы **IMAPIProviderShutdown: IUnknown** интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9828e-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="9828e-120">Вариант 2: Подсистемы MAPI позволяет быстрое завершение работы, только в том случае, если в явно отключает все поставщики MAPI</span><span class="sxs-lookup"><span data-stu-id="9828e-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="9828e-121">Администраторам необходимо явно задать следующий раздел реестра и значение, чтобы указать этот параметр для быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="9828e-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="9828e-122">Раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="9828e-122">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="9828e-123">Значение:</span><span class="sxs-lookup"><span data-stu-id="9828e-123">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="9828e-124">Если клиент MAPI инициирует быстрое завершение работы и вызывает **IMAPIClientShutdown::QueryFastShutdown** для запроса для поддержки быстрое завершение работы, подсистемы MAPI отвечает на запрос, возвращая S\_OK, если все поставщики MAPI, у которых активных сеансов с MAPI поддержки быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="9828e-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="9828e-125">Поставщика MAPI демонстрируется поддержки, реализовав **IMAPIProviderShutdown::QueryFastShutdown** для возврата кода об отсутствии ошибок (S\_ОК).</span><span class="sxs-lookup"><span data-stu-id="9828e-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="9828e-126">Если один или несколько таких поставщики MAPI возврата MAPI\_E\_NO\_поддержки, или не внедрять **IMAPIProviderShutdown::QueryFastShutdown**подсистемы MAPI возвращает код ошибки для **IMAPIClientShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="9828e-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="9828e-127">Вариант 3: Администратор отключает поддержку быстрое завершение работы клиента</span><span class="sxs-lookup"><span data-stu-id="9828e-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="9828e-128">Администраторам необходимо явно задать следующий раздел реестра и значение для отключения поддержки быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="9828e-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="9828e-129">Раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="9828e-129">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="9828e-130">Значение:</span><span class="sxs-lookup"><span data-stu-id="9828e-130">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="9828e-131">Если клиент MAPI инициирует быстрое завершение работы и вызывает **IMAPIClientShutdown::QueryFastShutdown** для запроса для поддержки быстрое завершение работы, подсистемы MAPI отвечает на запрос, возвращая MAPI_E_NO_SUPPORT, независимо от того, требуется ли любого поставщика MAPI поддерживает быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="9828e-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="9828e-132">В разделе этот параметр реестра в подсистеме MAPI никогда не вызывает метод **IMAPIProviderShutdown::QueryFastShutdown** или [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) любого поставщика.</span><span class="sxs-lookup"><span data-stu-id="9828e-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9828e-133">См. также</span><span class="sxs-lookup"><span data-stu-id="9828e-133">See also</span></span>

- [<span data-ttu-id="9828e-134">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="9828e-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="9828e-135">Обзор быстрого завершения работы</span><span class="sxs-lookup"><span data-stu-id="9828e-135">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="9828e-136">Рекомендации по быстрому завершению работы</span><span class="sxs-lookup"><span data-stu-id="9828e-136">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

