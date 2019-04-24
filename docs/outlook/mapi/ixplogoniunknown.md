---
title: Иксплогон IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282798"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="451a8-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="451a8-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="451a8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="451a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="451a8-105">Предоставляет диспетчеру очереди MAPI доступ к поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="451a8-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="451a8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="451a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="451a8-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="451a8-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="451a8-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="451a8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="451a8-109">Объекты входа в систему</span><span class="sxs-lookup"><span data-stu-id="451a8-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="451a8-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="451a8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="451a8-111">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="451a8-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="451a8-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="451a8-112">Called by:</span></span>  <br/> |<span data-ttu-id="451a8-113">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="451a8-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="451a8-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="451a8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="451a8-115">Иид_иксплогон</span><span class="sxs-lookup"><span data-stu-id="451a8-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="451a8-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="451a8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="451a8-117">ЛКСПЛОГОН</span><span class="sxs-lookup"><span data-stu-id="451a8-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="451a8-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="451a8-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="451a8-119">Аддресстипес</span><span class="sxs-lookup"><span data-stu-id="451a8-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="451a8-120">Возвращает типы получателей, которые обрабатывает поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="451a8-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="451a8-121">**Регистероптионс**</span><span class="sxs-lookup"><span data-stu-id="451a8-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="451a8-122">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="451a8-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="451a8-123">Транспортнотифи</span><span class="sxs-lookup"><span data-stu-id="451a8-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="451a8-124">Сигнализирует о возникновении события, о котором было запрошено уведомление поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="451a8-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="451a8-125">Простоя</span><span class="sxs-lookup"><span data-stu-id="451a8-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="451a8-126">Указывает на то, что система находится в режиме бездействия, что позволяет поставщику транспорта выполнять операции с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="451a8-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="451a8-127">Транспортлогофф</span><span class="sxs-lookup"><span data-stu-id="451a8-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="451a8-128">Инициирует процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="451a8-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="451a8-129">Субмитмессаже</span><span class="sxs-lookup"><span data-stu-id="451a8-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="451a8-130">Указывает на то, что диспетчер очереди MAPI имеет сообщение, которое будет доставлено поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="451a8-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="451a8-131">Ендмессаже</span><span class="sxs-lookup"><span data-stu-id="451a8-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="451a8-132">Информирует поставщика транспорта о том, что диспетчер очереди MAPI закончил обработку исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="451a8-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="451a8-133">Предмет</span><span class="sxs-lookup"><span data-stu-id="451a8-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="451a8-134">Указывает, получил ли поставщик транспорта одно или несколько входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="451a8-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="451a8-135">Стартмессаже</span><span class="sxs-lookup"><span data-stu-id="451a8-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="451a8-136">Инициирует передачу входящего сообщения от поставщика транспорта в Диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="451a8-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="451a8-137">Опенстатусентри</span><span class="sxs-lookup"><span data-stu-id="451a8-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="451a8-138">Открывает объект состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="451a8-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="451a8-139">Валидатестате</span><span class="sxs-lookup"><span data-stu-id="451a8-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="451a8-140">Проверяет внешнее состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="451a8-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="451a8-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="451a8-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="451a8-142">Отправляет поставщику транспорта немедленное предоставление всех ожидающих входящих и исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="451a8-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="451a8-143">См. также</span><span class="sxs-lookup"><span data-stu-id="451a8-143">See also</span></span>



[<span data-ttu-id="451a8-144">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="451a8-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

