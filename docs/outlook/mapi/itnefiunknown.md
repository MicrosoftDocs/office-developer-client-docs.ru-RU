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
ms.openlocfilehash: 1803707b46b9b58e7372e7e58cc36241d0ebdb4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571726"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="b6a4c-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6a4c-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="b6a4c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6a4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6a4c-105">Предоставляет методы для инкапсуляции свойства MAPI, не поддерживаемые системой обмена сообщениями в двоичные потоки, которые можно присоединить к сообщениям.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="b6a4c-106">Формат, используемый для этой инкапсуляция — Transport-Neutral Encapsulation формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="b6a4c-107">Целевой поставщика транспорта или на основе MAPI клиентское приложение можно, получив сообщение, содержащее вложения TNEF, восстановить свойства из вложения.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6a4c-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b6a4c-108">Header file:</span></span>  <br/> |<span data-ttu-id="b6a4c-109">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="b6a4c-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="b6a4c-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="b6a4c-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="b6a4c-111">Объекты TNEF</span><span class="sxs-lookup"><span data-stu-id="b6a4c-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="b6a4c-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b6a4c-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="b6a4c-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="b6a4c-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="b6a4c-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b6a4c-114">Called by:</span></span>  <br/> |<span data-ttu-id="b6a4c-115">Поставщики транспорта, поставщиков хранилища сообщений и шлюзов</span><span class="sxs-lookup"><span data-stu-id="b6a4c-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="b6a4c-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b6a4c-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b6a4c-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="b6a4c-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="b6a4c-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="b6a4c-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="b6a4c-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="b6a4c-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b6a4c-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="b6a4c-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b6a4c-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="b6a4c-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="b6a4c-122">Позволяет вызова поставщика услуг или шлюза добавить свойства к инкапсуляция вложения или сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="b6a4c-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="b6a4c-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="b6a4c-124">Извлекает свойства из инкапсуляция TNEF.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="b6a4c-125">Готово</span><span class="sxs-lookup"><span data-stu-id="b6a4c-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="b6a4c-126">По завершении обработки для всех операций TNEF в очереди и ожидание.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="b6a4c-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="b6a4c-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="b6a4c-128">Открывает интерфейс потока на основе текста инкапсулированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="b6a4c-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="b6a4c-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="b6a4c-130">Задает значение одного или нескольких свойств для инкапсулированное сообщение или вложение без изменения исходного сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="b6a4c-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="b6a4c-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="b6a4c-132">Кодирует представления для таблицы получателей сообщения в потоке данных TNEF для сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="b6a4c-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="b6a4c-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="b6a4c-134">Обрабатывает отдельные компоненты из сообщения одно за раз в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="b6a4c-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6a4c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b6a4c-135">See also</span></span>



[<span data-ttu-id="b6a4c-136">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="b6a4c-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

