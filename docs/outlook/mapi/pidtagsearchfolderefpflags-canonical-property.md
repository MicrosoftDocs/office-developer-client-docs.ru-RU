---
title: Каноническое свойство PidTagSearchFolderEfpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400665"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="80e45-103">Каноническое свойство PidTagSearchFolderEfpFlags</span><span class="sxs-lookup"><span data-stu-id="80e45-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="80e45-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80e45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80e45-105">Содержит флаги расширенной папки, которые применяются к контейнеру папки поиска для папки поиска.</span><span class="sxs-lookup"><span data-stu-id="80e45-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80e45-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="80e45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80e45-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="80e45-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="80e45-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="80e45-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80e45-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="80e45-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="80e45-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="80e45-110">Data type:</span></span>  <br/> |<span data-ttu-id="80e45-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="80e45-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="80e45-112">Область:</span><span class="sxs-lookup"><span data-stu-id="80e45-112">Area:</span></span>  <br/> |<span data-ttu-id="80e45-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="80e45-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80e45-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="80e45-114">Remarks</span></span>

<span data-ttu-id="80e45-115">В частности, это свойство должно содержать флаги в свойстве **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) и **ExtendedFlags** подчиненных свойств, в поле b для папки.</span><span class="sxs-lookup"><span data-stu-id="80e45-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="80e45-116">Сведения о папке флаги [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="80e45-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80e45-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="80e45-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80e45-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="80e45-118">Protocol specifications</span></span>

<span data-ttu-id="80e45-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80e45-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80e45-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="80e45-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80e45-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80e45-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80e45-122">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="80e45-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="80e45-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80e45-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80e45-124">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="80e45-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80e45-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="80e45-125">Header files</span></span>

<span data-ttu-id="80e45-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80e45-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="80e45-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="80e45-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="80e45-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="80e45-128">Mapitags.h</span></span>
  
> <span data-ttu-id="80e45-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="80e45-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80e45-130">См. также</span><span class="sxs-lookup"><span data-stu-id="80e45-130">See also</span></span>



[<span data-ttu-id="80e45-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="80e45-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80e45-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="80e45-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80e45-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="80e45-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80e45-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="80e45-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

