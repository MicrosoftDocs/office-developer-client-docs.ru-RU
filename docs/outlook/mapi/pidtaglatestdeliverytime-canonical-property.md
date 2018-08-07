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
ms.openlocfilehash: 0cf25dc5a1182d019ea183f2c0714925f220aeb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811310"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="95da3-103">Каноническое свойство PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="95da3-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="95da3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95da3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95da3-105">Содержит последние дата и время, когда сообщение передачи (агента) необходимо доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="95da3-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95da3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="95da3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95da3-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="95da3-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="95da3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="95da3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95da3-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="95da3-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="95da3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="95da3-110">Data type:</span></span>  <br/> |<span data-ttu-id="95da3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="95da3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="95da3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="95da3-112">Area:</span></span>  <br/> |<span data-ttu-id="95da3-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="95da3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95da3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="95da3-114">Remarks</span></span>

<span data-ttu-id="95da3-115">Если агента передачи сообщений не удается доставить сообщение, время, когда это свойство определяет, отменяет сообщение без доставки.</span><span class="sxs-lookup"><span data-stu-id="95da3-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="95da3-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="95da3-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="95da3-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="95da3-117">Header files</span></span>

<span data-ttu-id="95da3-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95da3-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="95da3-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="95da3-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="95da3-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="95da3-120">Mapitags.h</span></span>
  
> <span data-ttu-id="95da3-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="95da3-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95da3-122">См. также</span><span class="sxs-lookup"><span data-stu-id="95da3-122">See also</span></span>



[<span data-ttu-id="95da3-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95da3-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95da3-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95da3-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95da3-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="95da3-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95da3-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="95da3-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

