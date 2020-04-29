---
title: Итнеф IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428517"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="2f8ca-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f8ca-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="2f8ca-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f8ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f8ca-105">Предоставляет методы инкапсуляции свойств MAPI, которые не поддерживаются системой обмена сообщениями в двоичные потоки, которые можно вложить в сообщения.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="2f8ca-106">Для этой инкапсуляции используется формат TNEF, не зависящий от транспорта.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="2f8ca-107">Целевой поставщик транспорта или клиентское приложение на основе MAPI могут затем при получении сообщения, которое содержит вложение в формате TNEF, восстановите свойства из вложения.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f8ca-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2f8ca-108">Header file:</span></span>  <br/> |<span data-ttu-id="2f8ca-109">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="2f8ca-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="2f8ca-110">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="2f8ca-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="2f8ca-111">Объекты TNEF</span><span class="sxs-lookup"><span data-stu-id="2f8ca-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="2f8ca-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2f8ca-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f8ca-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="2f8ca-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="2f8ca-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2f8ca-114">Called by:</span></span>  <br/> |<span data-ttu-id="2f8ca-115">Поставщики транспорта, поставщики хранилищ сообщений и шлюзы</span><span class="sxs-lookup"><span data-stu-id="2f8ca-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="2f8ca-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="2f8ca-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2f8ca-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="2f8ca-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="2f8ca-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="2f8ca-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="2f8ca-119">лптнеф</span><span class="sxs-lookup"><span data-stu-id="2f8ca-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2f8ca-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="2f8ca-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2f8ca-121">аддпропс</span><span class="sxs-lookup"><span data-stu-id="2f8ca-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="2f8ca-122">Позволяет поставщику или шлюзу службы вызывающей службы добавлять свойства в инкапсуляцию сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="2f8ca-123">екстрактпропс</span><span class="sxs-lookup"><span data-stu-id="2f8ca-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="2f8ca-124">Извлекает свойства из инкапсуляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="2f8ca-125">Finish</span><span class="sxs-lookup"><span data-stu-id="2f8ca-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="2f8ca-126">Завершает обработку всех операций TNEF, которые находятся в очереди и ожидают.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="2f8ca-127">опентагжедбоди</span><span class="sxs-lookup"><span data-stu-id="2f8ca-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="2f8ca-128">Открывает потоковый интерфейс на тексте инкапсулированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="2f8ca-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="2f8ca-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="2f8ca-130">Задает значение одного или нескольких свойств для инкапсулированного сообщения или вложения, не изменяя исходное сообщение или вложение.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="2f8ca-131">енкодереЦипс</span><span class="sxs-lookup"><span data-stu-id="2f8ca-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="2f8ca-132">Кодирует представление таблицы получателей сообщения в потоке данных TNEF для сообщения.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="2f8ca-133">финишкомпонент</span><span class="sxs-lookup"><span data-stu-id="2f8ca-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="2f8ca-134">Обрабатывает отдельные компоненты из сообщения по одному за раз в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="2f8ca-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f8ca-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2f8ca-135">See also</span></span>



[<span data-ttu-id="2f8ca-136">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="2f8ca-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

