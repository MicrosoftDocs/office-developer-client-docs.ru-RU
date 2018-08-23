---
title: Каноническое свойство PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 79a0307aaf8b91a50485234acc2e1cbdd2314b47
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574169"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="59c44-103">Каноническое свойство PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="59c44-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="59c44-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59c44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59c44-105">Содержит список отображаемые имена основной (по) получателей сообщения, разделенных точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="59c44-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59c44-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="59c44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59c44-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="59c44-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="59c44-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="59c44-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59c44-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="59c44-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="59c44-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="59c44-110">Data type:</span></span>  <br/> |<span data-ttu-id="59c44-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="59c44-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="59c44-112">Область:</span><span class="sxs-lookup"><span data-stu-id="59c44-112">Area:</span></span>  <br/> |<span data-ttu-id="59c44-113">Message</span><span class="sxs-lookup"><span data-stu-id="59c44-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59c44-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="59c44-114">Remarks</span></span>

<span data-ttu-id="59c44-115">Хранилище сообщений вычисляет эти свойства сообщения объектов с помощью метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="59c44-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="59c44-116">Хранилище сообщений также поддерживает эти свойства, чтобы он всегда отражает последнее состояние сохраненного сообщения.</span><span class="sxs-lookup"><span data-stu-id="59c44-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="59c44-117">Значение синхронизируется во время каждого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="59c44-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="59c44-118">Если сообщение не имеет основной получателей, хранилище сообщений должны отвечать на звонок [IMAPIProp::GetProps](imapiprop-getprops.md) с возвращаемое значение S_OK и пустая строка для **PR_DISPLAY_TO**.</span><span class="sxs-lookup"><span data-stu-id="59c44-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="59c44-119">Из-за возможных необходимость локализации MAPI предоставляет эти руководства для всех получателей:</span><span class="sxs-lookup"><span data-stu-id="59c44-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="59c44-120">Все имена должна появиться возможность локализуется.</span><span class="sxs-lookup"><span data-stu-id="59c44-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="59c44-121">Точка с запятой должна быть символ, который используется для разделения имен в **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и **PR_DISPLAY_TO** свойств.</span><span class="sxs-lookup"><span data-stu-id="59c44-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="59c44-122">Точка с запятой не допускается в рамках получателей в MAPI.</span><span class="sxs-lookup"><span data-stu-id="59c44-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="59c44-123">Клиенты следует перевести каждого сталкивались с запятой в **PR_DISPLAY_TO** и связанных с ними свойства для локализованных разделитель перед внесением сведения видны в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="59c44-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="59c44-124">При пересылке сообщения, клиенты не требуется переводить разделители в строке основной получателя.</span><span class="sxs-lookup"><span data-stu-id="59c44-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="59c44-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="59c44-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59c44-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="59c44-126">Protocol specifications</span></span>

<span data-ttu-id="59c44-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59c44-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59c44-128">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="59c44-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59c44-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="59c44-129">Header files</span></span>

<span data-ttu-id="59c44-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59c44-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="59c44-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="59c44-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="59c44-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="59c44-132">Mapitags.h</span></span>
  
> <span data-ttu-id="59c44-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="59c44-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59c44-134">См. также</span><span class="sxs-lookup"><span data-stu-id="59c44-134">See also</span></span>



[<span data-ttu-id="59c44-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="59c44-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59c44-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="59c44-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59c44-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="59c44-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59c44-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="59c44-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

