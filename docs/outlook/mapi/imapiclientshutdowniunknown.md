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
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808841"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="00edf-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00edf-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="00edf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00edf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00edf-105">Включение клиент MAPI выполнить быстрое завершение работы процесса клиента.</span><span class="sxs-lookup"><span data-stu-id="00edf-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00edf-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="00edf-106">Header file:</span></span>  <br/> |<span data-ttu-id="00edf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00edf-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="00edf-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="00edf-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="00edf-109">Объект [IMAPISession](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="00edf-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="00edf-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="00edf-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="00edf-111">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="00edf-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="00edf-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="00edf-112">Called by:</span></span>  <br/> |<span data-ttu-id="00edf-113">Клиент MAPI</span><span class="sxs-lookup"><span data-stu-id="00edf-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="00edf-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="00edf-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="00edf-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="00edf-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="00edf-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="00edf-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="00edf-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="00edf-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="00edf-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="00edf-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="00edf-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="00edf-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="00edf-120">Запросы в подсистеме MAPI для быстрое завершение работы поддерживают, предоставленные загруженных поставщики MAPI.</span><span class="sxs-lookup"><span data-stu-id="00edf-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="00edf-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="00edf-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="00edf-122">Показывает завершена намерения клиент MAPI для продолжения.</span><span class="sxs-lookup"><span data-stu-id="00edf-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="00edf-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="00edf-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="00edf-124">Указывает намерения клиент MAPI, чтобы выйти из клиентского процесса немедленно.</span><span class="sxs-lookup"><span data-stu-id="00edf-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00edf-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="00edf-125">Remarks</span></span>

<span data-ttu-id="00edf-126">Быстрое завершение работы это позволяет клиент MAPI и любые загруженных поставщика MAPI, с которым клиент MAPI имеет активного сеанса MAPI для сохранения параметров MAPI и данных.</span><span class="sxs-lookup"><span data-stu-id="00edf-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="00edf-127">Это позволяет клиент MAPI для отключения всех внешних ссылок и выйдите из без причиной потери данных.</span><span class="sxs-lookup"><span data-stu-id="00edf-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="00edf-128">Клиент MAPI, которую необходимо выполнить быстрое завершение работы необходимо использовать интерфейс **IMAPIClientShutdown** .</span><span class="sxs-lookup"><span data-stu-id="00edf-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="00edf-129">Клиент MAPI можно получить путем вызова метода IUnknown::QueryInterface для любого объекта [IMAPISession](imapisessioniunknown.md) указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="00edf-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="00edf-130">Клиент MAPI всегда инициирует быстрое завершение работы путем вызова метода **IMAPIClientShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="00edf-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="00edf-131">Подсистема MAPI отвечает на запрос клиент MAPI, проверяя, поддерживает ли загруженных поставщики MAPI быстрое завершение работы клиента.</span><span class="sxs-lookup"><span data-stu-id="00edf-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="00edf-132">Администратор может использовать параметры реестра Windows для определения уровень поддержки поставщика, которая требуется для клиентов MAPI продолжить работу быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="00edf-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="00edf-133">Для получения дополнительных сведений см [Fast параметры завершения работы пользователя](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="00edf-134">Для продолжения быстрое завершение работы клиента вызывает метод **IMAPIClientShutdown::NotifyProcessShutdown** для указания подсистемы MAPI намерения завершить работу.</span><span class="sxs-lookup"><span data-stu-id="00edf-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="00edf-135">Клиент затем вызывает метод **IMAPIClientShutdown::DoFastShutdown** для указания, что процесс клиента завершает работу сразу же.</span><span class="sxs-lookup"><span data-stu-id="00edf-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="00edf-136">Дополнительные сведения о быстрое завершение работы см [быстрое завершение работы](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="00edf-137">Сведения о том, как успешно выполнить быстрое завершение работы, [рекомендации](best-practices-for-fast-shutdown.md)по быстрое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="00edf-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00edf-138">См. также</span><span class="sxs-lookup"><span data-stu-id="00edf-138">See also</span></span>



[<span data-ttu-id="00edf-139">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="00edf-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="00edf-140">Завершение работы клиента в MAPI</span><span class="sxs-lookup"><span data-stu-id="00edf-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

