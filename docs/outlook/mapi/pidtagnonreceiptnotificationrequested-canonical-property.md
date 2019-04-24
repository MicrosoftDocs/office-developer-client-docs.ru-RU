---
title: Каноническое свойство PidTagNonReceiptNotificationRequested
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329311"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="b5f48-103">Каноническое свойство PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="b5f48-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="b5f48-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5f48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5f48-105">Содержит значение TRUE, если отправителю сообщения требуется уведомление о недоставке для указанного получателя.</span><span class="sxs-lookup"><span data-stu-id="b5f48-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5f48-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b5f48-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5f48-107">ПР_НОН_РЕЦЕИПТ_НОТИФИКАТИОН_РЕКУЕСТЕД</span><span class="sxs-lookup"><span data-stu-id="b5f48-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="b5f48-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b5f48-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5f48-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="b5f48-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="b5f48-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b5f48-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5f48-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b5f48-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b5f48-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b5f48-112">Area:</span></span>  <br/> |<span data-ttu-id="b5f48-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="b5f48-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5f48-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5f48-114">Remarks</span></span>

<span data-ttu-id="b5f48-115">Если это свойство содержит значение FALSE, а свойство **пр_реад_рецеипт_рекуестед** ([PIDTAGREADRECEIPTREQUESTED](pidtagreadreceiptrequested-canonical-property.md)) содержит значение true, то поставщик услуг может переопределить свойство **пр_нон_рецеипт_нотификатион_рекуестед** и создать объект отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="b5f48-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b5f48-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b5f48-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b5f48-117">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b5f48-117">Header files</span></span>

<span data-ttu-id="b5f48-118">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b5f48-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5f48-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b5f48-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5f48-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b5f48-120">Mapitags.h</span></span>
  
> <span data-ttu-id="b5f48-121">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="b5f48-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5f48-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b5f48-122">See also</span></span>



[<span data-ttu-id="b5f48-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b5f48-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5f48-124">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b5f48-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5f48-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b5f48-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5f48-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b5f48-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

