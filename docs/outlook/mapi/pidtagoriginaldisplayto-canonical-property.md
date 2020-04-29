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
ms.openlocfilehash: 5a2f60051e5cb0717926a5c3e2f878a49919b04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342703"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="1666a-103">Каноническое свойство PidTagOriginalDisplayTo</span><span class="sxs-lookup"><span data-stu-id="1666a-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="1666a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1666a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1666a-105">Содержит отображаемые имена основных получателей исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="1666a-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1666a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1666a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1666a-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="1666a-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="1666a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1666a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1666a-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="1666a-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="1666a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1666a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1666a-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1666a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1666a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1666a-112">Area:</span></span>  <br/> |<span data-ttu-id="1666a-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="1666a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1666a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1666a-114">Remarks</span></span>

<span data-ttu-id="1666a-115">Эти свойства содержат список ASCII, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="1666a-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="1666a-116">Он предоставляется MAPI и копируется непосредственно из **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), когда создается отчет о доставке или недоставке или отчет о прочтении или непрочтении.</span><span class="sxs-lookup"><span data-stu-id="1666a-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="1666a-117">Это свойство может присутствовать в других сообщениях, определенных их классами сообщений.</span><span class="sxs-lookup"><span data-stu-id="1666a-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1666a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1666a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1666a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1666a-119">Protocol specifications</span></span>

<span data-ttu-id="1666a-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1666a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1666a-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1666a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1666a-122">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1666a-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1666a-123">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1666a-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1666a-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1666a-124">Header files</span></span>

<span data-ttu-id="1666a-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="1666a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1666a-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1666a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1666a-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="1666a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1666a-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="1666a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1666a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="1666a-129">See also</span></span>



[<span data-ttu-id="1666a-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1666a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1666a-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="1666a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1666a-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1666a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1666a-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1666a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

