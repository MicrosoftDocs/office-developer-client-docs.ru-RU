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
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811398"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="f201a-103">Каноническое свойство PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="f201a-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="f201a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f201a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f201a-105">Содержит значение TRUE, если отправитель сообщения запрашивает уведомления без уведомления для указанного получателя.</span><span class="sxs-lookup"><span data-stu-id="f201a-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f201a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f201a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f201a-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="f201a-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="f201a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f201a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f201a-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="f201a-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="f201a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f201a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f201a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f201a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f201a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f201a-112">Area:</span></span>  <br/> |<span data-ttu-id="f201a-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="f201a-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f201a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f201a-114">Remarks</span></span>

<span data-ttu-id="f201a-115">Если это свойство содержит значение FALSE, а свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) значение TRUE, поставщик услуг можно переопределить свойство **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** и создать отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="f201a-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f201a-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f201a-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f201a-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f201a-117">Header files</span></span>

<span data-ttu-id="f201a-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f201a-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="f201a-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f201a-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="f201a-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f201a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="f201a-121">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="f201a-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f201a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f201a-122">See also</span></span>



[<span data-ttu-id="f201a-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f201a-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f201a-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f201a-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f201a-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f201a-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f201a-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f201a-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

