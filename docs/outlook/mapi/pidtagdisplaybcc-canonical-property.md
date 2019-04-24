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
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="88da2-103">Каноническое свойство PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="88da2-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="88da2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88da2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88da2-105">Содержит список отображаемых имен получателей скрытой копии (BCC), разделенных точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="88da2-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88da2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="88da2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88da2-107">ПР_ДИСПЛАЙ_БКК, ПР_ДИСПЛАЙ_БКК_А, ПР_ДИСПЛАЙ_БКК_В</span><span class="sxs-lookup"><span data-stu-id="88da2-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="88da2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="88da2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="88da2-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="88da2-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="88da2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="88da2-110">Data type:</span></span>  <br/> |<span data-ttu-id="88da2-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="88da2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="88da2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="88da2-112">Area:</span></span>  <br/> |<span data-ttu-id="88da2-113">Сообщение</span><span class="sxs-lookup"><span data-stu-id="88da2-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88da2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="88da2-114">Remarks</span></span>

<span data-ttu-id="88da2-115">Хранилище сообщений вычисляет эти свойства объектов сообщений с помощью метода [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="88da2-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="88da2-116">Кроме того, хранилище сообщений поддерживает эти свойства, чтобы всегда отображалось последнее сохраненное состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="88da2-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="88da2-117">Значение синхронизируется во время каждого вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="88da2-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="88da2-118">Если у сообщения нет получателей скрытой копии, то хранилище сообщений должно отвечать на вызов [IMAPIProp::](imapiprop-getprops.md) /PROPS с возвращаемым значением S_OK и пустой строкой для **пр_дисплай_бкк**.</span><span class="sxs-lookup"><span data-stu-id="88da2-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="88da2-119">Из-за возможной локализации MAPI предоставляет следующие рекомендации для всех имен получателей:</span><span class="sxs-lookup"><span data-stu-id="88da2-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="88da2-120">Все имена должны быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="88da2-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="88da2-121">Точка с запятой должна быть символом, который используется для разделения имен в свойствах **пр_дисплай_бкк**, **пр_дисплай_кк** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и **пр_дисплай_то** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="88da2-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="88da2-122">Точки с запятой не допускаются в именах получателей в MAPI.</span><span class="sxs-lookup"><span data-stu-id="88da2-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="88da2-123">Клиенты должны перевести каждую точку с запятой, обнаруженную в этом свойстве, на локализованный символ разделителя, прежде чем сделать сведения о свойстве видимыми в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="88da2-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="88da2-124">При пересылке сообщений клиентам не нужно преобразовывать символы разделения в строку получателей скрытой копии.</span><span class="sxs-lookup"><span data-stu-id="88da2-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="88da2-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="88da2-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88da2-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="88da2-126">Protocol specifications</span></span>

<span data-ttu-id="88da2-127">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88da2-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88da2-128">Описывает формат сообщений, используемых для отправки сведений, связанных с общими папками на клиенте.</span><span class="sxs-lookup"><span data-stu-id="88da2-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88da2-129">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="88da2-129">Header files</span></span>

<span data-ttu-id="88da2-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="88da2-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="88da2-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="88da2-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="88da2-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="88da2-132">Mapitags.h</span></span>
  
> <span data-ttu-id="88da2-133">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="88da2-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88da2-134">См. также</span><span class="sxs-lookup"><span data-stu-id="88da2-134">See also</span></span>



[<span data-ttu-id="88da2-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="88da2-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88da2-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="88da2-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88da2-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="88da2-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88da2-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="88da2-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

