---
title: Каноническое свойство PidTagAlternateRecipientAllowed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipientAllowed
api_type:
- HeaderDef
ms.assetid: dbbdeb54-3d14-4601-a77b-55ee31f33416
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0fcea0f0bc19140c5a0762143ce91bd41ea8fd07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569325"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="663ec-103">Каноническое свойство PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="663ec-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="663ec-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="663ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="663ec-105">Содержит значение TRUE, если отправитель разрешает автоматическое перенаправление этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="663ec-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="663ec-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="663ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="663ec-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="663ec-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="663ec-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="663ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="663ec-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="663ec-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="663ec-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="663ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="663ec-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="663ec-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="663ec-112">Область:</span><span class="sxs-lookup"><span data-stu-id="663ec-112">Area:</span></span>  <br/> |<span data-ttu-id="663ec-113">Address</span><span class="sxs-lookup"><span data-stu-id="663ec-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="663ec-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="663ec-114">Remarks</span></span>

<span data-ttu-id="663ec-115">Если автоматическая переадресация не разрешается или обозначенный альтернативного получатели, будет создан отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="663ec-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="663ec-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="663ec-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="663ec-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="663ec-117">Protocol specifications</span></span>

<span data-ttu-id="663ec-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="663ec-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="663ec-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="663ec-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="663ec-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="663ec-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="663ec-121">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="663ec-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="663ec-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="663ec-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="663ec-123">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="663ec-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="663ec-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="663ec-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="663ec-125">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="663ec-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="663ec-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="663ec-126">Header files</span></span>

<span data-ttu-id="663ec-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="663ec-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="663ec-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="663ec-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="663ec-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="663ec-129">Mapitags.h</span></span>
  
> <span data-ttu-id="663ec-130">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="663ec-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="663ec-131">См. также</span><span class="sxs-lookup"><span data-stu-id="663ec-131">See also</span></span>



[<span data-ttu-id="663ec-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="663ec-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="663ec-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="663ec-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="663ec-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="663ec-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="663ec-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="663ec-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

