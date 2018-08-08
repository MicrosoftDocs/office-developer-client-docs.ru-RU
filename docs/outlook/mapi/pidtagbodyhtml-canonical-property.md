---
title: Каноническое свойство PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 19f0398d5e36cce13467a4fae86c4ea1d4019dd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810898"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="7b4e0-103">Каноническое свойство PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="7b4e0-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="7b4e0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b4e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b4e0-105">Содержит версию языка (HTML) текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="7b4e0-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b4e0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7b4e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b4e0-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="7b4e0-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="7b4e0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7b4e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b4e0-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="7b4e0-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="7b4e0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7b4e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b4e0-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7b4e0-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="7b4e0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7b4e0-112">Area:</span></span>  <br/> |<span data-ttu-id="7b4e0-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="7b4e0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b4e0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b4e0-114">Remarks</span></span>

<span data-ttu-id="7b4e0-115">Эти свойства содержит текст сообщения, как **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), но в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="7b4e0-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="7b4e0-116">Хранилище сообщений, который поддерживает HTML указывает это, установив флаг **STORE_HTML_OK** в его **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7b4e0-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="7b4e0-117">**Примечание** **STORE_HTML_OK** не определен в версии Mapidefs.h, включенные в Microsoft® Exchange 2000 Server и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="7b4e0-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="7b4e0-118">Если **STORE_HTML_OK** не определен, используется значение 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="7b4e0-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7b4e0-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b4e0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b4e0-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7b4e0-120">Protocol specifications</span></span>

<span data-ttu-id="7b4e0-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b4e0-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b4e0-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7b4e0-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b4e0-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b4e0-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b4e0-124">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="7b4e0-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b4e0-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7b4e0-125">Header files</span></span>

<span data-ttu-id="7b4e0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b4e0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b4e0-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b4e0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b4e0-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b4e0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7b4e0-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7b4e0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b4e0-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7b4e0-130">See also</span></span>



[<span data-ttu-id="7b4e0-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b4e0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b4e0-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b4e0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b4e0-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7b4e0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b4e0-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7b4e0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

