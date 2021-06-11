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
ms.openlocfilehash: 3fbd7205901616695bcdcd012601afd252ac05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355645"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="09700-103">Каноническое свойство PidTagOriginalDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="09700-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="09700-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09700-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09700-105">Содержит отображаемую информацию о любых получателях исходного сообщения с слепой копией углерода (BCC).</span><span class="sxs-lookup"><span data-stu-id="09700-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09700-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="09700-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="09700-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="09700-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="09700-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="09700-108">Identifier:</span></span>  <br/> |<span data-ttu-id="09700-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="09700-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="09700-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="09700-110">Data type:</span></span>  <br/> |<span data-ttu-id="09700-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09700-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="09700-112">Область:</span><span class="sxs-lookup"><span data-stu-id="09700-112">Area:</span></span>  <br/> |<span data-ttu-id="09700-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="09700-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09700-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="09700-114">Remarks</span></span>

<span data-ttu-id="09700-115">Эти свойства содержат список, разделенный зайколонами.</span><span class="sxs-lookup"><span data-stu-id="09700-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="09700-116">Они предоставлены MAPI и копированы непосредственно из **PR_DISPLAY_BCC** [(PidTagDisplayBcc),](pidtagdisplaybcc-canonical-property.md)когда создается отчет о доставке или неделивности или отчет о прочтениях.</span><span class="sxs-lookup"><span data-stu-id="09700-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="09700-117">Эти свойства могут присутствовать на других сообщениях, определенных классами сообщений.</span><span class="sxs-lookup"><span data-stu-id="09700-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="09700-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="09700-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="09700-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="09700-119">Protocol specifications</span></span>

<span data-ttu-id="09700-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09700-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09700-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="09700-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="09700-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09700-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09700-123">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="09700-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="09700-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="09700-124">Header files</span></span>

<span data-ttu-id="09700-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09700-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="09700-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="09700-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="09700-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="09700-127">Mapitags.h</span></span>
  
> <span data-ttu-id="09700-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="09700-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="09700-129">См. также</span><span class="sxs-lookup"><span data-stu-id="09700-129">See also</span></span>



[<span data-ttu-id="09700-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="09700-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="09700-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="09700-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="09700-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="09700-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="09700-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="09700-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

