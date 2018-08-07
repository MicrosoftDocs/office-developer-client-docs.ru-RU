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
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809081"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="03e81-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03e81-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="03e81-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03e81-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03e81-105">Разрешает подсистемы MAPI для оповещения Поставщик MAPI быстрое завершение работы клиент MAPI, чтобы поставщик MAPI могут отвечать на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="03e81-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03e81-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="03e81-106">Header file:</span></span>  <br/> |<span data-ttu-id="03e81-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03e81-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="03e81-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="03e81-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="03e81-109">Объекты поставщика: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)или [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="03e81-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="03e81-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="03e81-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="03e81-111">Поставщик MAPI</span><span class="sxs-lookup"><span data-stu-id="03e81-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="03e81-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="03e81-112">Called by:</span></span>  <br/> |<span data-ttu-id="03e81-113">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="03e81-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="03e81-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="03e81-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="03e81-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="03e81-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="03e81-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="03e81-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="03e81-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="03e81-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="03e81-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="03e81-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="03e81-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="03e81-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="03e81-120">Запросы, которые поддерживают поставщика MAPI для быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="03e81-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="03e81-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="03e81-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="03e81-122">Указывает поставщика MAPI, что клиент MAPI требуется выполнить быстрое завершение работы, чтобы поставщик можно выполнять действия, чтобы предотвратить потерю данных.</span><span class="sxs-lookup"><span data-stu-id="03e81-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="03e81-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="03e81-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="03e81-124">Указывает поставщика MAPI немедленно, выходе клиент MAPI, чтобы поставщик MAPI будут сохранены и отобразятся изменения, чтобы предотвратить потерю данных.</span><span class="sxs-lookup"><span data-stu-id="03e81-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03e81-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="03e81-125">Remarks</span></span>

<span data-ttu-id="03e81-126">Быстрое завершение работы позволяет клиент MAPI выйти из своего процесса в течение короткого времени, как кажется после клиента и загруженных поставщики MAPI сохранения параметров MAPI и данных.</span><span class="sxs-lookup"><span data-stu-id="03e81-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="03e81-127">Клиент MAPI всегда инициирует быстрое завершение работы и необходимо запросить подсистемы MAPI для поддержки быстрое завершение работы из загруженных поставщики MAPI.</span><span class="sxs-lookup"><span data-stu-id="03e81-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="03e81-128">Администратор может установить реестра Windows на уровне пользователя, чтобы указать уровень поддержки поставщика, который необходимо разрешить быстрое завершение работы всех клиентов MAPI.</span><span class="sxs-lookup"><span data-stu-id="03e81-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="03e81-129">Дополнительные сведения о параметрах реестра видеть [Fast параметры завершения работы пользователя](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="03e81-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="03e81-130">Тем не менее быстрое завершение работы будет успешно выполнена без потери данных поставщики MAPI следует реализовать интерфейс **IMAPIProviderShutdown** .</span><span class="sxs-lookup"><span data-stu-id="03e81-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="03e81-131">Поставщик MAPI, должна поддерживать быстрое завершение работы клиента должен возвращать значение S_OK в подсистему MAPI в методе **IMAPIProviderShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="03e81-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="03e81-132">При последующем подсистемы MAPI вызывает методы **IMAPIProviderShutdown::NotifyProcessShutdown** и **IMAPIProviderShutdown::DoFastShutdown** , поставщика MAPI должен выполнять действия, необходимые для сохранения параметров MAPI и данных и Подготовка к выхода клиента.</span><span class="sxs-lookup"><span data-stu-id="03e81-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="03e81-133">Поставщики MAPI, которые не должны поддерживать быстрое завершение работы клиента следует по-прежнему реализовать интерфейс **IMAPIProviderShutdown** и метод **IMAPIProviderShutdown::QueryFastShutdown** возвращает MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="03e81-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="03e81-134">Для Outlook как клиент MAPI в результате Outlook вынуждены ждать освобождения всех внешних ссылок освободить до его завершения.</span><span class="sxs-lookup"><span data-stu-id="03e81-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="03e81-135">В зависимости от реестра Windows пользователя политика для быстрое завершение работы не реализация интерфейса **IMAPIProviderShutdown** не обязательно быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="03e81-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="03e81-136">Дополнительные сведения о процессе быстрое завершение работы см [быстрое завершение работы](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="03e81-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="03e81-137">Сведения о том, как успешно выполнить быстрое завершение работы, [рекомендации](best-practices-for-fast-shutdown.md)по быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="03e81-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03e81-138">См. также</span><span class="sxs-lookup"><span data-stu-id="03e81-138">See also</span></span>



[<span data-ttu-id="03e81-139">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="03e81-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="03e81-140">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="03e81-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

