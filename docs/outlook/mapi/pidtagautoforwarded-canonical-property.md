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
ms.openlocfilehash: 49e5e3f84d747210ba42870be5fc328c83bae883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565902"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="d0c33-103">Каноническое свойство PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="d0c33-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="d0c33-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0c33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0c33-105">Содержит значение TRUE, если клиент запрашивает поле заголовка X-MS-Exchange-организации-автоматически переадресовано.</span><span class="sxs-lookup"><span data-stu-id="d0c33-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0c33-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d0c33-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0c33-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="d0c33-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="d0c33-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d0c33-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0c33-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="d0c33-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="d0c33-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d0c33-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0c33-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d0c33-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d0c33-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d0c33-112">Area:</span></span>  <br/> |<span data-ttu-id="d0c33-113">Общие отчеты</span><span class="sxs-lookup"><span data-stu-id="d0c33-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0c33-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d0c33-114">Remarks</span></span>

<span data-ttu-id="d0c33-115">Если это свойство присвоено значение FALSE или не используется, будут создаваться без поле заголовка X-MS-Exchange-организации-автоматически переадресовано.</span><span class="sxs-lookup"><span data-stu-id="d0c33-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d0c33-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d0c33-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0c33-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d0c33-117">Protocol specifications</span></span>

<span data-ttu-id="d0c33-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0c33-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0c33-119">Определяет каждого свойства, которое используется в объектах, описанные с префиксом MS-OXO документы.</span><span class="sxs-lookup"><span data-stu-id="d0c33-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="d0c33-120">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0c33-120">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0c33-121">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0c33-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0c33-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d0c33-122">Header files</span></span>

<span data-ttu-id="d0c33-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0c33-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0c33-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d0c33-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0c33-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0c33-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d0c33-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d0c33-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0c33-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d0c33-127">See also</span></span>



[<span data-ttu-id="d0c33-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d0c33-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0c33-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d0c33-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0c33-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d0c33-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0c33-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d0c33-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

