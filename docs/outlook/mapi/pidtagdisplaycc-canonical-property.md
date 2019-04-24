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
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360811"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="c9b9f-103">Каноническое свойство PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="c9b9f-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="c9b9f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9b9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9b9f-105">Содержит список отображаемых имен всех получателей сообщений копии (CC), разделенных точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="c9b9f-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9b9f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c9b9f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9b9f-107">ПР_ДИСПЛАЙ_КК, ПР_ДИСПЛАЙ_КК_А, ПР_ДИСПЛАЙ_КК_В</span><span class="sxs-lookup"><span data-stu-id="c9b9f-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="c9b9f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c9b9f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9b9f-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="c9b9f-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="c9b9f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c9b9f-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9b9f-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="c9b9f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c9b9f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c9b9f-112">Area:</span></span>  <br/> |<span data-ttu-id="c9b9f-113">Сообщение</span><span class="sxs-lookup"><span data-stu-id="c9b9f-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9b9f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9b9f-114">Remarks</span></span>

<span data-ttu-id="c9b9f-115">Хранилище сообщений вычисляет эти свойства объектов сообщений с помощью метода [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="c9b9f-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="c9b9f-116">Кроме того, хранилище сообщений поддерживает эти свойства, чтобы всегда отображалось последнее сохраненное состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="c9b9f-117">Значение синхронизируется во время каждого вызова [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="c9b9f-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="c9b9f-118">Если у сообщения нет получателей копии, то хранилище сообщений должно отвечать на вызов [IMAPIProp::](imapiprop-getprops.md) /PROPS со значением S_OK и пустой строкой для этих свойств.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="c9b9f-119">Из-за возможной локализации MAPI предоставляет следующие рекомендации для всех имен получателей:</span><span class="sxs-lookup"><span data-stu-id="c9b9f-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="c9b9f-120">Все имена должны быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="c9b9f-121">Точка с запятой должна быть символом, который используется для разделения имен в свойствах **пр_дисплай_бкк** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **пр_дисплай_кк**и **пр_дисплай_то** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c9b9f-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="c9b9f-122">Точки с запятой не допускаются в именах получателей в MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="c9b9f-123">Клиенты должны перевести каждую точку с запятой, обнаруженную в этом свойстве, на локализованный символ разделителя, прежде чем сделать сведения о свойстве видимыми в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="c9b9f-124">При пересылке сообщений клиентам не нужно преобразовывать символы разделения в строку получателей копии копии.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="c9b9f-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c9b9f-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9b9f-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c9b9f-126">Protocol specifications</span></span>

<span data-ttu-id="c9b9f-127">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9b9f-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9b9f-128">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9b9f-129">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="c9b9f-129">Header files</span></span>

<span data-ttu-id="c9b9f-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c9b9f-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9b9f-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9b9f-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c9b9f-132">Mapitags.h</span></span>
  
> <span data-ttu-id="c9b9f-133">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c9b9f-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9b9f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c9b9f-134">See also</span></span>



[<span data-ttu-id="c9b9f-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b9f-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9b9f-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b9f-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9b9f-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b9f-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9b9f-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c9b9f-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

