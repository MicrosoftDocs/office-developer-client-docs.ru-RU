---
title: Каноническое свойство PidTagSearchFolderLastUsed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderLastUsed
api_type:
- COM
ms.assetid: e4071307-6205-4079-ab65-7499d14f145c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cafa336bf915abd35de07a11ee65baf9ac4d69f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572692"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="fd691-103">Каноническое свойство PidTagSearchFolderLastUsed</span><span class="sxs-lookup"><span data-stu-id="fd691-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="fd691-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd691-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd691-105">Представляет время последнего обращения к папке.</span><span class="sxs-lookup"><span data-stu-id="fd691-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd691-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fd691-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd691-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="fd691-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="fd691-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fd691-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd691-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="fd691-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="fd691-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fd691-110">Data type:</span></span>  <br/> |<span data-ttu-id="fd691-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fd691-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fd691-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fd691-112">Area:</span></span>  <br/> |<span data-ttu-id="fd691-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="fd691-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd691-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fd691-114">Remarks</span></span>

<span data-ttu-id="fd691-115">Это свойство должен быть отформатирован в поле число минут после полночи по Гринвичу (UTC) 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="fd691-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd691-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fd691-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd691-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fd691-117">Protocol specifications</span></span>

<span data-ttu-id="fd691-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd691-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd691-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fd691-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd691-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd691-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd691-121">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="fd691-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd691-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fd691-122">Header files</span></span>

<span data-ttu-id="fd691-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd691-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd691-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fd691-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd691-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fd691-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fd691-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="fd691-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd691-127">См. также</span><span class="sxs-lookup"><span data-stu-id="fd691-127">See also</span></span>



[<span data-ttu-id="fd691-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd691-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd691-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd691-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd691-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fd691-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd691-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fd691-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

