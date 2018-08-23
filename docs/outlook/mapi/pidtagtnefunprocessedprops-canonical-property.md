---
title: Каноническое свойство PidTagTnefUnprocessedProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c25888353857f9233ba487661f5f27d64cd678cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577431"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a><span data-ttu-id="12332-103">Каноническое свойство PidTagTnefUnprocessedProps</span><span class="sxs-lookup"><span data-stu-id="12332-103">PidTagTnefUnprocessedProps Canonical Property</span></span>

  
  
<span data-ttu-id="12332-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12332-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12332-105">Выполняет сериализацию свойства при фильтрации транспорта Neutral Encapsulation формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="12332-105">Serializes properties when filtering Transport Neutral Encapsulation Format (TNEF).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12332-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="12332-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12332-107">PR_TNEF_UNPROCESSED_PROPS</span><span class="sxs-lookup"><span data-stu-id="12332-107">PR_TNEF_UNPROCESSED_PROPS</span></span>  <br/> |
|<span data-ttu-id="12332-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="12332-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12332-109">0x0E9C</span><span class="sxs-lookup"><span data-stu-id="12332-109">0x0E9C</span></span>  <br/> |
|<span data-ttu-id="12332-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="12332-110">Data type:</span></span>  <br/> |<span data-ttu-id="12332-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="12332-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="12332-112">Область:</span><span class="sxs-lookup"><span data-stu-id="12332-112">Area:</span></span>  <br/> |<span data-ttu-id="12332-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="12332-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12332-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="12332-114">Remarks</span></span>

<span data-ttu-id="12332-115">Используемый Microsoft Outlook и Outlook Web Access (OWA) для сохранения исходного формата TNEF в случае наличия TNEF именованных свойств, которые не могут быть созданы в хранилище.</span><span class="sxs-lookup"><span data-stu-id="12332-115">Used by Microsoft Outlook and Outlook Web Access (OWA) for saving the original TNEF in cases where the TNEF contains named properties that cannot be created in the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="12332-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="12332-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="12332-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="12332-117">Header files</span></span>

<span data-ttu-id="12332-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12332-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="12332-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="12332-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="12332-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="12332-120">Mapitags.h</span></span>
  
> <span data-ttu-id="12332-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="12332-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12332-122">См. также</span><span class="sxs-lookup"><span data-stu-id="12332-122">See also</span></span>



[<span data-ttu-id="12332-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12332-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12332-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12332-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12332-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="12332-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12332-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="12332-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

