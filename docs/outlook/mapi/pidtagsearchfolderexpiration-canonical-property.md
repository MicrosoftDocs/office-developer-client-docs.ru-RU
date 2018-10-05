---
title: Каноническое свойство PidTagSearchFolderExpiration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385948"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="af646-103">Каноническое свойство PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="af646-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="af646-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af646-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af646-105">Содержит время, по которому будет устаревших контейнер папки поиска и должен обновить или создать заново.</span><span class="sxs-lookup"><span data-stu-id="af646-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af646-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="af646-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af646-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="af646-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="af646-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="af646-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af646-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="af646-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="af646-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="af646-110">Data type:</span></span>  <br/> |<span data-ttu-id="af646-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="af646-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="af646-112">Область:</span><span class="sxs-lookup"><span data-stu-id="af646-112">Area:</span></span>  <br/> |<span data-ttu-id="af646-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="af646-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af646-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="af646-114">Remarks</span></span>

<span data-ttu-id="af646-115">Это свойство должен быть отформатирован в поле число минут после полночи по Гринвичу (UTC) 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="af646-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af646-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af646-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af646-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="af646-117">Protocol specifications</span></span>

<span data-ttu-id="af646-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af646-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af646-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="af646-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af646-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af646-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af646-121">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="af646-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af646-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="af646-122">Header files</span></span>

<span data-ttu-id="af646-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af646-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="af646-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="af646-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="af646-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af646-125">Mapitags.h</span></span>
  
> <span data-ttu-id="af646-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="af646-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af646-127">См. также</span><span class="sxs-lookup"><span data-stu-id="af646-127">See also</span></span>



[<span data-ttu-id="af646-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af646-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af646-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af646-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af646-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="af646-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af646-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="af646-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

