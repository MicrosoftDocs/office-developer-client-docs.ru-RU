---
title: Каноническое свойство PidTagReportTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 298c53e537819f800a3acc5cf07c01a7b9f978ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330151"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="18341-103">Каноническое свойство PidTagReportTime</span><span class="sxs-lookup"><span data-stu-id="18341-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="18341-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18341-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18341-105">Содержит дату и время создания отчета системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="18341-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18341-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="18341-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18341-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="18341-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="18341-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="18341-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18341-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="18341-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="18341-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="18341-110">Data type:</span></span>  <br/> |<span data-ttu-id="18341-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="18341-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="18341-112">Область:</span><span class="sxs-lookup"><span data-stu-id="18341-112">Area:</span></span>  <br/> |<span data-ttu-id="18341-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="18341-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18341-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="18341-114">Remarks</span></span>

<span data-ttu-id="18341-115">Это свойство представляет свойство для каждого получателя в отчетах о доставке и недоставке и свойство для каждого сообщения в отчетах о чтении и непрочтении.</span><span class="sxs-lookup"><span data-stu-id="18341-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="18341-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="18341-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18341-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="18341-117">Protocol specifications</span></span>

<span data-ttu-id="18341-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18341-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18341-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="18341-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18341-120">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18341-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18341-121">Задает свойства и операции, допустимые для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="18341-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="18341-122">[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18341-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18341-123">Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="18341-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18341-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="18341-124">Header files</span></span>

<span data-ttu-id="18341-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="18341-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="18341-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="18341-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="18341-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="18341-127">Mapitags.h</span></span>
  
> <span data-ttu-id="18341-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="18341-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18341-129">См. также</span><span class="sxs-lookup"><span data-stu-id="18341-129">See also</span></span>



[<span data-ttu-id="18341-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="18341-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18341-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="18341-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18341-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="18341-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18341-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="18341-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

