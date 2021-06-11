---
title: Каноническое свойство PidTagOriginalDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bbe277092b450a4254e02d00d2cf54e35ec6be44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355659"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="462dc-103">Каноническое свойство PidTagOriginalDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="462dc-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="462dc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="462dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="462dc-105">Содержит копию даты и времени доставки исходного сообщения в потоке.</span><span class="sxs-lookup"><span data-stu-id="462dc-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="462dc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="462dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="462dc-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="462dc-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="462dc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="462dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="462dc-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="462dc-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="462dc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="462dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="462dc-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="462dc-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="462dc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="462dc-112">Area:</span></span>  <br/> |<span data-ttu-id="462dc-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="462dc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="462dc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="462dc-114">Remarks</span></span>

<span data-ttu-id="462dc-115">Это свойство копируется из исходного **свойства PR_MESSAGE_DELIVERY_TIME** [(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в последующих операциях ответа или переадпортации и используется в отчетах чтения и непрочитания.</span><span class="sxs-lookup"><span data-stu-id="462dc-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="462dc-116">Отчеты о доставке **используют свойство PR_DELIVER_TIME** [(PidTagDeliverTime).](pidtagdelivertime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="462dc-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="462dc-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="462dc-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="462dc-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="462dc-118">Protocol specifications</span></span>

<span data-ttu-id="462dc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="462dc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="462dc-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="462dc-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="462dc-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="462dc-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="462dc-122">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="462dc-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="462dc-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="462dc-123">Header files</span></span>

<span data-ttu-id="462dc-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="462dc-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="462dc-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="462dc-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="462dc-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="462dc-126">Mapitags.h</span></span>
  
> <span data-ttu-id="462dc-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="462dc-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="462dc-128">См. также</span><span class="sxs-lookup"><span data-stu-id="462dc-128">See also</span></span>



[<span data-ttu-id="462dc-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="462dc-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="462dc-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="462dc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="462dc-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="462dc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="462dc-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="462dc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

