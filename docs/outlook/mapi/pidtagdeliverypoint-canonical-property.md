---
title: Каноническое свойство PidTagDeliveryPoint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439424"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="300a8-103">Каноническое свойство PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="300a8-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="300a8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="300a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="300a8-105">Определяет характер функциональной сущности, с помощью которой сообщение было или было бы доставлено получателю.</span><span class="sxs-lookup"><span data-stu-id="300a8-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="300a8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="300a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="300a8-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="300a8-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="300a8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="300a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="300a8-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="300a8-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="300a8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="300a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="300a8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="300a8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="300a8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="300a8-112">Area:</span></span>  <br/> |<span data-ttu-id="300a8-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="300a8-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="300a8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="300a8-114">Remarks</span></span>

<span data-ttu-id="300a8-115">Это свойство может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="300a8-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="300a8-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="300a8-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="300a8-117">Доставляется в список рассылки, точку доставки, которая, в свою очередь, может распространять сообщение среди многих получателей.</span><span class="sxs-lookup"><span data-stu-id="300a8-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="300a8-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="300a8-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="300a8-119">Доставляется в хранилище сообщений, а не непосредственно получателю.</span><span class="sxs-lookup"><span data-stu-id="300a8-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="300a8-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="300a8-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="300a8-121">Доставляется в единицу доступа (AU), которая не является физической единицей доступа для доставки (PDAU), например в систему факсов.</span><span class="sxs-lookup"><span data-stu-id="300a8-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="300a8-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="300a8-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="300a8-123">Доставляется в физическое подразделение доступа к доставке, например почтовому оператору.</span><span class="sxs-lookup"><span data-stu-id="300a8-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="300a8-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="300a8-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="300a8-125">Доставляется в физический почтовый ящик, например обычный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="300a8-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="300a8-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="300a8-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="300a8-127">Доставляется агенту частного пользователя (UA), например клиенту в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="300a8-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="300a8-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="300a8-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="300a8-129">Доставляется агенту общедоступных пользователей или поставщику общедоступных служб.</span><span class="sxs-lookup"><span data-stu-id="300a8-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="300a8-130">Значение по умолчанию — MAPI_MH_DP_PRIVATE_UA, то есть клиент MAPI.</span><span class="sxs-lookup"><span data-stu-id="300a8-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="300a8-131">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="300a8-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="300a8-132">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="300a8-132">Header files</span></span>

<span data-ttu-id="300a8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="300a8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="300a8-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="300a8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="300a8-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="300a8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="300a8-136">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="300a8-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="300a8-137">См. также</span><span class="sxs-lookup"><span data-stu-id="300a8-137">See also</span></span>



[<span data-ttu-id="300a8-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="300a8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="300a8-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="300a8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="300a8-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="300a8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="300a8-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="300a8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

