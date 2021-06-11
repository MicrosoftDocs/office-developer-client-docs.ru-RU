---
title: Каноническое свойство PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336325"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="35cb8-103">Каноническое свойство PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="35cb8-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="35cb8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35cb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35cb8-105">Содержит строку Unicode, запрашиваемую в содержимом вложений в магазине.</span><span class="sxs-lookup"><span data-stu-id="35cb8-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="35cb8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="35cb8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35cb8-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="35cb8-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="35cb8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="35cb8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35cb8-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="35cb8-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="35cb8-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="35cb8-110">Property type:</span></span>  <br/> |<span data-ttu-id="35cb8-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="35cb8-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="35cb8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="35cb8-112">Area:</span></span>  <br/> |<span data-ttu-id="35cb8-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="35cb8-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="35cb8-114">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="35cb8-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="35cb8-115">Этот тег ограничения MAPI, используемый при поиске содержимого вложений, может не быть определен в загружаемом файле загона, который у вас есть в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="35cb8-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="35cb8-116">Его можно добавить в код, используя следующее значение: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="35cb8-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="35cb8-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="35cb8-117">Protocol specifications</span></span>

<span data-ttu-id="35cb8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35cb8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35cb8-119">Содержит ссылки на связанные Microsoft Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="35cb8-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35cb8-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35cb8-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35cb8-121">Указывает свойства и операции для управления конфигурацией списка папки поиска.</span><span class="sxs-lookup"><span data-stu-id="35cb8-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35cb8-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="35cb8-122">Header files</span></span>

<span data-ttu-id="35cb8-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35cb8-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="35cb8-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="35cb8-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="35cb8-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35cb8-125">Mapitags.h</span></span>
  
> <span data-ttu-id="35cb8-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="35cb8-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35cb8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="35cb8-127">See also</span></span>



[<span data-ttu-id="35cb8-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="35cb8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35cb8-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="35cb8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35cb8-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="35cb8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35cb8-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="35cb8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

