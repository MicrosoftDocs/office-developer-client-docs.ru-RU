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
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360818"
---
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="be20d-103">Каноническое свойство PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="be20d-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="be20d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be20d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be20d-105">Содержит список ASCII отображаемого имени всех получателей сообщений с незрячими копиями (BCC), разделенных точками с забоем (;).</span><span class="sxs-lookup"><span data-stu-id="be20d-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be20d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="be20d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be20d-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="be20d-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="be20d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="be20d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be20d-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="be20d-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="be20d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="be20d-110">Data type:</span></span>  <br/> |<span data-ttu-id="be20d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be20d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="be20d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="be20d-112">Area:</span></span>  <br/> |<span data-ttu-id="be20d-113">Сообщение</span><span class="sxs-lookup"><span data-stu-id="be20d-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be20d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="be20d-114">Remarks</span></span>

<span data-ttu-id="be20d-115">Хранилище сообщений вычисляет эти свойства объектов сообщений с помощью метода [IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="be20d-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="be20d-116">Хранилище сообщений также поддерживает эти свойства, чтобы оно всегда отображало последнее сохраненное состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="be20d-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="be20d-117">Значение синхронизируется во время каждого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="be20d-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="be20d-118">Если сообщение не имеет получателей с незрячими копиями, хранилище сообщений должно ответить на вызов [IMAPIProp::GetProps](imapiprop-getprops.md) с возвращаемым значением S_OK и пустой строкой для **PR_DISPLAY_BCC.**</span><span class="sxs-lookup"><span data-stu-id="be20d-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="be20d-119">В связи с возможной необходимостью локализации MAPI предоставляет следующие рекомендации для всех имен получателей:</span><span class="sxs-lookup"><span data-stu-id="be20d-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="be20d-120">Все имена должны быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="be20d-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="be20d-121">Точка с запоем должна быть символом, используемым для разных имен в свойствах **PR_DISPLAY_BCC,** **PR_DISPLAY_CC** ([PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)и **PR_DISPLAY_TO** ([PidTagDisplayTo).](pidtagdisplayto-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="be20d-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="be20d-122">В MAPI имена получателей не допускаются.</span><span class="sxs-lookup"><span data-stu-id="be20d-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="be20d-123">Перед тем как сделать сведения о свойстве видимыми в пользовательском интерфейсе, клиенты должны перевести все точки с заданной точки с заданной точки в этом свойстве в локализованный знак сепаратора.</span><span class="sxs-lookup"><span data-stu-id="be20d-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="be20d-124">При перенаправлении сообщений клиентам не нужно переводить знаки в строке получателя с незрячими копиями.</span><span class="sxs-lookup"><span data-stu-id="be20d-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="be20d-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="be20d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be20d-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="be20d-126">Protocol specifications</span></span>

<span data-ttu-id="be20d-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be20d-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be20d-128">Описывает формат сообщений, используемых для отправки сведений, связанных с папками общего доступа на клиенте.</span><span class="sxs-lookup"><span data-stu-id="be20d-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be20d-129">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="be20d-129">Header files</span></span>

<span data-ttu-id="be20d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be20d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="be20d-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="be20d-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="be20d-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be20d-132">Mapitags.h</span></span>
  
> <span data-ttu-id="be20d-133">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="be20d-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be20d-134">См. также</span><span class="sxs-lookup"><span data-stu-id="be20d-134">See also</span></span>



[<span data-ttu-id="be20d-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be20d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be20d-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be20d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be20d-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="be20d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be20d-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="be20d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

