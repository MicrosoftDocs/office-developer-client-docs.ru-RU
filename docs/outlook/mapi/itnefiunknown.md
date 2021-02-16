---
title: ITnef IUnknown
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
# <a name="itnef--iunknown"></a><span data-ttu-id="57217-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57217-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="57217-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57217-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57217-105">Предоставляет методы для инкапсуляция свойств MAPI, которые не поддерживаются системой обмена сообщениями, в двоичные потоки, которые можно встроить в сообщения.</span><span class="sxs-lookup"><span data-stu-id="57217-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="57217-106">Формат, используемый для этого инкапсуляции, Transport-Neutral формат инкапсуляции (TNEF).</span><span class="sxs-lookup"><span data-stu-id="57217-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="57217-107">Затем целевой поставщик транспорта или клиентские приложения на основе MAPI могут при получении сообщения, которое содержит вложение TNEF, восстановить свойства из вложения.</span><span class="sxs-lookup"><span data-stu-id="57217-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="57217-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="57217-108">Header file:</span></span>  <br/> |<span data-ttu-id="57217-109">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="57217-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="57217-110">Выставим:</span><span class="sxs-lookup"><span data-stu-id="57217-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="57217-111">Объекты TNEF</span><span class="sxs-lookup"><span data-stu-id="57217-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="57217-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="57217-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="57217-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="57217-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="57217-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="57217-114">Called by:</span></span>  <br/> |<span data-ttu-id="57217-115">Поставщики транспорта, поставщики store сообщений и шлюзы</span><span class="sxs-lookup"><span data-stu-id="57217-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="57217-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="57217-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="57217-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="57217-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="57217-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="57217-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="57217-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="57217-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="57217-120">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="57217-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="57217-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="57217-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="57217-122">Позволяет поставщику или шлюзу вызываемой службы добавлять свойства в инкапсуляцию сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="57217-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="57217-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="57217-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="57217-124">Извлекает свойства из инкапсуляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="57217-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="57217-125">Finish</span><span class="sxs-lookup"><span data-stu-id="57217-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="57217-126">Завершает обработку всех операций TNEF, которые находятся в очереди и ожидают их.</span><span class="sxs-lookup"><span data-stu-id="57217-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="57217-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="57217-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="57217-128">Открывает интерфейс потока в тексте инкапсулированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="57217-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="57217-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="57217-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="57217-130">Задает значение одного или более свойств инкапсулированного сообщения или вложения без изменения исходного сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="57217-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="57217-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="57217-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="57217-132">Кодирует представление таблицы получателей сообщения в потоке данных TNEF для сообщения.</span><span class="sxs-lookup"><span data-stu-id="57217-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="57217-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="57217-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="57217-134">Обрабатывает отдельные компоненты из сообщения по одному в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="57217-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57217-135">См. также</span><span class="sxs-lookup"><span data-stu-id="57217-135">See also</span></span>



[<span data-ttu-id="57217-136">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="57217-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

