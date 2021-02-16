---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409659"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="4a2ae-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a2ae-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="4a2ae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a2ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a2ae-105">Позволяет подсистеме MAPI сообщить поставщику MAPI о быстром закрытии клиента MAPI, чтобы поставщик MAPI ответил на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a2ae-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4a2ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a2ae-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a2ae-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4a2ae-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="4a2ae-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4a2ae-109">Объекты поставщика: [IXPProvider,](ixpprovideriunknown.md) [IABProvider](iabprovideriunknown.md)или [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="4a2ae-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="4a2ae-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4a2ae-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a2ae-111">Поставщик MAPI</span><span class="sxs-lookup"><span data-stu-id="4a2ae-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="4a2ae-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4a2ae-112">Called by:</span></span>  <br/> |<span data-ttu-id="4a2ae-113">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="4a2ae-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="4a2ae-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="4a2ae-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4a2ae-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="4a2ae-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="4a2ae-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="4a2ae-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4a2ae-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="4a2ae-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4a2ae-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="4a2ae-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4a2ae-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="4a2ae-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="4a2ae-120">Запрашивает у поставщика MAPI поддержку быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="4a2ae-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="4a2ae-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="4a2ae-122">Указывает поставщику MAPI, что клиент MAPI собирается быстро закрыть работу, чтобы поставщик может принять меры для предотвращения потери данных.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="4a2ae-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="4a2ae-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="4a2ae-124">Указывает поставщику MAPI, что клиент MAPI немедленно выходит, чтобы поставщик MAPI сохранял изменения, чтобы предотвратить потерю данных.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a2ae-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a2ae-125">Remarks</span></span>

<span data-ttu-id="4a2ae-126">Быстрое завершение работы позволяет клиенту MAPI выйти из процесса в течение короткого времени, надеемся, после того как клиент и загруженные поставщики MAPI сэкономят параметры и данные MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="4a2ae-127">Клиент MAPI всегда инициирует быстрое завершение работы и должен запрашивать поддержку быстрого завершения работы подсистемы MAPI от загруженных поставщиков MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="4a2ae-128">Администратор может задать реестр Windows на уровне пользователя, чтобы указать уровень поддержки поставщика, необходимый для быстрого завершения работы всех клиентов MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="4a2ae-129">Дополнительные сведения о параметрах реестра см. в параметрах пользователей быстрого [завершения работы.](fast-shutdown-user-options.md)</span><span class="sxs-lookup"><span data-stu-id="4a2ae-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="4a2ae-130">Однако для успешного завершения работы без потери данных поставщики MAPI должны реализовать интерфейс **IMAPIProviderShutdown.**</span><span class="sxs-lookup"><span data-stu-id="4a2ae-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="4a2ae-131">Поставщик MAPI, который должен поддерживать быстрое завершение работы клиента, должен возвращать S_OK подсистеме MAPI в **методе IMAPIProviderShutdown::QueryFastShutdown.**</span><span class="sxs-lookup"><span data-stu-id="4a2ae-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="4a2ae-132">Когда подсистема MAPI впоследствии вызывает методы **IMAPIProviderShutdown::NotifyProcessShutdown** и **IMAPIProviderShutdown::D oFastShutdown,** поставщик MAPI должен принять необходимые действия для сохранения параметров и данных MAPI и подготовки к выходу клиента.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="4a2ae-133">Поставщики MAPI, которые не нуждаются в поддержке быстрого завершения работы клиента, по-прежнему должны реализовать интерфейс **IMAPIProviderShutdown,** а метод **IMAPIProviderShutdown::QueryFastShutdown** должен возвращать MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="4a2ae-134">Для Outlook в качестве клиента MAPI это приводит к ожиданию выпуска всех внешних ссылок перед выходом из outlook.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="4a2ae-135">В зависимости от параметра реестра Windows пользователя для быстрого завершения работы не реализация интерфейса **IMAPIProviderShutdown** не обязательно препятствует быстрому отключению клиента.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="4a2ae-136">Дополнительные сведения о процессе быстрого завершения работы см. в обзоре [быстрого завершения работы.](fast-shutdown-overview.md)</span><span class="sxs-lookup"><span data-stu-id="4a2ae-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="4a2ae-137">Сведения о том, как успешно выполнить быстрое завершение работы, см. в лучших [методиках быстрого завершения работы.](best-practices-for-fast-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="4a2ae-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a2ae-138">См. также</span><span class="sxs-lookup"><span data-stu-id="4a2ae-138">See also</span></span>



[<span data-ttu-id="4a2ae-139">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="4a2ae-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="4a2ae-140">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="4a2ae-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

