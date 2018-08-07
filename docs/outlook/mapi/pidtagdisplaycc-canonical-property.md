---
title: Каноническое свойство PidTagDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6257557a8848c1abbaf8ceb15f719c50e4fec8c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811078"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="ecda4-103">Каноническое свойство PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="ecda4-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="ecda4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecda4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecda4-105">Содержит список ASCII отображаемые имена получателей скрытой копии (CC) сообщения, разделенные точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="ecda4-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecda4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ecda4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecda4-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="ecda4-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="ecda4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ecda4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecda4-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="ecda4-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="ecda4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ecda4-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecda4-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ecda4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ecda4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ecda4-112">Area:</span></span>  <br/> |<span data-ttu-id="ecda4-113">Message</span><span class="sxs-lookup"><span data-stu-id="ecda4-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecda4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ecda4-114">Remarks</span></span>

<span data-ttu-id="ecda4-115">Хранилище сообщений вычисляет эти свойства сообщения объектов с помощью метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="ecda4-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="ecda4-116">Хранилище сообщений также поддерживает эти свойства, чтобы он всегда отражает последнее состояние сохраненного сообщения.</span><span class="sxs-lookup"><span data-stu-id="ecda4-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="ecda4-117">Значение синхронизируется во время каждого вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="ecda4-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="ecda4-118">Если сообщение не имеет копии получателей, хранилище сообщений должны ответить на звонок [IMAPIProp::GetProps](imapiprop-getprops.md) с возвращаемое значение S_OK и пустая строка для этих свойств.</span><span class="sxs-lookup"><span data-stu-id="ecda4-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="ecda4-119">Из-за возможных необходимость локализации MAPI предоставляет эти руководства для всех получателей:</span><span class="sxs-lookup"><span data-stu-id="ecda4-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="ecda4-120">Все имена должна появиться возможность локализуется.</span><span class="sxs-lookup"><span data-stu-id="ecda4-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="ecda4-121">Точка с запятой должна быть символ, который используется для разделения имен в **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**и свойства **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ecda4-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="ecda4-122">Точка с запятой не допускается в рамках получателей в MAPI.</span><span class="sxs-lookup"><span data-stu-id="ecda4-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="ecda4-123">Клиенты должны переведите каждой точкой с запятой, возникала в этом свойстве для локализованных разделитель перед внесением сведения свойство visible в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ecda4-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="ecda4-124">При пересылке сообщения, клиенты не требуется переводить разделители в строке получателей скрытой копии.</span><span class="sxs-lookup"><span data-stu-id="ecda4-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="ecda4-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ecda4-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecda4-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ecda4-126">Protocol specifications</span></span>

<span data-ttu-id="ecda4-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecda4-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecda4-128">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ecda4-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecda4-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ecda4-129">Header files</span></span>

<span data-ttu-id="ecda4-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecda4-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecda4-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ecda4-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecda4-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ecda4-132">Mapitags.h</span></span>
  
> <span data-ttu-id="ecda4-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ecda4-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecda4-134">См. также</span><span class="sxs-lookup"><span data-stu-id="ecda4-134">See also</span></span>



[<span data-ttu-id="ecda4-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ecda4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecda4-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ecda4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecda4-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ecda4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecda4-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ecda4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

