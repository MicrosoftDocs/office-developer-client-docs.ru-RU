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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346356"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="68edb-103">Каноническое свойство PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="68edb-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="68edb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68edb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68edb-105">Указывает состояние прихода для сообщений, запрашивающих уведомления.</span><span class="sxs-lookup"><span data-stu-id="68edb-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68edb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="68edb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68edb-107">ПР_РЕПОРТ_ДИСПОСИТИОН, ПР_РЕПОРТ_ДИСПОСИТИОН_А, ПР_РЕПОРТ_ДИСПОСИТИОН_В</span><span class="sxs-lookup"><span data-stu-id="68edb-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="68edb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="68edb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68edb-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="68edb-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="68edb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="68edb-110">Data type:</span></span>  <br/> |<span data-ttu-id="68edb-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="68edb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="68edb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="68edb-112">Area:</span></span>  <br/> |<span data-ttu-id="68edb-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="68edb-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68edb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68edb-114">Remarks</span></span>

<span data-ttu-id="68edb-115">Поддерживаются следующие допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="68edb-115">The following are valid values:</span></span>
  
- <span data-ttu-id="68edb-116">удалять</span><span class="sxs-lookup"><span data-stu-id="68edb-116">"deleted"</span></span>
    
- <span data-ttu-id="68edb-117">обработать</span><span class="sxs-lookup"><span data-stu-id="68edb-117">"processed"</span></span>
    
- <span data-ttu-id="68edb-118">WLM</span><span class="sxs-lookup"><span data-stu-id="68edb-118">"dispatched"</span></span>
    
- <span data-ttu-id="68edb-119">отказал</span><span class="sxs-lookup"><span data-stu-id="68edb-119">"denied"</span></span>
    
- <span data-ttu-id="68edb-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="68edb-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="68edb-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="68edb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68edb-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="68edb-122">Protocol specifications</span></span>

<span data-ttu-id="68edb-123">[[MS — ОКСПРОПС]]</span><span class="sxs-lookup"><span data-stu-id="68edb-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="68edb-124">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="68edb-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68edb-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="68edb-125">Header files</span></span>

<span data-ttu-id="68edb-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="68edb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="68edb-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="68edb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="68edb-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="68edb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="68edb-129">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="68edb-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68edb-130">См. также</span><span class="sxs-lookup"><span data-stu-id="68edb-130">See also</span></span>



[<span data-ttu-id="68edb-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="68edb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68edb-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="68edb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68edb-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="68edb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68edb-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="68edb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

