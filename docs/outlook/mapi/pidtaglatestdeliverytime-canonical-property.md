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
ms.openlocfilehash: 77ca51ae5a0e7e1d5a9be8f4ca05a1187fe71694
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407790"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="e9dec-103">Каноническое свойство PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="e9dec-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="e9dec-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9dec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9dec-105">Содержит последние дата и время, когда агент передачи сообщений (MTA) должен доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="e9dec-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9dec-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e9dec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9dec-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="e9dec-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="e9dec-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e9dec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9dec-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="e9dec-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="e9dec-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e9dec-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9dec-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e9dec-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e9dec-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e9dec-112">Area:</span></span>  <br/> |<span data-ttu-id="e9dec-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="e9dec-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9dec-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9dec-114">Remarks</span></span>

<span data-ttu-id="e9dec-115">Если MTA не может доставить сообщение по времени, указанному этим свойством, оно отменяет сообщение без доставки.</span><span class="sxs-lookup"><span data-stu-id="e9dec-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9dec-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e9dec-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e9dec-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e9dec-117">Header files</span></span>

<span data-ttu-id="e9dec-118">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e9dec-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9dec-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e9dec-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9dec-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="e9dec-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e9dec-121">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="e9dec-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9dec-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e9dec-122">See also</span></span>



[<span data-ttu-id="e9dec-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e9dec-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9dec-124">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e9dec-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9dec-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e9dec-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9dec-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e9dec-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

