---
title: Каноническое свойство PidTagReportDisposition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1e84308f3a9f9457c5db23c1ad9d42d6e856519e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583633"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="bcf10-103">Каноническое свойство PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="bcf10-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="bcf10-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcf10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcf10-105">Указывает состояние уведомления для сообщений, запрашивающих поступлений.</span><span class="sxs-lookup"><span data-stu-id="bcf10-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcf10-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bcf10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcf10-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="bcf10-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="bcf10-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bcf10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcf10-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="bcf10-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="bcf10-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bcf10-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcf10-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bcf10-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bcf10-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bcf10-112">Area:</span></span>  <br/> |<span data-ttu-id="bcf10-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf10-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcf10-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bcf10-114">Remarks</span></span>

<span data-ttu-id="bcf10-115">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="bcf10-115">The following are valid values:</span></span>
  
- <span data-ttu-id="bcf10-116">«удалить»</span><span class="sxs-lookup"><span data-stu-id="bcf10-116">"deleted"</span></span>
    
- <span data-ttu-id="bcf10-117">«обработки»</span><span class="sxs-lookup"><span data-stu-id="bcf10-117">"processed"</span></span>
    
- <span data-ttu-id="bcf10-118">«Отправлено»</span><span class="sxs-lookup"><span data-stu-id="bcf10-118">"dispatched"</span></span>
    
- <span data-ttu-id="bcf10-119">«Отказано»</span><span class="sxs-lookup"><span data-stu-id="bcf10-119">"denied"</span></span>
    
- <span data-ttu-id="bcf10-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="bcf10-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="bcf10-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bcf10-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcf10-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bcf10-122">Protocol specifications</span></span>

<span data-ttu-id="bcf10-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="bcf10-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="bcf10-124">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bcf10-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcf10-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bcf10-125">Header files</span></span>

<span data-ttu-id="bcf10-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcf10-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcf10-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bcf10-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcf10-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bcf10-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bcf10-129">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="bcf10-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcf10-130">См. также</span><span class="sxs-lookup"><span data-stu-id="bcf10-130">See also</span></span>



[<span data-ttu-id="bcf10-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf10-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcf10-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf10-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcf10-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf10-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcf10-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bcf10-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

