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
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="0302c-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0302c-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="0302c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0302c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0302c-105">Позволяет клиенту MAPI выполнять быстрое завершение клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="0302c-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0302c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0302c-106">Header file:</span></span>  <br/> |<span data-ttu-id="0302c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0302c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0302c-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="0302c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0302c-109">[Объект IMAPISession](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="0302c-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="0302c-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0302c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0302c-111">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="0302c-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="0302c-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0302c-112">Called by:</span></span>  <br/> |<span data-ttu-id="0302c-113">Клиент MAPI</span><span class="sxs-lookup"><span data-stu-id="0302c-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="0302c-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="0302c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0302c-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="0302c-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="0302c-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="0302c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0302c-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="0302c-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0302c-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="0302c-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0302c-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="0302c-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="0302c-120">Запрашивает поддержку быстрого завершения работы подсистемы MAPI, предоставляемую загруженными поставщиками MAPI.</span><span class="sxs-lookup"><span data-stu-id="0302c-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="0302c-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="0302c-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="0302c-122">Указывает на намерение клиента MAPI продолжить завершение работы.</span><span class="sxs-lookup"><span data-stu-id="0302c-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="0302c-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="0302c-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="0302c-124">Указывает на намерение клиента MAPI немедленно выйти из клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="0302c-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0302c-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="0302c-125">Remarks</span></span>

<span data-ttu-id="0302c-126">Быстрое завершение работы позволяет клиенту MAPI и любому загруженном поставщику MAPI, с которым у клиента MAPI есть активный сеанс MAPI, для сохранения параметров и данных MAPI.</span><span class="sxs-lookup"><span data-stu-id="0302c-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="0302c-127">Это позволяет клиенту MAPI отключать все внешние ссылки и выходить из нее без потери данных.</span><span class="sxs-lookup"><span data-stu-id="0302c-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="0302c-128">Клиент MAPI, который должен выполнять быстрое завершение работы, должен использовать интерфейс **IMAPIClientShutdown.**</span><span class="sxs-lookup"><span data-stu-id="0302c-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="0302c-129">Клиент MAPI может получить указатель на этот интерфейс, вызывая метод IUnknown::QueryInterface для любого объекта [IMAPISession.](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="0302c-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="0302c-130">Клиент MAPI всегда инициирует быстрое завершение работы, вызывая метод **IMAPIClientShutdown::QueryFastShutdown.**</span><span class="sxs-lookup"><span data-stu-id="0302c-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="0302c-131">Подсистема MAPI отвечает на запрос клиента MAPI, проверяя, поддерживают ли загруженные поставщики MAPI быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="0302c-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="0302c-132">Администратор может использовать параметры реестра Windows, чтобы определить уровень поддержки поставщика, необходимый клиентам MAPI для быстрого завершения работы.</span><span class="sxs-lookup"><span data-stu-id="0302c-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="0302c-133">Дополнительные сведения см. в параметрах пользователей быстрого [завершения работы.](fast-shutdown-user-options.md)</span><span class="sxs-lookup"><span data-stu-id="0302c-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="0302c-134">Чтобы продолжить быстрое завершение работы, клиент вызывает метод **IMAPIClientShutdown::NotifyProcessShutdown,** чтобы указать подсистеме MAPI намерение закрыть работу.</span><span class="sxs-lookup"><span data-stu-id="0302c-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="0302c-135">Затем клиент вызывает метод **IMAPIClientShutdown::D oFastShutdown,** чтобы указать, что клиентский процесс немедленно выходит из процесса.</span><span class="sxs-lookup"><span data-stu-id="0302c-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="0302c-136">Дополнительные сведения о быстром отключении см. в [обзоре быстрого завершения работы.](fast-shutdown-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0302c-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="0302c-137">Сведения о том, как успешно выполнить быстрое завершение работы, см. в ["Best Practices for Fast Shutdown".](best-practices-for-fast-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="0302c-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0302c-138">См. также</span><span class="sxs-lookup"><span data-stu-id="0302c-138">See also</span></span>



[<span data-ttu-id="0302c-139">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="0302c-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="0302c-140">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="0302c-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

