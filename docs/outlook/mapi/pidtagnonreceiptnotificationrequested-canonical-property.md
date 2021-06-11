---
title: PidTagNonReceiptNotificationRequested Canonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419753"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="4fd09-103">PidTagNonReceiptNotificationRequested Canonical Property</span><span class="sxs-lookup"><span data-stu-id="4fd09-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="4fd09-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fd09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fd09-105">Содержит TRUE, если отправителю сообщения нужно уведомление о неисписке для указанного получателя.</span><span class="sxs-lookup"><span data-stu-id="4fd09-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4fd09-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4fd09-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4fd09-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="4fd09-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="4fd09-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4fd09-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4fd09-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="4fd09-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="4fd09-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4fd09-110">Data type:</span></span>  <br/> |<span data-ttu-id="4fd09-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4fd09-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4fd09-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4fd09-112">Area:</span></span>  <br/> |<span data-ttu-id="4fd09-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="4fd09-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fd09-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4fd09-114">Remarks</span></span>

<span data-ttu-id="4fd09-115">Если это свойство содержит FALSE **PR_READ_RECEIPT_REQUESTED** [(Свойство PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)содержит TRUE, поставщик службы может переопрещать свойство PR_NON_RECEIPT_NOTIFICATION_REQUESTED и создать отчет о невывозе. </span><span class="sxs-lookup"><span data-stu-id="4fd09-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4fd09-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4fd09-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4fd09-117">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="4fd09-117">Header files</span></span>

<span data-ttu-id="4fd09-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4fd09-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="4fd09-119">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4fd09-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="4fd09-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4fd09-120">Mapitags.h</span></span>
  
> <span data-ttu-id="4fd09-121">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="4fd09-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4fd09-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4fd09-122">See also</span></span>



[<span data-ttu-id="4fd09-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4fd09-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4fd09-124">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4fd09-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4fd09-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4fd09-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4fd09-126">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="4fd09-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

