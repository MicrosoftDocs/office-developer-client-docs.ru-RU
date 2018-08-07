---
title: Каноническое свойство PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 07cea7606654bf32c1fe70e49254afeeb04f0e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811503"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="3b2ff-103">Каноническое свойство PidTagOriginatorDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="3b2ff-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="3b2ff-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b2ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b2ff-105">Содержит значение TRUE, если отправитель сообщения запрашивает отчетов о доставке для определенного получателя из систем обмена сообщениями перед сообщение помещается в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b2ff-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b2ff-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3b2ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b2ff-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="3b2ff-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="3b2ff-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3b2ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b2ff-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="3b2ff-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="3b2ff-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3b2ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="3b2ff-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3b2ff-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3b2ff-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3b2ff-112">Area:</span></span>  <br/> |<span data-ttu-id="3b2ff-113">MIME</span><span class="sxs-lookup"><span data-stu-id="3b2ff-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b2ff-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b2ff-114">Remarks</span></span>

<span data-ttu-id="3b2ff-115">Это свойство используется для направления в обработке сообщений, доставленных систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3b2ff-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="3b2ff-116">В этом случае сообщение необходимо также указать свойство **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="3b2ff-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="3b2ff-117">Установка свойства **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** на сообщение — это способ запрос отчетов о состоянии доставки для всех получателей.</span><span class="sxs-lookup"><span data-stu-id="3b2ff-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3b2ff-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3b2ff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b2ff-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3b2ff-119">Protocol specifications</span></span>

<span data-ttu-id="3b2ff-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b2ff-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b2ff-121">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3b2ff-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b2ff-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3b2ff-122">Header files</span></span>

<span data-ttu-id="3b2ff-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b2ff-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b2ff-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3b2ff-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b2ff-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3b2ff-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3b2ff-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3b2ff-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b2ff-127">См. также</span><span class="sxs-lookup"><span data-stu-id="3b2ff-127">See also</span></span>



[<span data-ttu-id="3b2ff-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3b2ff-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b2ff-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3b2ff-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b2ff-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3b2ff-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b2ff-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3b2ff-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

