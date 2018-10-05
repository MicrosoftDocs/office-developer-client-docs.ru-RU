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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392783"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="fed19-103">Каноническое свойство PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="fed19-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="fed19-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fed19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fed19-105">Содержит список идентификаторов запись для альтернативного получателей, обозначенного исходный получатель.</span><span class="sxs-lookup"><span data-stu-id="fed19-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fed19-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fed19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fed19-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="fed19-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="fed19-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fed19-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fed19-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="fed19-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="fed19-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fed19-110">Data type:</span></span>  <br/> |<span data-ttu-id="fed19-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fed19-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fed19-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fed19-112">Area:</span></span>  <br/> |<span data-ttu-id="fed19-113">Address</span><span class="sxs-lookup"><span data-stu-id="fed19-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fed19-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fed19-114">Remarks</span></span>

<span data-ttu-id="fed19-115">Это свойство используется для автоматической пересылки сообщений.</span><span class="sxs-lookup"><span data-stu-id="fed19-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="fed19-116">Она содержит структуру [FLATENTRYLIST](flatentrylist.md) альтернативного получателей.</span><span class="sxs-lookup"><span data-stu-id="fed19-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="fed19-117">Если autoforwarding не разрешается или обозначенный альтернативного получатели, создается отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="fed19-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fed19-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fed19-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fed19-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fed19-119">Protocol specifications</span></span>

<span data-ttu-id="fed19-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fed19-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fed19-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fed19-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fed19-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fed19-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fed19-123">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="fed19-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="fed19-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fed19-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fed19-125">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="fed19-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="fed19-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fed19-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fed19-127">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="fed19-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fed19-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fed19-128">Header files</span></span>

<span data-ttu-id="fed19-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fed19-129">Mapitags.h</span></span>
  
> <span data-ttu-id="fed19-130">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="fed19-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="fed19-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fed19-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="fed19-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fed19-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fed19-133">См. также</span><span class="sxs-lookup"><span data-stu-id="fed19-133">See also</span></span>



[<span data-ttu-id="fed19-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="fed19-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="fed19-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fed19-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fed19-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fed19-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fed19-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fed19-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fed19-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fed19-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

