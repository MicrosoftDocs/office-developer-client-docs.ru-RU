---
title: Каноническое свойство PidTagSearchFolderTemplateId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387204"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="ac309-103">Каноническое свойство PidTagSearchFolderTemplateId</span><span class="sxs-lookup"><span data-stu-id="ac309-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="ac309-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac309-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac309-105">Содержит идентификатор шаблона, который используется для поиска.</span><span class="sxs-lookup"><span data-stu-id="ac309-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac309-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ac309-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac309-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="ac309-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="ac309-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ac309-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac309-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="ac309-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="ac309-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ac309-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac309-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ac309-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ac309-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ac309-112">Area:</span></span>  <br/> |<span data-ttu-id="ac309-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="ac309-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac309-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ac309-114">Remarks</span></span>

<span data-ttu-id="ac309-115">Условия папки поиска задается с помощью шаблона.</span><span class="sxs-lookup"><span data-stu-id="ac309-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="ac309-116">Это свойство в окне сообщения, определяющий папки поиска определяет ее шаблон.</span><span class="sxs-lookup"><span data-stu-id="ac309-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="ac309-117">В дополнение к определяется условия поиска, шаблон также определяет папок, которые следует исключить из поиска, определяет элементы, исключаемые из поиска и задает значение **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ac309-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="ac309-118">Дополнительные сведения о шаблонах папки поиска можно [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ac309-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ac309-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ac309-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac309-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ac309-120">Protocol specifications</span></span>

<span data-ttu-id="ac309-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac309-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac309-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ac309-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac309-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac309-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac309-124">Задает свойства и операции для управления конфигурации список папок поиска.</span><span class="sxs-lookup"><span data-stu-id="ac309-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac309-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ac309-125">Header files</span></span>

<span data-ttu-id="ac309-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac309-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac309-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ac309-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac309-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac309-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ac309-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ac309-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac309-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ac309-130">See also</span></span>



[<span data-ttu-id="ac309-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ac309-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac309-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ac309-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac309-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ac309-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac309-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ac309-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

