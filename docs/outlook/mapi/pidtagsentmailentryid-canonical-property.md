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
ms.openlocfilehash: 869f7f0bb4ea5e7222201083cb6d41754d241396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811897"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="58e8a-103">Каноническое свойство PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="58e8a-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="58e8a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58e8a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58e8a-105">Содержит идентификатор записи к папке, куда необходимо переместить сообщение после отправки.</span><span class="sxs-lookup"><span data-stu-id="58e8a-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58e8a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="58e8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58e8a-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="58e8a-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="58e8a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="58e8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58e8a-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="58e8a-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="58e8a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="58e8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="58e8a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="58e8a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="58e8a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="58e8a-112">Area:</span></span>  <br/> |<span data-ttu-id="58e8a-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="58e8a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58e8a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="58e8a-114">Remarks</span></span>

<span data-ttu-id="58e8a-115">Это свойство часто копируются из свойства **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)), standard папку Отправленные клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="58e8a-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="58e8a-116">Клиентское приложение использует это свойство со свойством **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) для управления, что происходит после ее отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="58e8a-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="58e8a-117">Одно или другое должен быть набор, но не оба.</span><span class="sxs-lookup"><span data-stu-id="58e8a-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="58e8a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="58e8a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58e8a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="58e8a-119">Protocol specifications</span></span>

<span data-ttu-id="58e8a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58e8a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58e8a-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="58e8a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58e8a-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58e8a-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58e8a-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="58e8a-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="58e8a-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58e8a-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58e8a-125">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="58e8a-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58e8a-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="58e8a-126">Header files</span></span>

<span data-ttu-id="58e8a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58e8a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="58e8a-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="58e8a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="58e8a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="58e8a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="58e8a-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="58e8a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58e8a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="58e8a-131">See also</span></span>



[<span data-ttu-id="58e8a-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="58e8a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58e8a-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="58e8a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58e8a-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="58e8a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58e8a-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="58e8a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

