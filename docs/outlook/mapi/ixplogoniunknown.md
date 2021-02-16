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
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432536"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="960a3-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="960a3-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="960a3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="960a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="960a3-105">Предоставляет поставщику транспорта доступ к пулу MAPI.</span><span class="sxs-lookup"><span data-stu-id="960a3-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="960a3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="960a3-106">Header file:</span></span>  <br/> |<span data-ttu-id="960a3-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="960a3-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="960a3-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="960a3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="960a3-109">Транспортные объекты для логотипа</span><span class="sxs-lookup"><span data-stu-id="960a3-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="960a3-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="960a3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="960a3-111">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="960a3-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="960a3-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="960a3-112">Called by:</span></span>  <br/> |<span data-ttu-id="960a3-113">Пулер MAPI</span><span class="sxs-lookup"><span data-stu-id="960a3-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="960a3-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="960a3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="960a3-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="960a3-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="960a3-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="960a3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="960a3-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="960a3-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="960a3-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="960a3-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="960a3-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="960a3-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="960a3-120">Возвращает типы получателей, обрабатываемого поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="960a3-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="960a3-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="960a3-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="960a3-122">*Не поддерживается и не документируется.*</span><span class="sxs-lookup"><span data-stu-id="960a3-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="960a3-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="960a3-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="960a3-124">Сигнализирует о возникновении события, о котором поставщик транспорта запросил уведомление.</span><span class="sxs-lookup"><span data-stu-id="960a3-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="960a3-125">Бездействие</span><span class="sxs-lookup"><span data-stu-id="960a3-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="960a3-126">Указывает, что система простаивает, что позволяет поставщику транспорта выполнять операции с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="960a3-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="960a3-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="960a3-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="960a3-128">Инициирует процесс выйдите из нее.</span><span class="sxs-lookup"><span data-stu-id="960a3-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="960a3-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="960a3-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="960a3-130">Указывает, что у пула MAPI есть сообщение, которое должен доставить поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="960a3-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="960a3-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="960a3-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="960a3-132">Сообщает поставщику транспорта, что пул MAPI завершил обработку исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="960a3-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="960a3-133">Опрос</span><span class="sxs-lookup"><span data-stu-id="960a3-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="960a3-134">Указывает, получил ли поставщик транспорта одно или несколько входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="960a3-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="960a3-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="960a3-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="960a3-136">Инициирует передачу входящие сообщения от поставщика транспорта в пулер MAPI.</span><span class="sxs-lookup"><span data-stu-id="960a3-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="960a3-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="960a3-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="960a3-138">Открывает объект состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="960a3-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="960a3-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="960a3-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="960a3-140">Проверяет внешнее состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="960a3-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="960a3-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="960a3-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="960a3-142">Запрашивает у поставщика транспорта немедленно доставить все ожидающих входящие или исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="960a3-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="960a3-143">См. также</span><span class="sxs-lookup"><span data-stu-id="960a3-143">See also</span></span>



[<span data-ttu-id="960a3-144">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="960a3-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

