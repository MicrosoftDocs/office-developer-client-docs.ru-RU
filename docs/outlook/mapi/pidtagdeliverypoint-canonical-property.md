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
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="fd6c1-103">Каноническое свойство PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="fd6c1-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="fd6c1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd6c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd6c1-105">Указывает природу функциональной сущности, с помощью которой сообщение было или было доставлено получателю.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd6c1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fd6c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd6c1-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="fd6c1-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="fd6c1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fd6c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd6c1-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="fd6c1-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="fd6c1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fd6c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="fd6c1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fd6c1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fd6c1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fd6c1-112">Area:</span></span>  <br/> |<span data-ttu-id="fd6c1-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="fd6c1-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd6c1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd6c1-114">Remarks</span></span>

<span data-ttu-id="fd6c1-115">Это свойство может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fd6c1-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="fd6c1-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="fd6c1-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="fd6c1-117">Доставленная в список рассылки точка доставки, которая, в свою очередь, может распространять сообщение среди многих получателей.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="fd6c1-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="fd6c1-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="fd6c1-119">Доставляется в хранилище сообщений, а не непосредственно получателю.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="fd6c1-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="fd6c1-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="fd6c1-121">Доставляется в единицу доступа (AU), за исключением физического блока доступа к доставке (PDAU), например в систему факсимилов.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="fd6c1-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="fd6c1-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="fd6c1-123">Доставляется в физическое подразделение доступа к доставке, например к почтовому оператору.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="fd6c1-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="fd6c1-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="fd6c1-125">Доставляется в физический клиент системы доставки, например обычный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="fd6c1-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="fd6c1-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="fd6c1-127">Доставляется частному агенту пользователей (UA), например клиенту в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="fd6c1-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="fd6c1-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="fd6c1-129">Доставлено агенту общедоступных пользователей или поставщику общедоступных услуг.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="fd6c1-130">По умолчанию значение MAPI_MH_DP_PRIVATE_UA, то есть клиент MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fd6c1-131">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fd6c1-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fd6c1-132">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="fd6c1-132">Header files</span></span>

<span data-ttu-id="fd6c1-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd6c1-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd6c1-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd6c1-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fd6c1-135">Mapitags.h</span></span>
  
> <span data-ttu-id="fd6c1-136">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="fd6c1-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd6c1-137">См. также</span><span class="sxs-lookup"><span data-stu-id="fd6c1-137">See also</span></span>



[<span data-ttu-id="fd6c1-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd6c1-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd6c1-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd6c1-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd6c1-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fd6c1-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd6c1-141">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="fd6c1-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

