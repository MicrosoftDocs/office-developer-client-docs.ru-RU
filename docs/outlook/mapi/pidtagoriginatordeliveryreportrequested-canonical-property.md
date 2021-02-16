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
ms.openlocfilehash: a92ee13e571032c050f69677d9daba8dad7aea3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356303"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="968eb-103">Каноническое свойство PidTagOriginatorDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="968eb-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="968eb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="968eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="968eb-105">Содержит значение TRUE, если отправитель сообщения запрашивает отчет о доставке определенного получателя из системы обмена сообщениями, прежде чем сообщение будет помещено в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="968eb-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="968eb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="968eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="968eb-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="968eb-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="968eb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="968eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="968eb-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="968eb-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="968eb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="968eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="968eb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="968eb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="968eb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="968eb-112">Area:</span></span>  <br/> |<span data-ttu-id="968eb-113">MIME</span><span class="sxs-lookup"><span data-stu-id="968eb-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="968eb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="968eb-114">Remarks</span></span>

<span data-ttu-id="968eb-115">Это свойство используется для управления системой обмена сообщениями при обработке доставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="968eb-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="968eb-116">В этом случае в сообщении  также должно быть PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED[(PidTagOriginatorNonDeliveryReportRequested)](pidtagoriginatornondeliveryreportrequested-canonical-property.md)со свойством FALSE.</span><span class="sxs-lookup"><span data-stu-id="968eb-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="968eb-117">Установка свойства **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** для сообщения — это способ запроса отчетов о состоянии доставки для всех получателей.</span><span class="sxs-lookup"><span data-stu-id="968eb-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="968eb-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="968eb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="968eb-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="968eb-119">Protocol specifications</span></span>

<span data-ttu-id="968eb-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="968eb-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="968eb-121">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="968eb-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="968eb-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="968eb-122">Header files</span></span>

<span data-ttu-id="968eb-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="968eb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="968eb-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="968eb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="968eb-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="968eb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="968eb-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="968eb-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="968eb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="968eb-127">See also</span></span>



[<span data-ttu-id="968eb-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="968eb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="968eb-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="968eb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="968eb-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="968eb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="968eb-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="968eb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

