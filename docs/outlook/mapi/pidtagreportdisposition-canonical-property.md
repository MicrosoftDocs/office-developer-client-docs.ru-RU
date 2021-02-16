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
ms.openlocfilehash: dae31959cddad7ad61ea32f2372ea34bdbff658e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423708"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="d6e76-103">Каноническое свойство PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="d6e76-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="d6e76-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6e76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6e76-105">Указывает состояние квитанции для сообщений, запрашивает квитанции.</span><span class="sxs-lookup"><span data-stu-id="d6e76-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6e76-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d6e76-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6e76-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="d6e76-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="d6e76-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d6e76-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6e76-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="d6e76-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="d6e76-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d6e76-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6e76-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6e76-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d6e76-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d6e76-112">Area:</span></span>  <br/> |<span data-ttu-id="d6e76-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="d6e76-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6e76-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6e76-114">Remarks</span></span>

<span data-ttu-id="d6e76-115">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d6e76-115">The following are valid values:</span></span>
  
- <span data-ttu-id="d6e76-116">"deleted"</span><span class="sxs-lookup"><span data-stu-id="d6e76-116">"deleted"</span></span>
    
- <span data-ttu-id="d6e76-117">"processed"</span><span class="sxs-lookup"><span data-stu-id="d6e76-117">"processed"</span></span>
    
- <span data-ttu-id="d6e76-118">"dispatched"</span><span class="sxs-lookup"><span data-stu-id="d6e76-118">"dispatched"</span></span>
    
- <span data-ttu-id="d6e76-119">"denied"</span><span class="sxs-lookup"><span data-stu-id="d6e76-119">"denied"</span></span>
    
- <span data-ttu-id="d6e76-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="d6e76-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d6e76-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d6e76-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6e76-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d6e76-122">Protocol specifications</span></span>

<span data-ttu-id="d6e76-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="d6e76-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="d6e76-124">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="d6e76-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6e76-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="d6e76-125">Header files</span></span>

<span data-ttu-id="d6e76-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6e76-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6e76-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d6e76-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6e76-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6e76-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d6e76-129">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="d6e76-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6e76-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d6e76-130">See also</span></span>



[<span data-ttu-id="d6e76-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d6e76-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6e76-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d6e76-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6e76-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d6e76-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6e76-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d6e76-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

