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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315038"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="bead3-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bead3-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="bead3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bead3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bead3-105">Предоставляет методы инкапсуляции свойств MAPI, которые не поддерживаются системой обмена сообщениями в двоичные потоки, которые можно вложить в сообщения.</span><span class="sxs-lookup"><span data-stu-id="bead3-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="bead3-106">Для этой инкапсуляции используется формат TNEF, не зависящий от транспорта.</span><span class="sxs-lookup"><span data-stu-id="bead3-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="bead3-107">Целевой поставщик транспорта или клиентское приложение на основе MAPI могут затем при получении сообщения, которое содержит вложение в формате TNEF, восстановите свойства из вложения.</span><span class="sxs-lookup"><span data-stu-id="bead3-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bead3-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bead3-108">Header file:</span></span>  <br/> |<span data-ttu-id="bead3-109">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="bead3-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="bead3-110">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="bead3-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="bead3-111">Объекты TNEF</span><span class="sxs-lookup"><span data-stu-id="bead3-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="bead3-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="bead3-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="bead3-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="bead3-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="bead3-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="bead3-114">Called by:</span></span>  <br/> |<span data-ttu-id="bead3-115">Поставщики транспорта, поставщики хранилищ сообщений и шлюзы</span><span class="sxs-lookup"><span data-stu-id="bead3-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="bead3-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="bead3-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bead3-117">ИИД_ИТНЕФ</span><span class="sxs-lookup"><span data-stu-id="bead3-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="bead3-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="bead3-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="bead3-119">ЛПТНЕФ</span><span class="sxs-lookup"><span data-stu-id="bead3-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bead3-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="bead3-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bead3-121">Аддпропс</span><span class="sxs-lookup"><span data-stu-id="bead3-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="bead3-122">Позволяет поставщику или шлюзу службы вызывающей службы добавлять свойства в инкапсуляцию сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="bead3-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="bead3-123">Екстрактпропс</span><span class="sxs-lookup"><span data-stu-id="bead3-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="bead3-124">Извлекает свойства из инкапсуляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="bead3-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="bead3-125">Finish</span><span class="sxs-lookup"><span data-stu-id="bead3-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="bead3-126">Завершает обработку всех операций TNEF, которые находятся в очереди и ожидают.</span><span class="sxs-lookup"><span data-stu-id="bead3-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="bead3-127">Опентагжедбоди</span><span class="sxs-lookup"><span data-stu-id="bead3-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="bead3-128">Открывает потоковый интерфейс на тексте инкапсулированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="bead3-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="bead3-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="bead3-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="bead3-130">Задает значение одного или нескольких свойств для инкапсулированного сообщения или вложения, не изменяя исходное сообщение или вложение.</span><span class="sxs-lookup"><span data-stu-id="bead3-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="bead3-131">ЕнкодереЦипс</span><span class="sxs-lookup"><span data-stu-id="bead3-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="bead3-132">Кодирует представление таблицы получателей сообщения в потоке данных TNEF для сообщения.</span><span class="sxs-lookup"><span data-stu-id="bead3-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="bead3-133">Финишкомпонент</span><span class="sxs-lookup"><span data-stu-id="bead3-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="bead3-134">Обрабатывает отдельные компоненты из сообщения по одному за раз в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="bead3-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bead3-135">См. также</span><span class="sxs-lookup"><span data-stu-id="bead3-135">See also</span></span>



[<span data-ttu-id="bead3-136">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="bead3-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

