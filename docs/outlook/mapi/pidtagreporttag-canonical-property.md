---
title: Каноническое свойство PidTagReportTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 581bf372-8705-4617-aaa4-a1d761eb9b58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c832842568ea3d64d50b56d226b66d551402ba6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811729"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="e966e-103">Каноническое свойство PidTagReportTag</span><span class="sxs-lookup"><span data-stu-id="e966e-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="e966e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e966e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e966e-105">Содержит значение двоичные тег, системы обмена сообщениями следует скопировать любой отчет, созданный для сообщения.</span><span class="sxs-lookup"><span data-stu-id="e966e-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e966e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e966e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e966e-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="e966e-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="e966e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e966e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e966e-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="e966e-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="e966e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e966e-110">Data type:</span></span>  <br/> |<span data-ttu-id="e966e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e966e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e966e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e966e-112">Area:</span></span>  <br/> |<span data-ttu-id="e966e-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="e966e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e966e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e966e-114">Remarks</span></span>

<span data-ttu-id="e966e-115">Это свойство, как свойство **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) используется для сопоставления с отчетом с исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e966e-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e966e-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e966e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e966e-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e966e-117">Protocol specifications</span></span>

<span data-ttu-id="e966e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e966e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e966e-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e966e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e966e-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e966e-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e966e-121">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e966e-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e966e-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e966e-122">Header files</span></span>

<span data-ttu-id="e966e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e966e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e966e-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e966e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e966e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e966e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e966e-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e966e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e966e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e966e-127">See also</span></span>



[<span data-ttu-id="e966e-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e966e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e966e-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e966e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e966e-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e966e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e966e-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e966e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

