---
title: Каноническое свойство PidTagDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cd37d72d6a214f91e371b7126c90e3fda25cde2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578901"
---
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="0babd-103">Каноническое свойство PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="0babd-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="0babd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0babd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0babd-105">Содержит список ASCII отображаемые имена получателей скрытой копии (СК) сообщения, разделенные точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="0babd-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0babd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0babd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0babd-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="0babd-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="0babd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0babd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0babd-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="0babd-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="0babd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0babd-110">Data type:</span></span>  <br/> |<span data-ttu-id="0babd-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0babd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0babd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0babd-112">Area:</span></span>  <br/> |<span data-ttu-id="0babd-113">Message</span><span class="sxs-lookup"><span data-stu-id="0babd-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0babd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0babd-114">Remarks</span></span>

<span data-ttu-id="0babd-115">Хранилище сообщений вычисляет эти свойства сообщения объектов с помощью метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="0babd-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="0babd-116">Хранилище сообщений также поддерживает эти свойства, чтобы он всегда отражает последнее состояние сохраненного сообщения.</span><span class="sxs-lookup"><span data-stu-id="0babd-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="0babd-117">Значение синхронизируется во время каждого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="0babd-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="0babd-118">Если сообщение не имеет скрытой копии получателей, хранилища сообщений должны ответить на звонок [IMAPIProp::GetProps](imapiprop-getprops.md) с возвращаемое значение S_OK и пустая строка для **PR_DISPLAY_BCC**.</span><span class="sxs-lookup"><span data-stu-id="0babd-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="0babd-119">Из-за возможных необходимость локализации MAPI предоставляет эти руководства для всех получателей:</span><span class="sxs-lookup"><span data-stu-id="0babd-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="0babd-120">Все имена должна появиться возможность локализуется.</span><span class="sxs-lookup"><span data-stu-id="0babd-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="0babd-121">Точка с запятой должна быть символ, который используется для разделения имен в **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и свойства **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0babd-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="0babd-122">Точка с запятой не допускается в рамках получателей в MAPI.</span><span class="sxs-lookup"><span data-stu-id="0babd-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="0babd-123">Клиенты должны переведите каждой точкой с запятой, возникала в этом свойстве для локализованных разделитель перед внесением сведения свойство visible в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="0babd-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="0babd-124">При пересылке сообщения, клиенты не требуется переводить разделители в строке получателей скрытой копии.</span><span class="sxs-lookup"><span data-stu-id="0babd-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="0babd-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0babd-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0babd-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0babd-126">Protocol specifications</span></span>

<span data-ttu-id="0babd-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0babd-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0babd-128">Описывает формат сообщений, используемые для отправки сведения, относящиеся к общим папкам на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="0babd-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0babd-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0babd-129">Header files</span></span>

<span data-ttu-id="0babd-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0babd-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0babd-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0babd-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="0babd-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0babd-132">Mapitags.h</span></span>
  
> <span data-ttu-id="0babd-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0babd-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0babd-134">См. также</span><span class="sxs-lookup"><span data-stu-id="0babd-134">See also</span></span>



[<span data-ttu-id="0babd-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0babd-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0babd-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0babd-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0babd-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0babd-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0babd-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0babd-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

