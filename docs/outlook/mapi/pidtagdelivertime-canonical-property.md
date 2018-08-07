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
ms.openlocfilehash: 40839e34a61b5e5fdd3d7b69d8c553d7e469cd22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811052"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="e7f26-103">Каноническое свойство PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="e7f26-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="e7f26-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7f26-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7f26-105">Содержит дату и время, когда исходное сообщение было доставлено.</span><span class="sxs-lookup"><span data-stu-id="e7f26-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7f26-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e7f26-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7f26-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="e7f26-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="e7f26-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e7f26-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7f26-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="e7f26-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="e7f26-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e7f26-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7f26-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e7f26-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e7f26-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e7f26-112">Area:</span></span>  <br/> |<span data-ttu-id="e7f26-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="e7f26-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7f26-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7f26-114">Remarks</span></span>

<span data-ttu-id="e7f26-115">Это свойство является свойством каждого получателя на отчетов о доставке, которое указывает время, когда исходное сообщение было доставлено обмена сообщениями пользователя, для которого создается отчет о доставке.</span><span class="sxs-lookup"><span data-stu-id="e7f26-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7f26-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e7f26-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e7f26-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e7f26-117">Header files</span></span>

<span data-ttu-id="e7f26-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7f26-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7f26-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e7f26-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7f26-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7f26-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e7f26-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e7f26-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7f26-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e7f26-122">See also</span></span>



[<span data-ttu-id="e7f26-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="e7f26-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="e7f26-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7f26-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7f26-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7f26-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7f26-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e7f26-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7f26-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e7f26-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

