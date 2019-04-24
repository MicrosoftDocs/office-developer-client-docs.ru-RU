---
title: Каноническое свойство PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359047"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="a9ef2-103">Каноническое свойство PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="a9ef2-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="a9ef2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9ef2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9ef2-105">Содержит версию текста сообщения на языке гипертекстовой разМетки (HTML).</span><span class="sxs-lookup"><span data-stu-id="a9ef2-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9ef2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a9ef2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9ef2-107">ПР_БОДИ_ХТМЛ, ПР_БОДИ_ХТМЛ_А, ПР_БОДИ_ХТМЛ_В</span><span class="sxs-lookup"><span data-stu-id="a9ef2-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="a9ef2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a9ef2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9ef2-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="a9ef2-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="a9ef2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a9ef2-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9ef2-111">ПТ_УНИКОДЕ, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a9ef2-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a9ef2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a9ef2-112">Area:</span></span>  <br/> |<span data-ttu-id="a9ef2-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="a9ef2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9ef2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9ef2-114">Remarks</span></span>

<span data-ttu-id="a9ef2-115">Эти свойства содержат тот же текст сообщения, что и **пр_боди_контент_локатион** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), но в HTML.</span><span class="sxs-lookup"><span data-stu-id="a9ef2-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="a9ef2-116">Хранилище сообщений, поддерживающее HTML, указывает на это путем установки флага **сторе_хтмл_ок** в его **пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a9ef2-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="a9ef2-117">**Note (Примечание** ) **Сторе_хтмл_ок** не определен в версиях MAPIDEFS. h, включенНых в Microsoft ® Exchange 2000 Server и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="a9ef2-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="a9ef2-118">Если **сторе_хтмл_ок** не определен, используйте вместо этого значение 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="a9ef2-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a9ef2-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a9ef2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9ef2-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a9ef2-120">Protocol specifications</span></span>

<span data-ttu-id="a9ef2-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9ef2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9ef2-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a9ef2-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9ef2-123">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9ef2-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9ef2-124">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="a9ef2-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9ef2-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="a9ef2-125">Header files</span></span>

<span data-ttu-id="a9ef2-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a9ef2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9ef2-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a9ef2-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9ef2-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="a9ef2-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a9ef2-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="a9ef2-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9ef2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a9ef2-130">See also</span></span>



[<span data-ttu-id="a9ef2-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a9ef2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9ef2-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="a9ef2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9ef2-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a9ef2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9ef2-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a9ef2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

