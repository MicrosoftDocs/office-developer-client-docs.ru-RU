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
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811064"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="a4af4-103">Каноническое свойство PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="a4af4-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="a4af4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4af4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4af4-105">Определяет характер функциональным сущности, с помощью которого был или будет доставлено получателю сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4af4-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4af4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a4af4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4af4-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="a4af4-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="a4af4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a4af4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4af4-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="a4af4-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="a4af4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a4af4-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4af4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a4af4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a4af4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a4af4-112">Area:</span></span>  <br/> |<span data-ttu-id="a4af4-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="a4af4-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4af4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4af4-114">Remarks</span></span>

<span data-ttu-id="a4af4-115">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a4af4-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="a4af4-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="a4af4-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="a4af4-117">Доставлено в список рассылки, отделения который в свою очередь может распространять сообщения большому количеству получателей.</span><span class="sxs-lookup"><span data-stu-id="a4af4-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="a4af4-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="a4af4-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="a4af4-119">Доставлено сообщение магазин вместо непосредственно получателю.</span><span class="sxs-lookup"><span data-stu-id="a4af4-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="a4af4-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="a4af4-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="a4af4-121">Доставки единице доступа (AU), отличный от физических доставки доступа единицу измерения (PDAU), таких как система ФАКСОВ.</span><span class="sxs-lookup"><span data-stu-id="a4af4-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="a4af4-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="a4af4-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="a4af4-123">Доставлено единицы доступа физических доставки, например человеческого почтовый поставщика.</span><span class="sxs-lookup"><span data-stu-id="a4af4-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="a4af4-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="a4af4-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="a4af4-125">Доставлено patron физических доставки системы, такие как обычное почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="a4af4-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="a4af4-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="a4af4-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="a4af4-127">Доставлено агент закрытый пользователя (UA), такие как клиент внутренних почтовых систем.</span><span class="sxs-lookup"><span data-stu-id="a4af4-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="a4af4-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="a4af4-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="a4af4-129">Доставлено агентов пользователей общедоступных служб или поставщик услуг public.</span><span class="sxs-lookup"><span data-stu-id="a4af4-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="a4af4-130">Значение по умолчанию — MAPI_MH_DP_PRIVATE_UA, то есть, клиент MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4af4-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a4af4-131">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a4af4-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a4af4-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a4af4-132">Header files</span></span>

<span data-ttu-id="a4af4-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4af4-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4af4-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a4af4-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4af4-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4af4-135">Mapitags.h</span></span>
  
> <span data-ttu-id="a4af4-136">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a4af4-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4af4-137">См. также</span><span class="sxs-lookup"><span data-stu-id="a4af4-137">See also</span></span>



[<span data-ttu-id="a4af4-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a4af4-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4af4-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a4af4-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4af4-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a4af4-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4af4-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a4af4-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

