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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339251"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="dae51-103">Каноническое свойство PidTagSubfolders</span><span class="sxs-lookup"><span data-stu-id="dae51-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="dae51-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dae51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dae51-105">Содержит значение TRUE, если папка содержит вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="dae51-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dae51-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dae51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dae51-107">ПР_СУБФОЛДЕРС</span><span class="sxs-lookup"><span data-stu-id="dae51-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="dae51-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dae51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dae51-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="dae51-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="dae51-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dae51-110">Data type:</span></span>  <br/> |<span data-ttu-id="dae51-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dae51-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="dae51-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dae51-112">Area:</span></span>  <br/> |<span data-ttu-id="dae51-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="dae51-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dae51-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dae51-114">Remarks</span></span>

<span data-ttu-id="dae51-115">Хранилища сообщений должны предоставлять это свойство для всех папок.</span><span class="sxs-lookup"><span data-stu-id="dae51-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dae51-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dae51-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dae51-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dae51-117">Protocol specifications</span></span>

<span data-ttu-id="dae51-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dae51-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dae51-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dae51-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dae51-120">[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dae51-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dae51-121">Обрабатывает операции с папками.</span><span class="sxs-lookup"><span data-stu-id="dae51-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dae51-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="dae51-122">Header files</span></span>

<span data-ttu-id="dae51-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="dae51-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="dae51-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dae51-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="dae51-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="dae51-125">Mapitags.h</span></span>
  
> <span data-ttu-id="dae51-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="dae51-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dae51-127">См. также</span><span class="sxs-lookup"><span data-stu-id="dae51-127">See also</span></span>



[<span data-ttu-id="dae51-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dae51-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dae51-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="dae51-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dae51-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dae51-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dae51-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dae51-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

