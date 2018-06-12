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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 0b16fba054533f1cb5d21f3f4b1788c073eca13b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809651"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="dcbb5-103">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcbb5-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="dcbb5-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dcbb5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dcbb5-105">Предоставляет доступ очереди MAPI для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcbb5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dcbb5-106">Header file:</span></span>  <br/> |<span data-ttu-id="dcbb5-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="dcbb5-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="dcbb5-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="dcbb5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="dcbb5-109">Объекты входа транспорта</span><span class="sxs-lookup"><span data-stu-id="dcbb5-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="dcbb5-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="dcbb5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="dcbb5-111">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="dcbb5-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="dcbb5-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="dcbb5-112">Called by:</span></span>  <br/> |<span data-ttu-id="dcbb5-113">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="dcbb5-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="dcbb5-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="dcbb5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dcbb5-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="dcbb5-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="dcbb5-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="dcbb5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="dcbb5-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="dcbb5-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dcbb5-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="dcbb5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dcbb5-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="dcbb5-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="dcbb5-120">Возвращает типы получателей, которые обрабатывают поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="dcbb5-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="dcbb5-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="dcbb5-122">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="dcbb5-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="dcbb5-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="dcbb5-124">Указывает на возникновение события, о том, какие поставщика транспорта запрошено уведомление.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-125">Простоя</span><span class="sxs-lookup"><span data-stu-id="dcbb5-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="dcbb5-126">Указывает, что система не занята, включив поставщика транспорта для выполнения операций с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="dcbb5-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="dcbb5-128">Запускает процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="dcbb5-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="dcbb5-130">Указывает, что диспетчер очереди MAPI для поставщика транспорта для доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="dcbb5-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="dcbb5-132">Информирует поставщика транспорта, что диспетчер очереди MAPI завершения обработки на исходящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-133">Опрос</span><span class="sxs-lookup"><span data-stu-id="dcbb5-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="dcbb5-134">Указывает, поставщика транспорта, полученных одного или нескольких входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="dcbb5-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="dcbb5-136">Инициирует передачи входящих сообщений от поставщика транспорта диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="dcbb5-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="dcbb5-138">Открывает объект состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="dcbb5-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="dcbb5-140">Проверяет состояние внешних поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="dcbb5-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="dcbb5-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="dcbb5-142">Запросы, что поставщик транспорта сразу же доставить все ожидающие входящих или исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="dcbb5-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dcbb5-143">См. также</span><span class="sxs-lookup"><span data-stu-id="dcbb5-143">See also</span></span>



[<span data-ttu-id="dcbb5-144">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="dcbb5-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

