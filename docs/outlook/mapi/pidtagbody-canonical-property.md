---
title: Каноническое свойство PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 23d943d5576f5e9d7694b03c90dea79a878dee64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810888"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="3db9a-103">Каноническое свойство PidTagBody</span><span class="sxs-lookup"><span data-stu-id="3db9a-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="3db9a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3db9a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3db9a-105">Содержит текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="3db9a-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3db9a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3db9a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3db9a-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="3db9a-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="3db9a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3db9a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3db9a-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="3db9a-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="3db9a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3db9a-110">Data type:</span></span>  <br/> |<span data-ttu-id="3db9a-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3db9a-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3db9a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3db9a-112">Area:</span></span>  <br/> |<span data-ttu-id="3db9a-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="3db9a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3db9a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3db9a-114">Remarks</span></span>

<span data-ttu-id="3db9a-115">Эти свойства обычно используются только в сообщении электронной почты — это (IPM).</span><span class="sxs-lookup"><span data-stu-id="3db9a-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="3db9a-116">Хранилищ сообщений, которые поддерживают форматированный текст (RTF) игнорировать любые изменения пробелы в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="3db9a-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="3db9a-117">При **PR_BODY** хранится в первый раз, хранилище сообщений также создает и сохраняет свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) версии RTF текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="3db9a-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="3db9a-118">Если вызывается метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , были ли изменены **PR_BODY** хранилище сообщений вызывает функцию [RTFSync](rtfsync.md) для синхронизации с версией RTF.</span><span class="sxs-lookup"><span data-stu-id="3db9a-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="3db9a-119">Только изменился пробелы свойства остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="3db9a-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="3db9a-120">Это позволяет сохранить все нестандартный формат RTF форматирования при передаче сообщения через поддерживающими RTF клиентов и системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3db9a-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="3db9a-121">Значение для этого свойства должны быть выражены на странице кода операционной системы, где работает MAPI.</span><span class="sxs-lookup"><span data-stu-id="3db9a-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3db9a-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3db9a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3db9a-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3db9a-123">Protocol specifications</span></span>

<span data-ttu-id="3db9a-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3db9a-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3db9a-125">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3db9a-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3db9a-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3db9a-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3db9a-127">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="3db9a-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3db9a-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3db9a-128">Header files</span></span>

<span data-ttu-id="3db9a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3db9a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="3db9a-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3db9a-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="3db9a-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3db9a-131">Mapitags.h</span></span>
  
> <span data-ttu-id="3db9a-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3db9a-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3db9a-133">См. также</span><span class="sxs-lookup"><span data-stu-id="3db9a-133">See also</span></span>



[<span data-ttu-id="3db9a-134">Каноническое свойство PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="3db9a-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="3db9a-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3db9a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3db9a-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3db9a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3db9a-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3db9a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3db9a-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3db9a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

