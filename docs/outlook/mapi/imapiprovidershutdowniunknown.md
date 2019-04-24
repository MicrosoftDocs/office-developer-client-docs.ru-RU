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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322409"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="78862-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78862-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="78862-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78862-105">Позволяет подсистеме MAPI сообщать поставщику MAPI быстрое завершение работы клиента MAPI, чтобы поставщик MAPI мог ответить на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="78862-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78862-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="78862-106">Header file:</span></span>  <br/> |<span data-ttu-id="78862-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="78862-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="78862-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="78862-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="78862-109">Объекты поставщика: [иксппровидер](ixpprovideriunknown.md), [иабпровидер](iabprovideriunknown.md)или [функцииimsprovider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="78862-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="78862-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="78862-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="78862-111">Поставщик MAPI</span><span class="sxs-lookup"><span data-stu-id="78862-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="78862-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="78862-112">Called by:</span></span>  <br/> |<span data-ttu-id="78862-113">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="78862-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="78862-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="78862-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="78862-115">Иид_имапипровидершутдовн</span><span class="sxs-lookup"><span data-stu-id="78862-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="78862-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="78862-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="78862-117">ЛПМАПИПРОВИДЕРШУТДОВН</span><span class="sxs-lookup"><span data-stu-id="78862-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="78862-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="78862-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="78862-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="78862-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="78862-120">ЗаПрашивает у поставщика MAPI поддержку быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="78862-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="78862-121">Нотифипроцессшутдовн</span><span class="sxs-lookup"><span data-stu-id="78862-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="78862-122">Указывает поставщику MAPI, что клиент MAPI планирует выполнить быстрое завершение работы, чтобы поставщик мог выполнять действия для предотвращения потери данных.</span><span class="sxs-lookup"><span data-stu-id="78862-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="78862-123">Дофастшутдовн</span><span class="sxs-lookup"><span data-stu-id="78862-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="78862-124">Указывает поставщику MAPI, что клиент MAPI немедленно завершает работу, поэтому поставщик MAPI сохранит изменения, чтобы предотвратить потерю данных.</span><span class="sxs-lookup"><span data-stu-id="78862-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78862-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="78862-125">Remarks</span></span>

<span data-ttu-id="78862-126">Быстрое завершение работы позволяет клиенту MAPI выйти из процесса в течение короткого периода времени, надеюсь, после сохранения параметров и данных MAPI у клиента и загруженных поставщиков MAPI.</span><span class="sxs-lookup"><span data-stu-id="78862-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="78862-127">Клиент MAPI всегда инициирует быстрое завершение работы и запрашивает подсистему MAPI для поддержки быстрого завершения работы от загруженных поставщиков MAPI.</span><span class="sxs-lookup"><span data-stu-id="78862-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="78862-128">Администратор может настроить реестр Windows на уровне пользователя, чтобы указать уровень поддержки поставщика, который необходим для быстрого завершения работы всех клиентов MAPI.</span><span class="sxs-lookup"><span data-stu-id="78862-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="78862-129">Дополнительные сведения о параметрах реестра приведены в разделе [Параметры быстрого завершения работы пользователя](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="78862-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="78862-130">Однако для успешного завершения работы без потери данных поставщики MAPI должны реализовать интерфейс **IMAPIProviderShutdown** .</span><span class="sxs-lookup"><span data-stu-id="78862-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="78862-131">Поставщик MAPI, который должен поддерживать быстрое завершение работы клиента, должен вернуть значение S_OK в подсистему MAPI в методе **IMAPIProviderShutdown:: QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="78862-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="78862-132">Когда подсистема MAPI затем вызывает метод **IMAPIProviderShutdown:: нотифипроцессшутдовн** и **IMAPIProviderShutdown::D ОФАСТШУТДОВН** , поставщик MAPI должен выполнить необходимые действия для сохранения параметров и данных MAPI, а также Подготовьтесь к выходу клиента.</span><span class="sxs-lookup"><span data-stu-id="78862-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="78862-133">Поставщики MAPI, которые не нуждаются в поддержке быстрого завершения работы клиента, по-прежнему должны реализовывать интерфейс **IMAPIProviderShutdown** и иметь метод **IMAPIProviderShutdown:: QueryFastShutdown** , возвращающий мапи_е_но_суппорт.</span><span class="sxs-lookup"><span data-stu-id="78862-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="78862-134">Для Outlook в качестве клиента MAPI это приводит к тому, что Outlook ждет, пока все внешние ссылки будут сняты до завершения работы.</span><span class="sxs-lookup"><span data-stu-id="78862-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="78862-135">В зависимости от параметра реестра Windows для быстрого завершения работы, отсутствие реализации интерфейса **IMAPIProviderShutdown** не обязательно препятствует быстрому завершению работы клиента.</span><span class="sxs-lookup"><span data-stu-id="78862-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="78862-136">Дополнительные сведения о процессе быстрого завершения работы приведены в разделе [Обзор быстрого завершения работы](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="78862-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="78862-137">Сведения о том, как успешно выполнить быстрое завершение работы, приведены в разделе рекомендации [по быстроМу завершенИю работы](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="78862-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78862-138">См. также</span><span class="sxs-lookup"><span data-stu-id="78862-138">See also</span></span>



[<span data-ttu-id="78862-139">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="78862-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="78862-140">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="78862-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

