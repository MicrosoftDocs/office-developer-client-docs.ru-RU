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
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326637"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="ef8f4-103">Каноническое свойство PidTagBody</span><span class="sxs-lookup"><span data-stu-id="ef8f4-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="ef8f4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef8f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef8f4-105">Содержит текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef8f4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ef8f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef8f4-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="ef8f4-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="ef8f4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ef8f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef8f4-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="ef8f4-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="ef8f4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ef8f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef8f4-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ef8f4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ef8f4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ef8f4-112">Area:</span></span>  <br/> |<span data-ttu-id="ef8f4-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="ef8f4-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef8f4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef8f4-114">Remarks</span></span>

<span data-ttu-id="ef8f4-115">Эти свойства обычно используются только в межличностных сообщениях (IPM).</span><span class="sxs-lookup"><span data-stu-id="ef8f4-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="ef8f4-116">В хранилищах сообщений, поддерживаюх формат "Богатый текст" (RTF), игнорируются любые изменения в белом пространстве в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="ef8f4-117">Когда **PR_BODY** хранится впервые, хранилище сообщений также создает и сохраняет **свойство** PR_RTF_COMPRESSED [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)— версию RTF текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="ef8f4-118">Если метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) впоследствии  вызывается и PR_BODY изменен, хранилище сообщений вызывает функцию [RTFSync](rtfsync.md) для обеспечения синхронизации с версией RTF.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="ef8f4-119">Если изменено только белое пространство, свойства остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="ef8f4-120">При этом сохраняется любое нетривиальный форматирование RTF, когда сообщение передается через клиенты и системы обмена сообщениями, не знаюющие RTF.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="ef8f4-121">Значение этого свойства должно быть выражено на странице кода операционной системы, на которую запущен MAPI.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ef8f4-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ef8f4-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef8f4-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ef8f4-123">Protocol specifications</span></span>

<span data-ttu-id="ef8f4-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef8f4-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef8f4-125">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef8f4-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef8f4-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef8f4-127">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef8f4-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="ef8f4-128">Header files</span></span>

<span data-ttu-id="ef8f4-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef8f4-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef8f4-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef8f4-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ef8f4-131">Mapitags.h</span></span>
  
> <span data-ttu-id="ef8f4-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ef8f4-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef8f4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ef8f4-133">See also</span></span>



[<span data-ttu-id="ef8f4-134">Каноническое свойство PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="ef8f4-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="ef8f4-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ef8f4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef8f4-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ef8f4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef8f4-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ef8f4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef8f4-138">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="ef8f4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

