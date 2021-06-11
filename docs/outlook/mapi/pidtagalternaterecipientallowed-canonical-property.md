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
ms.openlocfilehash: 0faeb12ee54ec5d1c584bacd51590b157035f4fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327988"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="5ffa4-103">Каноническое свойство PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="5ffa4-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="5ffa4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ffa4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ffa4-105">Содержит TRUE, если отправитель разрешает автопродавку этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ffa4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5ffa4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ffa4-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="5ffa4-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="5ffa4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5ffa4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ffa4-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="5ffa4-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="5ffa4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5ffa4-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ffa4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5ffa4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5ffa4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5ffa4-112">Area:</span></span>  <br/> |<span data-ttu-id="5ffa4-113">Адрес</span><span class="sxs-lookup"><span data-stu-id="5ffa4-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ffa4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ffa4-114">Remarks</span></span>

<span data-ttu-id="5ffa4-115">Если автопередача запрещена или не назначен альтернативный получатель, следует сгенерить отчет о неделивстве.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5ffa4-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ffa4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ffa4-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5ffa4-117">Protocol specifications</span></span>

<span data-ttu-id="5ffa4-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ffa4-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ffa4-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ffa4-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ffa4-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ffa4-121">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5ffa4-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ffa4-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ffa4-123">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5ffa4-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ffa4-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ffa4-125">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ffa4-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5ffa4-126">Header files</span></span>

<span data-ttu-id="5ffa4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ffa4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ffa4-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ffa4-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5ffa4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="5ffa4-130">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ffa4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5ffa4-131">See also</span></span>



[<span data-ttu-id="5ffa4-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ffa4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ffa4-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ffa4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ffa4-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5ffa4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ffa4-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5ffa4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

