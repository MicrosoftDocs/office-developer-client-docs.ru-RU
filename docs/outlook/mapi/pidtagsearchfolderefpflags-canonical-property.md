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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336430"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="d2e6d-103">Каноническое свойство PidTagSearchFolderEfpFlags</span><span class="sxs-lookup"><span data-stu-id="d2e6d-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d2e6d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2e6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2e6d-105">Содержит флаги расширенных папок, которые применяются к контейнеру папки поиска для папки поиска.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2e6d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d2e6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2e6d-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d2e6d-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="d2e6d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d2e6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2e6d-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="d2e6d-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="d2e6d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d2e6d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2e6d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d2e6d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d2e6d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d2e6d-112">Area:</span></span>  <br/> |<span data-ttu-id="d2e6d-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="d2e6d-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2e6d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2e6d-114">Remarks</span></span>

<span data-ttu-id="d2e6d-115">Это свойство должно содержать флаги в свойстве **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags)](pidtagextendedfolderflags-canonical-property.md)и вложенное свойство **ExtendedFlags** в поле b для папки.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="d2e6d-116">Сведения о флагах папок см. [в [MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2e6d-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d2e6d-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d2e6d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2e6d-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d2e6d-118">Protocol specifications</span></span>

<span data-ttu-id="d2e6d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2e6d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2e6d-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2e6d-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2e6d-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2e6d-122">Указывает свойства и операции для управления конфигурацией списка папок поиска.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="d2e6d-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2e6d-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2e6d-124">Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2e6d-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="d2e6d-125">Header files</span></span>

<span data-ttu-id="d2e6d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2e6d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2e6d-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2e6d-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d2e6d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d2e6d-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2e6d-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d2e6d-130">See also</span></span>



[<span data-ttu-id="d2e6d-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d2e6d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2e6d-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d2e6d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2e6d-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d2e6d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2e6d-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d2e6d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

