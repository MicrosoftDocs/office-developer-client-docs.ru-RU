---
title: Каноническое свойство PidTagAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7c304de3184e49044d3f83cef1f1ebaac019b2ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360098"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="01cc4-103">Каноническое свойство PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="01cc4-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="01cc4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01cc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01cc4-105">Содержит список идентификаторов записей для альтернативных получателей, назначенных исходным получателем.</span><span class="sxs-lookup"><span data-stu-id="01cc4-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01cc4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="01cc4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01cc4-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="01cc4-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="01cc4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="01cc4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01cc4-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="01cc4-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="01cc4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="01cc4-110">Data type:</span></span>  <br/> |<span data-ttu-id="01cc4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="01cc4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="01cc4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="01cc4-112">Area:</span></span>  <br/> |<span data-ttu-id="01cc4-113">Address</span><span class="sxs-lookup"><span data-stu-id="01cc4-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01cc4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="01cc4-114">Remarks</span></span>

<span data-ttu-id="01cc4-115">Это свойство используется для автоматически переадресованных сообщений.</span><span class="sxs-lookup"><span data-stu-id="01cc4-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="01cc4-116">Он содержит структуру [флатентрилист](flatentrylist.md) альтернативных получателей.</span><span class="sxs-lookup"><span data-stu-id="01cc4-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="01cc4-117">Если Перемотка не разрешены или если не назначен альтернативный получатель, создается отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="01cc4-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="01cc4-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01cc4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01cc4-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="01cc4-119">Protocol specifications</span></span>

<span data-ttu-id="01cc4-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01cc4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01cc4-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="01cc4-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01cc4-122">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01cc4-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01cc4-123">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="01cc4-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="01cc4-124">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01cc4-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01cc4-125">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="01cc4-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="01cc4-126">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01cc4-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01cc4-127">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="01cc4-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01cc4-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="01cc4-128">Header files</span></span>

<span data-ttu-id="01cc4-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="01cc4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="01cc4-130">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="01cc4-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="01cc4-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="01cc4-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="01cc4-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="01cc4-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01cc4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="01cc4-133">See also</span></span>



[<span data-ttu-id="01cc4-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="01cc4-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="01cc4-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01cc4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01cc4-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="01cc4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01cc4-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="01cc4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01cc4-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="01cc4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

