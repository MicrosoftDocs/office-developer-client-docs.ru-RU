---
title: Каноническое свойство PidTagSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342513"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="c4ec8-103">Каноническое свойство PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="c4ec8-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c4ec8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4ec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4ec8-105">Содержит идентификатор записи папки, в которой сообщение должно быть перемещено после отправки.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4ec8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c4ec8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4ec8-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c4ec8-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c4ec8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c4ec8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4ec8-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="c4ec8-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="c4ec8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c4ec8-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4ec8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c4ec8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c4ec8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c4ec8-112">Area:</span></span>  <br/> |<span data-ttu-id="c4ec8-113">MAPI, не передаваемая</span><span class="sxs-lookup"><span data-stu-id="c4ec8-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4ec8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4ec8-114">Remarks</span></span>

<span data-ttu-id="c4ec8-115">Это свойство часто копируется из **свойства PR_IPM_SENTMAIL_ENTRYID** [(PidTagIpmSentMailEntryId),](pidtagipmsentmailentryid-canonical-property.md)стандартной папки отправленных элементов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="c4ec8-116">Клиентские приложения используют это свойство с **свойством PR_DELETE_AFTER_SUBMIT** [(PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)для управления тем, что происходит с сообщением после его отправки.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="c4ec8-117">Либо один, либо другой должны быть установлены, но не оба.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4ec8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c4ec8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4ec8-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c4ec8-119">Protocol specifications</span></span>

<span data-ttu-id="c4ec8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4ec8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4ec8-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4ec8-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4ec8-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4ec8-123">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c4ec8-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4ec8-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4ec8-125">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4ec8-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="c4ec8-126">Header files</span></span>

<span data-ttu-id="c4ec8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4ec8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4ec8-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4ec8-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4ec8-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c4ec8-130">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4ec8-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c4ec8-131">See also</span></span>



[<span data-ttu-id="c4ec8-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c4ec8-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4ec8-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c4ec8-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4ec8-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c4ec8-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4ec8-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="c4ec8-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

