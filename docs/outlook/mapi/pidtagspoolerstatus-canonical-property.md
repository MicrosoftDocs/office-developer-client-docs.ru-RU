---
title: Каноническое свойство PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d04144a4f5ef714b59b608bfe19367bcb3c1ced8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588575"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="93425-103">Каноническое свойство PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="93425-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="93425-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93425-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93425-105">Отображается состояние сообщения на основе сведений, которые могут диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="93425-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93425-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="93425-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93425-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="93425-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="93425-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="93425-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93425-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="93425-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="93425-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="93425-110">Data type:</span></span>  <br/> |<span data-ttu-id="93425-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="93425-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="93425-112">Область:</span><span class="sxs-lookup"><span data-stu-id="93425-112">Area:</span></span>  <br/> |<span data-ttu-id="93425-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="93425-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93425-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="93425-114">Remarks</span></span>

<span data-ttu-id="93425-115">Это свойство вычисляется путем MAPI на объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="93425-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="93425-116">Это свойство отображается только входящих сообщений и зарезервирован во всех остальных случаях.</span><span class="sxs-lookup"><span data-stu-id="93425-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="93425-117">Он указывает ли сообщение было доставлено в конечное расположение или обмена мгновенными сообщениями поставщика обработчик потенциально удалена ли сообщение во время его маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="93425-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="93425-118">Клиентские приложения никогда не следует устанавливать это свойство.</span><span class="sxs-lookup"><span data-stu-id="93425-118">Client applications should never set this property.</span></span> <span data-ttu-id="93425-119">Для входящего сообщения клиента или поставщика можно вызвать [IMAPIProp::GetProps](imapiprop-getprops.md) на это свойство, чтобы определить состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="93425-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="93425-120">Значение S_OK указывает, что сообщение было успешно доставлено в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="93425-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="93425-121">Значение MAPI_E_OBJECT_DELETED указывает, что сообщение было удалено и никогда не было зафиксировано в хранилище.</span><span class="sxs-lookup"><span data-stu-id="93425-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="93425-122">Поставщики хранилища сообщений должны поддерживать это свойство на сообщения, получателя таблиц и таблице исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="93425-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="93425-123">Клиенты и поставщики должна появиться возможность задать столбцы в таблице исходящей очереди и ограничения на основе этого свойства.</span><span class="sxs-lookup"><span data-stu-id="93425-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93425-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="93425-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="93425-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="93425-125">Header files</span></span>

<span data-ttu-id="93425-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93425-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="93425-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="93425-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="93425-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93425-128">Mapitags.h</span></span>
  
> <span data-ttu-id="93425-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="93425-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93425-130">См. также</span><span class="sxs-lookup"><span data-stu-id="93425-130">See also</span></span>



[<span data-ttu-id="93425-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93425-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93425-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93425-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93425-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="93425-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93425-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="93425-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

