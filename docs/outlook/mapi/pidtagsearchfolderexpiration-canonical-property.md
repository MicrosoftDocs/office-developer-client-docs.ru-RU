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
ms.openlocfilehash: a2f72f68926665087ee8e3a0c9e8394042a8f955
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590773"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="d85ce-103">Каноническое свойство PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="d85ce-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="d85ce-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d85ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d85ce-105">Содержит время, по которому будет устаревших контейнер папки поиска и должен обновить или создать заново.</span><span class="sxs-lookup"><span data-stu-id="d85ce-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d85ce-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d85ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d85ce-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="d85ce-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="d85ce-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d85ce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d85ce-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="d85ce-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="d85ce-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d85ce-110">Data type:</span></span>  <br/> |<span data-ttu-id="d85ce-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d85ce-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d85ce-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d85ce-112">Area:</span></span>  <br/> |<span data-ttu-id="d85ce-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="d85ce-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d85ce-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d85ce-114">Remarks</span></span>

<span data-ttu-id="d85ce-115">Это свойство должен быть отформатирован в поле число минут после полночи по Гринвичу (UTC) 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="d85ce-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d85ce-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d85ce-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d85ce-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d85ce-117">Protocol specifications</span></span>

<span data-ttu-id="d85ce-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d85ce-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d85ce-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d85ce-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d85ce-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d85ce-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d85ce-121">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="d85ce-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d85ce-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d85ce-122">Header files</span></span>

<span data-ttu-id="d85ce-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d85ce-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d85ce-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d85ce-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d85ce-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d85ce-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d85ce-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d85ce-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d85ce-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d85ce-127">See also</span></span>



[<span data-ttu-id="d85ce-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d85ce-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d85ce-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d85ce-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d85ce-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d85ce-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d85ce-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d85ce-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

