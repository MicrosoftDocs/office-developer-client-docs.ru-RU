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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357724"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="b2f81-103">Каноническое свойство PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="b2f81-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="b2f81-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2f81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2f81-105">Содержит дату и время доставки исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2f81-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2f81-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b2f81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2f81-107">ПР_ДЕЛИВЕР_ТИМЕ</span><span class="sxs-lookup"><span data-stu-id="b2f81-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="b2f81-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b2f81-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2f81-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="b2f81-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="b2f81-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b2f81-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2f81-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b2f81-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b2f81-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b2f81-112">Area:</span></span>  <br/> |<span data-ttu-id="b2f81-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="b2f81-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2f81-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2f81-114">Remarks</span></span>

<span data-ttu-id="b2f81-115">Это свойство является свойством для каждого получателя в отчете о доставке, которое указывает время доставки исходного сообщения пользователю обмена сообщениями, для которого создается отчет о доставке.</span><span class="sxs-lookup"><span data-stu-id="b2f81-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b2f81-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b2f81-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b2f81-117">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b2f81-117">Header files</span></span>

<span data-ttu-id="b2f81-118">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b2f81-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2f81-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b2f81-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2f81-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b2f81-120">Mapitags.h</span></span>
  
> <span data-ttu-id="b2f81-121">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b2f81-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2f81-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b2f81-122">See also</span></span>



[<span data-ttu-id="b2f81-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="b2f81-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="b2f81-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b2f81-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2f81-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b2f81-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2f81-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b2f81-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2f81-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b2f81-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

