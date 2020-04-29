---
title: Каноническое свойство PidTagReadReceiptRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0e49b73c777988ad3559a442af920af3d8f4bdbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356471"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="69a03-103">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="69a03-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="69a03-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69a03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69a03-105">Содержит значение TRUE, если отправителю требуется, чтобы система обмена сообщениями создавала отчет о прочтении, когда получатель прочитал сообщение.</span><span class="sxs-lookup"><span data-stu-id="69a03-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69a03-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="69a03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69a03-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="69a03-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="69a03-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="69a03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69a03-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="69a03-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="69a03-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="69a03-110">Data type:</span></span>  <br/> |<span data-ttu-id="69a03-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="69a03-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="69a03-112">Область:</span><span class="sxs-lookup"><span data-stu-id="69a03-112">Area:</span></span>  <br/> |<span data-ttu-id="69a03-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="69a03-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69a03-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="69a03-114">Remarks</span></span>

<span data-ttu-id="69a03-115">Для этого свойства должно быть задано значение TRUE, чтобы проверить значения в свойствах **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) и **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="69a03-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="69a03-116">Если сообщение с набором **PR_READ_RECEIPT_REQUESTED** удаляется или истечет до тех пор, пока система обмена сообщениями не сможет создать отчет о прочтении, создается отчет о непрочтении.</span><span class="sxs-lookup"><span data-stu-id="69a03-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="69a03-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="69a03-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69a03-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="69a03-118">Protocol specifications</span></span>

<span data-ttu-id="69a03-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69a03-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69a03-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="69a03-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69a03-121">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69a03-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69a03-122">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="69a03-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69a03-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="69a03-123">Header files</span></span>

<span data-ttu-id="69a03-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="69a03-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="69a03-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="69a03-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="69a03-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="69a03-126">Mapitags.h</span></span>
  
> <span data-ttu-id="69a03-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="69a03-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69a03-128">См. также</span><span class="sxs-lookup"><span data-stu-id="69a03-128">See also</span></span>



[<span data-ttu-id="69a03-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69a03-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69a03-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="69a03-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69a03-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="69a03-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69a03-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="69a03-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

