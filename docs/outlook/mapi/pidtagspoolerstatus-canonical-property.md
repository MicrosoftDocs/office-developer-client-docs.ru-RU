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
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348211"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="5ac98-103">Каноническое свойство PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="5ac98-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="5ac98-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ac98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ac98-105">Содержит состояние сообщения на основе сведений, доступных для диспетчера очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ac98-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ac98-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5ac98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ac98-107">ПР_СПУЛЕР_СТАТУС</span><span class="sxs-lookup"><span data-stu-id="5ac98-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="5ac98-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5ac98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ac98-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="5ac98-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="5ac98-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5ac98-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ac98-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5ac98-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5ac98-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5ac98-112">Area:</span></span>  <br/> |<span data-ttu-id="5ac98-113">Несъемный MAPI</span><span class="sxs-lookup"><span data-stu-id="5ac98-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ac98-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ac98-114">Remarks</span></span>

<span data-ttu-id="5ac98-115">Это свойство вычисляется MAPI для объектов Message.</span><span class="sxs-lookup"><span data-stu-id="5ac98-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="5ac98-116">Это свойство отображается только для входящих сообщений и зарезервировано во всех остальных случаях.</span><span class="sxs-lookup"><span data-stu-id="5ac98-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="5ac98-117">Указывает, было ли сообщение доставлено в конечное расположение или же может ли поставщик обработчика сообщений удалить сообщение при его повторной маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="5ac98-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="5ac98-118">Клиентские приложения никогда не должны задавать это свойство.</span><span class="sxs-lookup"><span data-stu-id="5ac98-118">Client applications should never set this property.</span></span> <span data-ttu-id="5ac98-119">Для входящего сообщения клиент или поставщик услуг может вызвать [IMAPIProp::](imapiprop-getprops.md) /PROPS для этого свойства, чтобы определить состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="5ac98-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="5ac98-120">Значение S_OK указывает на то, что сообщение успешно доставлено в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="5ac98-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="5ac98-121">Значение МАПИ_Е_ОБЖЕКТ_ДЕЛЕТЕД указывает на то, что сообщение было удалено и не было зафиксировано в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5ac98-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="5ac98-122">Поставщики хранилища сообщений должны поддерживать это свойство в сообщениях, таблицах получателей и таблице исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="5ac98-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="5ac98-123">Клиенты и поставщики должны иметь возможность задавать столбцы в таблице исходящей очереди и ограничиваться в соответствии с этим свойством.</span><span class="sxs-lookup"><span data-stu-id="5ac98-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5ac98-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ac98-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5ac98-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="5ac98-125">Header files</span></span>

<span data-ttu-id="5ac98-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5ac98-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ac98-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5ac98-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ac98-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="5ac98-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5ac98-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="5ac98-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ac98-130">См. также</span><span class="sxs-lookup"><span data-stu-id="5ac98-130">See also</span></span>



[<span data-ttu-id="5ac98-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ac98-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ac98-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5ac98-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ac98-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5ac98-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ac98-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5ac98-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

