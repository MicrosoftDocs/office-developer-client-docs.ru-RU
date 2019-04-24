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
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="94373-103">Каноническое свойство PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="94373-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="94373-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94373-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94373-105">Содержит идентификатор папки, в которую следует переместить сообщение после отправки.</span><span class="sxs-lookup"><span data-stu-id="94373-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94373-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="94373-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94373-107">ПР_СЕНТМАИЛ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="94373-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="94373-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="94373-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94373-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="94373-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="94373-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="94373-110">Data type:</span></span>  <br/> |<span data-ttu-id="94373-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="94373-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="94373-112">Область:</span><span class="sxs-lookup"><span data-stu-id="94373-112">Area:</span></span>  <br/> |<span data-ttu-id="94373-113">Несъемный MAPI</span><span class="sxs-lookup"><span data-stu-id="94373-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94373-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94373-114">Remarks</span></span>

<span data-ttu-id="94373-115">Это свойство часто копируется из свойства **пр_ипм_сентмаил_ентрид** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) в стандартную папку "Отправленные" клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="94373-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="94373-116">Клиентское приложение использует это свойство со свойством **пр_делете_афтер_субмит** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)), чтобы контролировать, что происходит с сообщением после его отправки.</span><span class="sxs-lookup"><span data-stu-id="94373-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="94373-117">Необходимо задать либо один, либо другой, но не оба варианта.</span><span class="sxs-lookup"><span data-stu-id="94373-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94373-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="94373-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94373-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="94373-119">Protocol specifications</span></span>

<span data-ttu-id="94373-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94373-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94373-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="94373-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94373-122">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94373-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94373-123">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="94373-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="94373-124">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94373-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94373-125">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="94373-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94373-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="94373-126">Header files</span></span>

<span data-ttu-id="94373-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="94373-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="94373-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="94373-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="94373-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="94373-129">Mapitags.h</span></span>
  
> <span data-ttu-id="94373-130">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="94373-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94373-131">См. также</span><span class="sxs-lookup"><span data-stu-id="94373-131">See also</span></span>



[<span data-ttu-id="94373-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="94373-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94373-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="94373-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94373-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="94373-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94373-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="94373-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

