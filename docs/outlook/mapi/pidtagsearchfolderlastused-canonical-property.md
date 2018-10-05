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
ms.openlocfilehash: 7ff6df6eddc8e610341cb09ccb152f4ad748a984
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384166"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="c8288-103">Каноническое свойство PidTagSearchFolderLastUsed</span><span class="sxs-lookup"><span data-stu-id="c8288-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="c8288-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8288-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8288-105">Представляет время последнего обращения к папке.</span><span class="sxs-lookup"><span data-stu-id="c8288-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8288-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c8288-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8288-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="c8288-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="c8288-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c8288-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8288-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="c8288-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="c8288-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c8288-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8288-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c8288-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c8288-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c8288-112">Area:</span></span>  <br/> |<span data-ttu-id="c8288-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="c8288-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8288-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c8288-114">Remarks</span></span>

<span data-ttu-id="c8288-115">Это свойство должен быть отформатирован в поле число минут после полночи по Гринвичу (UTC) 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="c8288-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8288-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c8288-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8288-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c8288-117">Protocol specifications</span></span>

<span data-ttu-id="c8288-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8288-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8288-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c8288-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8288-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8288-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8288-121">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="c8288-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8288-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c8288-122">Header files</span></span>

<span data-ttu-id="c8288-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8288-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8288-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c8288-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8288-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8288-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c8288-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c8288-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8288-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c8288-127">See also</span></span>



[<span data-ttu-id="c8288-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8288-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8288-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8288-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8288-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c8288-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8288-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c8288-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

