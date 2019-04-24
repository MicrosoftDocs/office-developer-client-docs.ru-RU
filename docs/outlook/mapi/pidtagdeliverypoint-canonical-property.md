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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360881"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="87056-103">Каноническое свойство PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="87056-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="87056-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87056-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87056-105">Указывает природу функционального объекта, с помощью которого сообщение было доставлено получателю или было доставлено ему.</span><span class="sxs-lookup"><span data-stu-id="87056-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87056-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="87056-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87056-107">ПР_ДЕЛИВЕРИ_ПОИНТ</span><span class="sxs-lookup"><span data-stu-id="87056-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="87056-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="87056-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87056-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="87056-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="87056-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="87056-110">Data type:</span></span>  <br/> |<span data-ttu-id="87056-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87056-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87056-112">Область:</span><span class="sxs-lookup"><span data-stu-id="87056-112">Area:</span></span>  <br/> |<span data-ttu-id="87056-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="87056-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87056-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="87056-114">Remarks</span></span>

<span data-ttu-id="87056-115">Это свойство может иметь только одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="87056-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="87056-116">МАПИ_МХ_ДП_МЛ</span><span class="sxs-lookup"><span data-stu-id="87056-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="87056-117">ДоСтавляется в список рассылки, точка доставки, в свою очередь, может распространять сообщение нескольким получателям.</span><span class="sxs-lookup"><span data-stu-id="87056-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="87056-118">МАПИ_МХ_ДП_МС</span><span class="sxs-lookup"><span data-stu-id="87056-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="87056-119">ДоСтавляется в хранилище сообщений, а не непосредственно получателю.</span><span class="sxs-lookup"><span data-stu-id="87056-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="87056-120">МАПИ_МХ_ДП_ОСЕР_АУ</span><span class="sxs-lookup"><span data-stu-id="87056-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="87056-121">ДоСтавляется в единицу доступа (AU), отличную от единицы доступа к физической доставке (ПДАУ), например, системы ФАКСИМИЛЬной связи.</span><span class="sxs-lookup"><span data-stu-id="87056-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="87056-122">МАПИ_МХ_ДП_ПДАУ</span><span class="sxs-lookup"><span data-stu-id="87056-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="87056-123">ДоСтавляется на единицу доступа к физической доставке, например по почтовым перевозчикам.</span><span class="sxs-lookup"><span data-stu-id="87056-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="87056-124">МАПИ_МХ_ДП_ПДС_ПАТРОН</span><span class="sxs-lookup"><span data-stu-id="87056-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="87056-125">ДоСтавляется в физическую систему доставки патрон, например обычные почтовые почтовые ящики.</span><span class="sxs-lookup"><span data-stu-id="87056-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="87056-126">МАПИ_МХ_ДП_ПРИВАТЕ_УА</span><span class="sxs-lookup"><span data-stu-id="87056-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="87056-127">ДоСтавляется в частный агент пользователя (UA), например в клиентскую систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="87056-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="87056-128">МАПИ_МХ_ДП_ПУБЛИК_УА</span><span class="sxs-lookup"><span data-stu-id="87056-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="87056-129">ДоСтавляется общедоступному агенту пользователя или общедоступному поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="87056-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="87056-130">Значение по умолчанию — МАПИ_МХ_ДП_ПРИВАТЕ_УА, то есть, клиент MAPI.</span><span class="sxs-lookup"><span data-stu-id="87056-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="87056-131">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="87056-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="87056-132">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="87056-132">Header files</span></span>

<span data-ttu-id="87056-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="87056-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="87056-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="87056-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="87056-135">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="87056-135">Mapitags.h</span></span>
  
> <span data-ttu-id="87056-136">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="87056-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87056-137">См. также</span><span class="sxs-lookup"><span data-stu-id="87056-137">See also</span></span>



[<span data-ttu-id="87056-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="87056-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87056-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="87056-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87056-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="87056-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87056-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="87056-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

