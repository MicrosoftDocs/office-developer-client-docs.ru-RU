---
title: Каноническое свойство PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2f17f273afc3f2537195cde21c7bc30626b13a26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573204"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="edd2f-103">Каноническое свойство PidTagSearchFolderDefinition</span><span class="sxs-lookup"><span data-stu-id="edd2f-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="edd2f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edd2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edd2f-105">Содержит данные, которые указывает условия поиска.</span><span class="sxs-lookup"><span data-stu-id="edd2f-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edd2f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="edd2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edd2f-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="edd2f-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="edd2f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="edd2f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="edd2f-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="edd2f-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="edd2f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="edd2f-110">Data type:</span></span>  <br/> |<span data-ttu-id="edd2f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="edd2f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="edd2f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="edd2f-112">Area:</span></span>  <br/> |<span data-ttu-id="edd2f-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="edd2f-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edd2f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="edd2f-114">Remarks</span></span>

<span data-ttu-id="edd2f-115">Содержимое каждого поля больших двоичных объектов (BLOB) этого свойства зависит от идентификатор шаблона, который указан в свойстве **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="edd2f-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="edd2f-116">Сведения о шаблонах структуры и поиска больших двоичных ОБЪЕКТОВ можно [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="edd2f-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="edd2f-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="edd2f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edd2f-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="edd2f-118">Protocol specifications</span></span>

<span data-ttu-id="edd2f-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd2f-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd2f-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="edd2f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edd2f-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd2f-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd2f-122">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="edd2f-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edd2f-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="edd2f-123">Header files</span></span>

<span data-ttu-id="edd2f-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edd2f-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="edd2f-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="edd2f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="edd2f-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="edd2f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="edd2f-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="edd2f-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edd2f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="edd2f-128">See also</span></span>



[<span data-ttu-id="edd2f-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="edd2f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edd2f-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="edd2f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edd2f-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="edd2f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edd2f-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="edd2f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

