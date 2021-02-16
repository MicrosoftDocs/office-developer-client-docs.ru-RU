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
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="ced56-103">Каноническое свойство PidTagOriginalDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="ced56-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="ced56-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced56-105">Содержит отображаемую информацию о любых получателях с незрячими копиями (BCC) исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="ced56-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ced56-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ced56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ced56-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="ced56-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="ced56-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ced56-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ced56-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="ced56-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="ced56-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ced56-110">Data type:</span></span>  <br/> |<span data-ttu-id="ced56-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ced56-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ced56-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ced56-112">Area:</span></span>  <br/> |<span data-ttu-id="ced56-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="ced56-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ced56-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ced56-114">Remarks</span></span>

<span data-ttu-id="ced56-115">Эти свойства содержат список, разделенный с зазнайки.</span><span class="sxs-lookup"><span data-stu-id="ced56-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="ced56-116">Они печатаются с помощью MAPI и копируется непосредственно из PR_DISPLAY_BCC **(** [PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)при составлении отчета о доставке или ненадежаности, а также чтения или непрочитанные отчеты.</span><span class="sxs-lookup"><span data-stu-id="ced56-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="ced56-117">Эти свойства могут присутствовать в других сообщениях в зависимости от их классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="ced56-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ced56-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ced56-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ced56-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ced56-119">Protocol specifications</span></span>

<span data-ttu-id="ced56-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ced56-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ced56-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="ced56-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ced56-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ced56-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ced56-123">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ced56-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ced56-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="ced56-124">Header files</span></span>

<span data-ttu-id="ced56-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ced56-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ced56-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ced56-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ced56-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ced56-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ced56-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ced56-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ced56-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ced56-129">See also</span></span>



[<span data-ttu-id="ced56-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ced56-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ced56-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ced56-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ced56-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ced56-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ced56-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ced56-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

