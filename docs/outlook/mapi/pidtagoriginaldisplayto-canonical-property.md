---
title: Каноническое свойство PidTagOriginalDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5adeec9a8f7092a2a32008a189918892ca50a952
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589198"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="d3017-103">Каноническое свойство PidTagOriginalDisplayTo</span><span class="sxs-lookup"><span data-stu-id="d3017-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="d3017-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3017-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3017-105">Содержит отображаемые имена основной (получателям) исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="d3017-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3017-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d3017-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3017-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="d3017-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="d3017-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d3017-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d3017-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="d3017-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="d3017-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d3017-110">Data type:</span></span>  <br/> |<span data-ttu-id="d3017-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d3017-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d3017-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d3017-112">Area:</span></span>  <br/> |<span data-ttu-id="d3017-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="d3017-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3017-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d3017-114">Remarks</span></span>

<span data-ttu-id="d3017-115">Эти свойства содержат список ASCII, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="d3017-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="d3017-116">Он поставляется с MAPI и копирования непосредственно из **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) при доставке или создается отчет о недоставке или чтение или nonread отчета.</span><span class="sxs-lookup"><span data-stu-id="d3017-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="d3017-117">Это свойство может присутствовать в другие сообщения в соответствии с их классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="d3017-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d3017-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d3017-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3017-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d3017-119">Protocol specifications</span></span>

<span data-ttu-id="d3017-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3017-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3017-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d3017-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d3017-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3017-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3017-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d3017-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3017-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d3017-124">Header files</span></span>

<span data-ttu-id="d3017-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3017-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3017-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d3017-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d3017-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d3017-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d3017-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d3017-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3017-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d3017-129">See also</span></span>



[<span data-ttu-id="d3017-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d3017-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3017-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d3017-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3017-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d3017-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3017-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d3017-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

