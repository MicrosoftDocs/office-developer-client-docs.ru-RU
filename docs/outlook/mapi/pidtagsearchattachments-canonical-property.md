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
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="fd310-103">Каноническое свойство PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="fd310-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="fd310-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd310-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd310-105">Содержит строку в Юникоде, запрашиваемую в содержимом вложения в хранилище.</span><span class="sxs-lookup"><span data-stu-id="fd310-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="fd310-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fd310-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd310-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="fd310-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="fd310-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fd310-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd310-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="fd310-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="fd310-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="fd310-110">Property type:</span></span>  <br/> |<span data-ttu-id="fd310-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fd310-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fd310-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fd310-112">Area:</span></span>  <br/> |<span data-ttu-id="fd310-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="fd310-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fd310-114">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fd310-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="fd310-115">Этот тег ограничения MAPI, используемый при поиске содержимого вложений, может не определяться в файле заголовков, доступных для загрузки.</span><span class="sxs-lookup"><span data-stu-id="fd310-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="fd310-116">Вы можете добавить его в код, используя следующее значение: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="fd310-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="fd310-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fd310-117">Protocol specifications</span></span>

<span data-ttu-id="fd310-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd310-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd310-119">Содержит ссылки на соответствующие спецификации протоколов Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fd310-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd310-120">[[MS — ОКСОСРЧ]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd310-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd310-121">Задает свойства и операции для управления конфигурацией списка папок поиска.</span><span class="sxs-lookup"><span data-stu-id="fd310-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd310-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fd310-122">Header files</span></span>

<span data-ttu-id="fd310-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="fd310-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd310-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fd310-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd310-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="fd310-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fd310-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="fd310-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd310-127">См. также</span><span class="sxs-lookup"><span data-stu-id="fd310-127">See also</span></span>



[<span data-ttu-id="fd310-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd310-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd310-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="fd310-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd310-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fd310-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd310-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fd310-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

