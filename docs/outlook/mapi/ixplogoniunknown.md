---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ecfbf33641c86d4f162c521466ca2bf0b79a61d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581407"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="6177a-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6177a-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="6177a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6177a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6177a-105">Предоставляет доступ очереди MAPI для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="6177a-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6177a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6177a-106">Header file:</span></span>  <br/> |<span data-ttu-id="6177a-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="6177a-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="6177a-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="6177a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6177a-109">Объекты входа транспорта</span><span class="sxs-lookup"><span data-stu-id="6177a-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="6177a-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="6177a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6177a-111">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="6177a-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="6177a-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="6177a-112">Called by:</span></span>  <br/> |<span data-ttu-id="6177a-113">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="6177a-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="6177a-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="6177a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6177a-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="6177a-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="6177a-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="6177a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6177a-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="6177a-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6177a-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="6177a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6177a-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="6177a-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="6177a-120">Возвращает типы получателей, которые обрабатывают поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="6177a-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="6177a-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="6177a-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="6177a-122">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="6177a-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="6177a-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="6177a-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="6177a-124">Указывает на возникновение события, о том, какие поставщика транспорта запрошено уведомление.</span><span class="sxs-lookup"><span data-stu-id="6177a-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="6177a-125">Простоя</span><span class="sxs-lookup"><span data-stu-id="6177a-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="6177a-126">Указывает, что система не занята, включив поставщика транспорта для выполнения операций с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="6177a-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="6177a-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="6177a-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="6177a-128">Запускает процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="6177a-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="6177a-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="6177a-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="6177a-130">Указывает, что диспетчер очереди MAPI для поставщика транспорта для доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="6177a-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="6177a-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="6177a-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="6177a-132">Информирует поставщика транспорта, что диспетчер очереди MAPI завершения обработки на исходящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="6177a-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="6177a-133">Опрос</span><span class="sxs-lookup"><span data-stu-id="6177a-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="6177a-134">Указывает, поставщика транспорта, полученных одного или нескольких входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="6177a-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="6177a-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="6177a-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="6177a-136">Инициирует передачи входящих сообщений от поставщика транспорта диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="6177a-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="6177a-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="6177a-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="6177a-138">Открывает объект состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="6177a-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="6177a-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="6177a-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="6177a-140">Проверяет состояние внешних поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="6177a-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="6177a-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="6177a-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="6177a-142">Запросы, что поставщик транспорта сразу же доставить все ожидающие входящих или исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="6177a-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6177a-143">См. также</span><span class="sxs-lookup"><span data-stu-id="6177a-143">See also</span></span>



[<span data-ttu-id="6177a-144">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="6177a-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

