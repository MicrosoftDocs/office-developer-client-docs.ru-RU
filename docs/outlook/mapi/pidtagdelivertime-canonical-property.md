---
title: Каноническое свойство PidTagDeliverTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435280"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="96214-103">Каноническое свойство PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="96214-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="96214-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96214-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96214-105">Содержит дату и время доставки исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="96214-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96214-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="96214-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96214-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="96214-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="96214-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="96214-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96214-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="96214-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="96214-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="96214-110">Data type:</span></span>  <br/> |<span data-ttu-id="96214-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="96214-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="96214-112">Область:</span><span class="sxs-lookup"><span data-stu-id="96214-112">Area:</span></span>  <br/> |<span data-ttu-id="96214-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="96214-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96214-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="96214-114">Remarks</span></span>

<span data-ttu-id="96214-115">Это свойство является свойством для каждого получателя в отчете о доставке, которое указывает время доставки исходного сообщения пользователю сообщения, для которого создается отчет о доставке.</span><span class="sxs-lookup"><span data-stu-id="96214-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="96214-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="96214-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="96214-117">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="96214-117">Header files</span></span>

<span data-ttu-id="96214-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96214-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="96214-119">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="96214-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="96214-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96214-120">Mapitags.h</span></span>
  
> <span data-ttu-id="96214-121">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="96214-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96214-122">См. также</span><span class="sxs-lookup"><span data-stu-id="96214-122">See also</span></span>



[<span data-ttu-id="96214-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="96214-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="96214-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96214-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96214-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96214-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96214-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="96214-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96214-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="96214-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

