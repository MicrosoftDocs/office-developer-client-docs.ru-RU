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
ms.openlocfilehash: dc77f9c7b58fc925048d6dec2bee2ff96a8723b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810824"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="61f6e-103">Каноническое свойство PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="61f6e-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="61f6e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61f6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61f6e-105">Содержит значение TRUE, если отправитель разрешает автоматическое перенаправление этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="61f6e-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61f6e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="61f6e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61f6e-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="61f6e-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="61f6e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="61f6e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="61f6e-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="61f6e-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="61f6e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="61f6e-110">Data type:</span></span>  <br/> |<span data-ttu-id="61f6e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="61f6e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="61f6e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="61f6e-112">Area:</span></span>  <br/> |<span data-ttu-id="61f6e-113">Address</span><span class="sxs-lookup"><span data-stu-id="61f6e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61f6e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="61f6e-114">Remarks</span></span>

<span data-ttu-id="61f6e-115">Если автоматическая переадресация не разрешается или обозначенный альтернативного получатели, будет создан отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="61f6e-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="61f6e-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="61f6e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="61f6e-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="61f6e-117">Protocol specifications</span></span>

<span data-ttu-id="61f6e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61f6e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61f6e-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="61f6e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="61f6e-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61f6e-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61f6e-121">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="61f6e-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="61f6e-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61f6e-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61f6e-123">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="61f6e-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="61f6e-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61f6e-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61f6e-125">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="61f6e-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="61f6e-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="61f6e-126">Header files</span></span>

<span data-ttu-id="61f6e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61f6e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="61f6e-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="61f6e-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="61f6e-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="61f6e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="61f6e-130">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="61f6e-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61f6e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="61f6e-131">See also</span></span>



[<span data-ttu-id="61f6e-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="61f6e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61f6e-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="61f6e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61f6e-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="61f6e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61f6e-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="61f6e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

