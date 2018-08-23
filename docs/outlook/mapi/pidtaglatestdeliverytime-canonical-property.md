---
title: Каноническое свойство PidTagLatestDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3640ec4471b72dea81d56cc2c462ef145095480f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590927"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="1d21e-103">Каноническое свойство PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="1d21e-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="1d21e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d21e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d21e-105">Содержит последние дата и время, когда сообщение передачи (агента) необходимо доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="1d21e-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d21e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1d21e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d21e-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="1d21e-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="1d21e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1d21e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1d21e-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="1d21e-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="1d21e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1d21e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1d21e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1d21e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1d21e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1d21e-112">Area:</span></span>  <br/> |<span data-ttu-id="1d21e-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="1d21e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d21e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d21e-114">Remarks</span></span>

<span data-ttu-id="1d21e-115">Если агента передачи сообщений не удается доставить сообщение, время, когда это свойство определяет, отменяет сообщение без доставки.</span><span class="sxs-lookup"><span data-stu-id="1d21e-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1d21e-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1d21e-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1d21e-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1d21e-117">Header files</span></span>

<span data-ttu-id="1d21e-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d21e-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d21e-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1d21e-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="1d21e-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1d21e-120">Mapitags.h</span></span>
  
> <span data-ttu-id="1d21e-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1d21e-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d21e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="1d21e-122">See also</span></span>



[<span data-ttu-id="1d21e-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1d21e-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d21e-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1d21e-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d21e-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1d21e-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d21e-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1d21e-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

