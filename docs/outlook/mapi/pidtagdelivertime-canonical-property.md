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
ms.openlocfilehash: 198e388f5cfb6ab0431e7b7a78b9a0be3d103597
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582121"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="714e0-103">Каноническое свойство PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="714e0-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="714e0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="714e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="714e0-105">Содержит дату и время, когда исходное сообщение было доставлено.</span><span class="sxs-lookup"><span data-stu-id="714e0-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="714e0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="714e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="714e0-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="714e0-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="714e0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="714e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="714e0-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="714e0-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="714e0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="714e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="714e0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="714e0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="714e0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="714e0-112">Area:</span></span>  <br/> |<span data-ttu-id="714e0-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="714e0-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="714e0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="714e0-114">Remarks</span></span>

<span data-ttu-id="714e0-115">Это свойство является свойством каждого получателя на отчетов о доставке, которое указывает время, когда исходное сообщение было доставлено обмена сообщениями пользователя, для которого создается отчет о доставке.</span><span class="sxs-lookup"><span data-stu-id="714e0-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="714e0-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="714e0-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="714e0-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="714e0-117">Header files</span></span>

<span data-ttu-id="714e0-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="714e0-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="714e0-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="714e0-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="714e0-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="714e0-120">Mapitags.h</span></span>
  
> <span data-ttu-id="714e0-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="714e0-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="714e0-122">См. также</span><span class="sxs-lookup"><span data-stu-id="714e0-122">See also</span></span>



[<span data-ttu-id="714e0-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="714e0-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="714e0-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="714e0-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="714e0-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="714e0-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="714e0-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="714e0-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="714e0-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="714e0-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

