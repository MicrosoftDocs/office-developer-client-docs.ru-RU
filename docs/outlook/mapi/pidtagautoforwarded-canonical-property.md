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
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="efbbc-103">Каноническое свойство PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="efbbc-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="efbbc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efbbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efbbc-105">Содержит значение true, если клиент запрашивает поле заголовка X – MS/Exchange – Organization – переадресованное.</span><span class="sxs-lookup"><span data-stu-id="efbbc-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efbbc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="efbbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efbbc-107">ПР_АУТО_ФОРВАРДЕД</span><span class="sxs-lookup"><span data-stu-id="efbbc-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="efbbc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="efbbc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="efbbc-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="efbbc-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="efbbc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="efbbc-110">Data type:</span></span>  <br/> |<span data-ttu-id="efbbc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="efbbc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="efbbc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="efbbc-112">Area:</span></span>  <br/> |<span data-ttu-id="efbbc-113">Общие отчеты</span><span class="sxs-lookup"><span data-stu-id="efbbc-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efbbc-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="efbbc-114">Remarks</span></span>

<span data-ttu-id="efbbc-115">Если этому свойству присвоено значение FALSE или не используется, будет создано поле заголовка X-MS-Exchange-Organization-reForwarded.</span><span class="sxs-lookup"><span data-stu-id="efbbc-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="efbbc-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="efbbc-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="efbbc-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="efbbc-117">Protocol specifications</span></span>

<span data-ttu-id="efbbc-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efbbc-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efbbc-119">Определяет каждое свойство, используемое в объектах, описанных в документах с префиксом MS-оксо.</span><span class="sxs-lookup"><span data-stu-id="efbbc-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="efbbc-120">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efbbc-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efbbc-121">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="efbbc-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="efbbc-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="efbbc-122">Header files</span></span>

<span data-ttu-id="efbbc-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="efbbc-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="efbbc-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="efbbc-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="efbbc-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="efbbc-125">Mapitags.h</span></span>
  
> <span data-ttu-id="efbbc-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="efbbc-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="efbbc-127">См. также</span><span class="sxs-lookup"><span data-stu-id="efbbc-127">See also</span></span>



[<span data-ttu-id="efbbc-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="efbbc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efbbc-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="efbbc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efbbc-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="efbbc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efbbc-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="efbbc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

