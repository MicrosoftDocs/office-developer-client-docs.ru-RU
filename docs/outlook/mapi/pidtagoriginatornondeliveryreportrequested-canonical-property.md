---
title: Каноническое свойство PidTagOriginatorNonDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 841d2b14efc781d89727b0c7ed677f527526a4ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811488"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="c25be-103">Каноническое свойство PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="c25be-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="c25be-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c25be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c25be-105">Содержит значение TRUE, если отправитель сообщения запрашивает о недоставке для определенного получателя.</span><span class="sxs-lookup"><span data-stu-id="c25be-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c25be-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c25be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c25be-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="c25be-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="c25be-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c25be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c25be-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="c25be-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="c25be-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c25be-110">Data type:</span></span>  <br/> |<span data-ttu-id="c25be-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c25be-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c25be-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c25be-112">Area:</span></span>  <br/> |<span data-ttu-id="c25be-113">MIME</span><span class="sxs-lookup"><span data-stu-id="c25be-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c25be-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c25be-114">Remarks</span></span>

<span data-ttu-id="c25be-115">Это свойство используется для направления системе обмена сообщениями в обработке недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c25be-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="c25be-116">В этом случае сообщение необходимо также указать свойство **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="c25be-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c25be-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c25be-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c25be-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c25be-118">Protocol specifications</span></span>

<span data-ttu-id="c25be-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c25be-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c25be-120">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c25be-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c25be-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c25be-121">Header files</span></span>

<span data-ttu-id="c25be-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c25be-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="c25be-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c25be-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="c25be-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c25be-124">Mapitags.h</span></span>
  
> <span data-ttu-id="c25be-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c25be-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c25be-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c25be-126">See also</span></span>



[<span data-ttu-id="c25be-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c25be-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c25be-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c25be-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c25be-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c25be-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c25be-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c25be-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

