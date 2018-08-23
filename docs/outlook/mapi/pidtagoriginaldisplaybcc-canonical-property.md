---
title: Каноническое свойство PidTagOriginalDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayBcc
api_type:
- COM
ms.assetid: 7bf66f0c-3095-4b4a-a32e-db278e1adc5a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 20f70f9e7bfecd955eb6bfb1c05c6b2010cb52cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563410"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="65db1-103">Каноническое свойство PidTagOriginalDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="65db1-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="65db1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65db1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65db1-105">Содержит отображаемые имена получателей скрытой копии (СК) исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="65db1-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65db1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="65db1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65db1-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="65db1-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="65db1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="65db1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="65db1-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="65db1-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="65db1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="65db1-110">Data type:</span></span>  <br/> |<span data-ttu-id="65db1-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="65db1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="65db1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="65db1-112">Area:</span></span>  <br/> |<span data-ttu-id="65db1-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="65db1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65db1-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="65db1-114">Remarks</span></span>

<span data-ttu-id="65db1-115">Эти свойства содержат список разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="65db1-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="65db1-116">Они поставляется с MAPI и при доставке или уведомление о недоставке или чтение или nonread отчета создается копируются непосредственно из **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="65db1-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="65db1-117">Эти свойства может присутствовать в другие сообщения в соответствии с их классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="65db1-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="65db1-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="65db1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65db1-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="65db1-119">Protocol specifications</span></span>

<span data-ttu-id="65db1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65db1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65db1-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="65db1-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="65db1-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65db1-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65db1-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="65db1-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65db1-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="65db1-124">Header files</span></span>

<span data-ttu-id="65db1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65db1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="65db1-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="65db1-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="65db1-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="65db1-127">Mapitags.h</span></span>
  
> <span data-ttu-id="65db1-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="65db1-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65db1-129">См. также</span><span class="sxs-lookup"><span data-stu-id="65db1-129">See also</span></span>



[<span data-ttu-id="65db1-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="65db1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65db1-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="65db1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65db1-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="65db1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65db1-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="65db1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

