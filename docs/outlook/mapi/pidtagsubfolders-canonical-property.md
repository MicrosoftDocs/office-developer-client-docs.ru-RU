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
ms.openlocfilehash: 8de14542c0d2a4e6d95fb4258697b827f82b8d06
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384404"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="67927-103">Каноническое свойство PidTagSubfolders</span><span class="sxs-lookup"><span data-stu-id="67927-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="67927-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67927-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67927-105">Содержит значение TRUE, если папка содержит вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="67927-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67927-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="67927-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67927-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="67927-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="67927-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="67927-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67927-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="67927-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="67927-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="67927-110">Data type:</span></span>  <br/> |<span data-ttu-id="67927-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="67927-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="67927-112">Область:</span><span class="sxs-lookup"><span data-stu-id="67927-112">Area:</span></span>  <br/> |<span data-ttu-id="67927-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="67927-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67927-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="67927-114">Remarks</span></span>

<span data-ttu-id="67927-115">Хранилищ сообщений необходимо задать это свойство для всех папок.</span><span class="sxs-lookup"><span data-stu-id="67927-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="67927-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="67927-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67927-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="67927-117">Protocol specifications</span></span>

<span data-ttu-id="67927-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67927-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67927-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="67927-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67927-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67927-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67927-121">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="67927-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67927-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="67927-122">Header files</span></span>

<span data-ttu-id="67927-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67927-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="67927-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="67927-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="67927-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67927-125">Mapitags.h</span></span>
  
> <span data-ttu-id="67927-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="67927-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67927-127">См. также</span><span class="sxs-lookup"><span data-stu-id="67927-127">See also</span></span>



[<span data-ttu-id="67927-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="67927-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67927-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="67927-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67927-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="67927-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67927-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="67927-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

