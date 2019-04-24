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
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="b6c15-103">Каноническое свойство PidTagBody</span><span class="sxs-lookup"><span data-stu-id="b6c15-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="b6c15-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6c15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6c15-105">Содержит текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6c15-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6c15-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b6c15-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6c15-107">ПР_БОДИ, ПР_БОДИ_А, ПР_БОДИ_В</span><span class="sxs-lookup"><span data-stu-id="b6c15-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="b6c15-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b6c15-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6c15-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="b6c15-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="b6c15-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b6c15-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6c15-111">ПТ_УНИКОДЕ, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b6c15-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b6c15-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b6c15-112">Area:</span></span>  <br/> |<span data-ttu-id="b6c15-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="b6c15-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6c15-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b6c15-114">Remarks</span></span>

<span data-ttu-id="b6c15-115">Эти свойства обычно используются только в межпользовательских сообщениях (IPM).</span><span class="sxs-lookup"><span data-stu-id="b6c15-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="b6c15-116">Хранилища сообщений, поддерживающие формат RTF, игнорируют все изменения пробелов в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6c15-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="b6c15-117">Когда **пр_боди** хранится в первый раз, хранилище сообщений также создает и сохраняет свойство **пр_ртф_компрессед** ([PIDTAGRTFCOMPRESSED](pidtagrtfcompressed-canonical-property.md)), в формате RTF для текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="b6c15-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="b6c15-118">Если метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) вызывается и **пр_боди** был изменен, хранилище сообщений вызывает функцию [ртфсинк](rtfsync.md) , чтобы обеспечить синхронизацию с версией RTF.</span><span class="sxs-lookup"><span data-stu-id="b6c15-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="b6c15-119">Если было изменено только пустое пространство, свойства остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="b6c15-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="b6c15-120">При этом сохраняется любое нетривиальное форматирование RTF, когда сообщение проходит через клиентов, не поддерживающих RTF, и систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b6c15-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="b6c15-121">Значение этого свойства должно быть выражено на кодовой странице операционной системы, в которой выполняется служба MAPI.</span><span class="sxs-lookup"><span data-stu-id="b6c15-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b6c15-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b6c15-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6c15-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b6c15-123">Protocol specifications</span></span>

<span data-ttu-id="b6c15-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c15-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c15-125">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b6c15-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6c15-126">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c15-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c15-127">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="b6c15-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6c15-128">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b6c15-128">Header files</span></span>

<span data-ttu-id="b6c15-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b6c15-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6c15-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b6c15-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6c15-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b6c15-131">Mapitags.h</span></span>
  
> <span data-ttu-id="b6c15-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b6c15-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6c15-133">См. также</span><span class="sxs-lookup"><span data-stu-id="b6c15-133">See also</span></span>



[<span data-ttu-id="b6c15-134">Каноническое свойство PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="b6c15-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="b6c15-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b6c15-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6c15-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b6c15-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6c15-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b6c15-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6c15-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b6c15-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

