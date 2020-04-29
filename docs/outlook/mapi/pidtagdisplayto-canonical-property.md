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
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360790"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="cfc4c-103">Каноническое свойство PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="cfc4c-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="cfc4c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfc4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfc4c-105">Содержит список отображаемых имен основных получателей сообщения (к), разделенных точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="cfc4c-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cfc4c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cfc4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cfc4c-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="cfc4c-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="cfc4c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cfc4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cfc4c-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="cfc4c-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="cfc4c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cfc4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="cfc4c-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cfc4c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cfc4c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cfc4c-112">Area:</span></span>  <br/> |<span data-ttu-id="cfc4c-113">Сообщение</span><span class="sxs-lookup"><span data-stu-id="cfc4c-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfc4c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cfc4c-114">Remarks</span></span>

<span data-ttu-id="cfc4c-115">Хранилище сообщений вычисляет эти свойства объектов сообщений с помощью метода [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="cfc4c-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="cfc4c-116">Кроме того, хранилище сообщений поддерживает эти свойства, чтобы всегда отображалось последнее сохраненное состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="cfc4c-117">Значение синхронизируется во время каждого вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="cfc4c-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="cfc4c-118">Если у сообщения нет основного получателя, то оно должно отвечать на вызов [IMAPIProp::::/PROPS](imapiprop-getprops.md) с возвращаемым значением S_OK и пустой строкой для **PR_DISPLAY_TO**.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="cfc4c-119">Из-за возможной локализации MAPI предоставляет следующие рекомендации для всех имен получателей:</span><span class="sxs-lookup"><span data-stu-id="cfc4c-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="cfc4c-120">Все имена должны быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="cfc4c-121">Точка с запятой должна быть символом, который используется для разделения имен в **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и свойства **PR_DISPLAY_TO** .</span><span class="sxs-lookup"><span data-stu-id="cfc4c-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="cfc4c-122">Точки с запятой не допускаются в именах получателей в MAPI.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="cfc4c-123">Клиенты должны перевести каждую точку с запятой, обнаруженную в **PR_DISPLAY_TO** и связанных свойствах, в локализованный символ разделителя перед отображением сведений в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="cfc4c-124">При пересылке сообщений клиентам не требуется переводить символы разделения на строку основного получателя.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="cfc4c-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cfc4c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cfc4c-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cfc4c-126">Protocol specifications</span></span>

<span data-ttu-id="cfc4c-127">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfc4c-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfc4c-128">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cfc4c-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cfc4c-129">Header files</span></span>

<span data-ttu-id="cfc4c-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="cfc4c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="cfc4c-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="cfc4c-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="cfc4c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="cfc4c-133">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="cfc4c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cfc4c-134">См. также</span><span class="sxs-lookup"><span data-stu-id="cfc4c-134">See also</span></span>



[<span data-ttu-id="cfc4c-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cfc4c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cfc4c-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="cfc4c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cfc4c-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cfc4c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cfc4c-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cfc4c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

