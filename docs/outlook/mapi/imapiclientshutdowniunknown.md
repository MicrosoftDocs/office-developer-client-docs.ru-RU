---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435336"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="8c4ca-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c4ca-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="8c4ca-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c4ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c4ca-105">Позволяет клиенту MAPI выполнять быстрое завершение клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c4ca-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8c4ca-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c4ca-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c4ca-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8c4ca-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="8c4ca-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8c4ca-109">[Объект IMAPISession](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="8c4ca-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="8c4ca-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8c4ca-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c4ca-111">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="8c4ca-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="8c4ca-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8c4ca-112">Called by:</span></span>  <br/> |<span data-ttu-id="8c4ca-113">Клиент MAPI</span><span class="sxs-lookup"><span data-stu-id="8c4ca-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="8c4ca-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8c4ca-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8c4ca-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="8c4ca-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="8c4ca-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="8c4ca-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8c4ca-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="8c4ca-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8c4ca-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="8c4ca-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8c4ca-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="8c4ca-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="8c4ca-120">Запрашивает подсистему MAPI для поддержки быстрого отключения, предоставляемую загруженными поставщиками MAPI.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="8c4ca-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="8c4ca-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="8c4ca-122">Указывает намерение клиента MAPI приступить к закрытию.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="8c4ca-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="8c4ca-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="8c4ca-124">Указывает намерение клиента MAPI немедленно выйти из клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c4ca-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c4ca-125">Remarks</span></span>

<span data-ttu-id="8c4ca-126">Целью быстрого отключения является разрешение клиенту MAPI и любому загруженного поставщика MAPI, с которым клиент MAPI имеет активный сеанс MAPI для сохранения параметров и данных MAPI.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="8c4ca-127">Это позволяет клиенту MAPI отключить все внешние ссылки и выйти, не вызывая потери данных.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="8c4ca-128">Клиент MAPI, который должен выполнить быстрое отключение, должен использовать **интерфейс IMAPIClientShutdown.**</span><span class="sxs-lookup"><span data-stu-id="8c4ca-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="8c4ca-129">Клиент MAPI может получить указатель на этот интерфейс, позвонив методу IUnknown::QueryInterface на любом [объекте IMAPISession.](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="8c4ca-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="8c4ca-130">Клиент MAPI всегда инициирует быстрое отключение, вызывая **метод IMAPIClientShutdown::QueryFastShutdown.**</span><span class="sxs-lookup"><span data-stu-id="8c4ca-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="8c4ca-131">Подсистема MAPI отвечает на запрос клиента MAPI, проверяя, поддерживают ли загруженные поставщики MAPI быструю остановку клиента.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="8c4ca-132">Администратор может использовать Windows реестра, чтобы определить уровень поддержки поставщика, необходимой клиентам MAPI для быстрого отключения.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="8c4ca-133">Дополнительные сведения см. в [меню Fast Shutdown User Options.](fast-shutdown-user-options.md)</span><span class="sxs-lookup"><span data-stu-id="8c4ca-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="8c4ca-134">Чтобы перейти к быстрому отключению, клиент вызывает **метод IMAPIClientShutdown::NotifyProcessShutdown,** чтобы указать подсистеме MAPI намерение закрыться.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="8c4ca-135">Затем клиент вызывает **метод IMAPIClientShutdown::D FastShutdown,** чтобы указать, что клиентский процесс немедленно выходит.</span><span class="sxs-lookup"><span data-stu-id="8c4ca-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="8c4ca-136">Дополнительные сведения о быстром закрытии см. в [обзоре быстрого отключения.](fast-shutdown-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8c4ca-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="8c4ca-137">Сведения о том, как успешно выполнить быстрое отключение, см. в см. в руб. "Лучшие практики [для быстрого отключения".](best-practices-for-fast-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="8c4ca-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c4ca-138">См. также</span><span class="sxs-lookup"><span data-stu-id="8c4ca-138">See also</span></span>



[<span data-ttu-id="8c4ca-139">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="8c4ca-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="8c4ca-140">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="8c4ca-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

