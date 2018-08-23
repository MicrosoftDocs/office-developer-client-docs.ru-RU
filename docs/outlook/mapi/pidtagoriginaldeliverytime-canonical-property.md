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
ms.openlocfilehash: 0fee808a02262ef47bff0279c929824becc23912
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589401"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="eb3ff-103">Каноническое свойство PidTagOriginalDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="eb3ff-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="eb3ff-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb3ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb3ff-105">Содержит копию исходного сообщения дату и время доставки в потоке.</span><span class="sxs-lookup"><span data-stu-id="eb3ff-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb3ff-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="eb3ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb3ff-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="eb3ff-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="eb3ff-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="eb3ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb3ff-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="eb3ff-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="eb3ff-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="eb3ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb3ff-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="eb3ff-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="eb3ff-112">Область:</span><span class="sxs-lookup"><span data-stu-id="eb3ff-112">Area:</span></span>  <br/> |<span data-ttu-id="eb3ff-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="eb3ff-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb3ff-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="eb3ff-114">Remarks</span></span>

<span data-ttu-id="eb3ff-115">Это свойство копируются из исходного свойства **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) в последующих ответить или операции и в отчетах чтения и nonread.</span><span class="sxs-lookup"><span data-stu-id="eb3ff-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="eb3ff-116">Отчеты о доставке используйте свойство **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eb3ff-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb3ff-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eb3ff-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb3ff-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="eb3ff-118">Protocol specifications</span></span>

<span data-ttu-id="eb3ff-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb3ff-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb3ff-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="eb3ff-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eb3ff-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb3ff-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb3ff-122">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="eb3ff-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb3ff-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="eb3ff-123">Header files</span></span>

<span data-ttu-id="eb3ff-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb3ff-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb3ff-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="eb3ff-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb3ff-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eb3ff-126">Mapitags.h</span></span>
  
> <span data-ttu-id="eb3ff-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="eb3ff-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb3ff-128">См. также</span><span class="sxs-lookup"><span data-stu-id="eb3ff-128">See also</span></span>



[<span data-ttu-id="eb3ff-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb3ff-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb3ff-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb3ff-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb3ff-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="eb3ff-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb3ff-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="eb3ff-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

