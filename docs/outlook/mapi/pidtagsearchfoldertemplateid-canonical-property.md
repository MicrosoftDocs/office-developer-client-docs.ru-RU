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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336626"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="6937e-103">Каноническое свойство PidTagSearchFolderTemplateId</span><span class="sxs-lookup"><span data-stu-id="6937e-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="6937e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6937e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6937e-105">Содержит ИД шаблона, используемого для поиска.</span><span class="sxs-lookup"><span data-stu-id="6937e-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6937e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6937e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6937e-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="6937e-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="6937e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6937e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6937e-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="6937e-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="6937e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6937e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6937e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6937e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6937e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6937e-112">Area:</span></span>  <br/> |<span data-ttu-id="6937e-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="6937e-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6937e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6937e-114">Remarks</span></span>

<span data-ttu-id="6937e-115">Критерии папки поиска заданы шаблоном.</span><span class="sxs-lookup"><span data-stu-id="6937e-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="6937e-116">Это свойство в сообщении, которое определяет папку поиска, определяет соответствующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="6937e-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="6937e-117">Помимо определения критериев поиска, шаблон также определяет папки, которые необходимо исключить из поиска, определяет элементы, которые необходимо исключить из поиска, и указывает значение **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType).](pidtagsearchfolderstoragetype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6937e-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="6937e-118">Дополнительные сведения о шаблонах папок поиска см. [в [MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6937e-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6937e-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6937e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6937e-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6937e-120">Protocol specifications</span></span>

<span data-ttu-id="6937e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6937e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6937e-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6937e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6937e-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6937e-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6937e-124">Указывает свойства и операции для управления конфигурацией списка папок поиска.</span><span class="sxs-lookup"><span data-stu-id="6937e-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6937e-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6937e-125">Header files</span></span>

<span data-ttu-id="6937e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6937e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6937e-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6937e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6937e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6937e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6937e-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6937e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6937e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6937e-130">See also</span></span>



[<span data-ttu-id="6937e-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6937e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6937e-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6937e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6937e-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6937e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6937e-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6937e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

