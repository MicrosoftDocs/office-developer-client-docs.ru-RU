---
title: Каноническое свойство PidTagSubfolders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubfolders
api_type:
- COM
ms.assetid: b456b07b-4d83-46bf-a305-4f322ea7dbd1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 93e5510802fe5ff0327d7ed3fc702fa61cd3c1c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565580"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="cacbd-103">Каноническое свойство PidTagSubfolders</span><span class="sxs-lookup"><span data-stu-id="cacbd-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="cacbd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cacbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cacbd-105">Содержит значение TRUE, если папка содержит вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="cacbd-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cacbd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cacbd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cacbd-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="cacbd-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="cacbd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cacbd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cacbd-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="cacbd-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="cacbd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cacbd-110">Data type:</span></span>  <br/> |<span data-ttu-id="cacbd-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cacbd-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="cacbd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cacbd-112">Area:</span></span>  <br/> |<span data-ttu-id="cacbd-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="cacbd-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cacbd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="cacbd-114">Remarks</span></span>

<span data-ttu-id="cacbd-115">Хранилищ сообщений необходимо задать это свойство для всех папок.</span><span class="sxs-lookup"><span data-stu-id="cacbd-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cacbd-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cacbd-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cacbd-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cacbd-117">Protocol specifications</span></span>

<span data-ttu-id="cacbd-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cacbd-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cacbd-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cacbd-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cacbd-120">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cacbd-120">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cacbd-121">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="cacbd-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cacbd-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cacbd-122">Header files</span></span>

<span data-ttu-id="cacbd-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cacbd-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="cacbd-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cacbd-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="cacbd-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cacbd-125">Mapitags.h</span></span>
  
> <span data-ttu-id="cacbd-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="cacbd-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cacbd-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cacbd-127">See also</span></span>



[<span data-ttu-id="cacbd-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cacbd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cacbd-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cacbd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cacbd-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cacbd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cacbd-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cacbd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

