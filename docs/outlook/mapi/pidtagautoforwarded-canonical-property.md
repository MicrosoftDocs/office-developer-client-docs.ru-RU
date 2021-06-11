---
title: Каноническое свойство PidTagAutoForwarded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326616"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="6bc03-103">Каноническое свойство PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="6bc03-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="6bc03-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bc03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bc03-105">Содержит TRUE, если клиент запрашивает заглавное Exchange X-MS-Exchange-Organization-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="6bc03-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6bc03-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6bc03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6bc03-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="6bc03-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="6bc03-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6bc03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6bc03-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="6bc03-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="6bc03-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6bc03-110">Data type:</span></span>  <br/> |<span data-ttu-id="6bc03-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6bc03-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6bc03-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6bc03-112">Area:</span></span>  <br/> |<span data-ttu-id="6bc03-113">Общие отчеты</span><span class="sxs-lookup"><span data-stu-id="6bc03-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bc03-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6bc03-114">Remarks</span></span>

<span data-ttu-id="6bc03-115">Если это свойство настроено на FALSE или не используется, не будет создано Exchange X-MS-Exchange-Organization-AutoForwarded header.</span><span class="sxs-lookup"><span data-stu-id="6bc03-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6bc03-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6bc03-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6bc03-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6bc03-117">Protocol specifications</span></span>

<span data-ttu-id="6bc03-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6bc03-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6bc03-119">Определяет каждое свойство, которое используется в объектах, описанных в документах с префиксом MS-OXO.</span><span class="sxs-lookup"><span data-stu-id="6bc03-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="6bc03-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6bc03-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6bc03-121">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="6bc03-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6bc03-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6bc03-122">Header files</span></span>

<span data-ttu-id="6bc03-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6bc03-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6bc03-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6bc03-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6bc03-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6bc03-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6bc03-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6bc03-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6bc03-127">См. также</span><span class="sxs-lookup"><span data-stu-id="6bc03-127">See also</span></span>



[<span data-ttu-id="6bc03-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6bc03-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6bc03-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6bc03-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6bc03-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6bc03-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6bc03-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6bc03-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

