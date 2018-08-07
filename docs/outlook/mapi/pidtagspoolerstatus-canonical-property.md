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
ms.openlocfilehash: df52f668e91b707c0436b394186b27fdbb3a5dbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811951"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="87954-103">Каноническое свойство PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="87954-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="87954-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87954-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87954-105">Отображается состояние сообщения на основе сведений, которые могут диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="87954-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87954-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="87954-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87954-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="87954-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="87954-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="87954-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87954-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="87954-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="87954-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="87954-110">Data type:</span></span>  <br/> |<span data-ttu-id="87954-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87954-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87954-112">Область:</span><span class="sxs-lookup"><span data-stu-id="87954-112">Area:</span></span>  <br/> |<span data-ttu-id="87954-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="87954-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87954-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="87954-114">Remarks</span></span>

<span data-ttu-id="87954-115">Это свойство вычисляется путем MAPI на объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="87954-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="87954-116">Это свойство отображается только входящих сообщений и зарезервирован во всех остальных случаях.</span><span class="sxs-lookup"><span data-stu-id="87954-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="87954-117">Он указывает ли сообщение было доставлено в конечное расположение или обмена мгновенными сообщениями поставщика обработчик потенциально удалена ли сообщение во время его маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="87954-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="87954-118">Клиентские приложения никогда не следует устанавливать это свойство.</span><span class="sxs-lookup"><span data-stu-id="87954-118">Client applications should never set this property.</span></span> <span data-ttu-id="87954-119">Для входящего сообщения клиента или поставщика можно вызвать [IMAPIProp::GetProps](imapiprop-getprops.md) на это свойство, чтобы определить состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="87954-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="87954-120">Значение S_OK указывает, что сообщение было успешно доставлено в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="87954-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="87954-121">Значение MAPI_E_OBJECT_DELETED указывает, что сообщение было удалено и никогда не было зафиксировано в хранилище.</span><span class="sxs-lookup"><span data-stu-id="87954-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="87954-122">Поставщики хранилища сообщений должны поддерживать это свойство на сообщения, получателя таблиц и таблице исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="87954-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="87954-123">Клиенты и поставщики должна появиться возможность задать столбцы в таблице исходящей очереди и ограничения на основе этого свойства.</span><span class="sxs-lookup"><span data-stu-id="87954-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87954-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="87954-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="87954-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="87954-125">Header files</span></span>

<span data-ttu-id="87954-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87954-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="87954-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="87954-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="87954-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="87954-128">Mapitags.h</span></span>
  
> <span data-ttu-id="87954-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="87954-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87954-130">См. также</span><span class="sxs-lookup"><span data-stu-id="87954-130">See also</span></span>



[<span data-ttu-id="87954-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="87954-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87954-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="87954-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87954-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="87954-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87954-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="87954-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

