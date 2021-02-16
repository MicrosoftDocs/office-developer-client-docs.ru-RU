---
title: Каноническое свойство PidTagDeferredDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredDeliveryTime
api_type:
- HeaderDef
ms.assetid: 263ac923-692f-40d4-bdd5-116dc5c49766
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7197159fd55016454de3fa806fc30d0700ef5f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359929"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="c3f41-103">Каноническое свойство PidTagDeferredDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="c3f41-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="c3f41-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3f41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3f41-105">Содержит дату и время, когда отправитель сообщения хочет доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="c3f41-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3f41-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c3f41-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3f41-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="c3f41-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="c3f41-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c3f41-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3f41-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="c3f41-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="c3f41-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c3f41-110">Data type:</span></span>  <br/> |<span data-ttu-id="c3f41-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c3f41-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c3f41-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c3f41-112">Area:</span></span>  <br/> |<span data-ttu-id="c3f41-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="c3f41-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3f41-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3f41-114">Remarks</span></span>

<span data-ttu-id="c3f41-115">MAPI не выполняет отложенную доставку; это возможность для обработки отложенной доставки в рамках системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c3f41-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c3f41-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c3f41-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3f41-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c3f41-117">Protocol specifications</span></span>

<span data-ttu-id="c3f41-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3f41-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3f41-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c3f41-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c3f41-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3f41-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3f41-121">Указывает свойства и операции, которые разрешены для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c3f41-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3f41-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c3f41-122">Header files</span></span>

<span data-ttu-id="c3f41-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3f41-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3f41-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c3f41-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3f41-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c3f41-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c3f41-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c3f41-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3f41-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c3f41-127">See also</span></span>



[<span data-ttu-id="c3f41-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c3f41-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3f41-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c3f41-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3f41-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c3f41-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3f41-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c3f41-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

