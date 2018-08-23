---
title: Каноническое свойство PidTagMessageToMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 51a8f1768f9b4ed859989058c66044c807068386
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583934"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="d6491-103">Каноническое свойство PidTagMessageToMe</span><span class="sxs-lookup"><span data-stu-id="d6491-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="d6491-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6491-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6491-105">Содержит значение TRUE, если этого обмена сообщениями пользователя специально с именем как основной (получатель сообщения по) и не является частью списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="d6491-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6491-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d6491-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6491-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="d6491-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="d6491-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d6491-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6491-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="d6491-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="d6491-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d6491-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6491-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d6491-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d6491-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d6491-112">Area:</span></span>  <br/> |<span data-ttu-id="d6491-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="d6491-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6491-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d6491-114">Remarks</span></span>

<span data-ttu-id="d6491-115">Это свойство обеспечивает удобный способ для определения, является ли имя пользователя отображается явным образом в основной список получателей, без проверки всех записей в списке.</span><span class="sxs-lookup"><span data-stu-id="d6491-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="d6491-116">Это свойство также используется для автоматической обработки сообщений, полученных во время поступления.</span><span class="sxs-lookup"><span data-stu-id="d6491-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="d6491-117">В параметр поставщика транспорта это свойство содержит значение FALSE или не включена, если обмена сообщениями пользователя отсутствует в списке непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="d6491-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="d6491-118">Доставка сообщений, связанные с обозначение скрытой копии или раскрытие списков рассылки не вызывает это свойство должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="d6491-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="d6491-119">Получатель должно быть задано явным образом.</span><span class="sxs-lookup"><span data-stu-id="d6491-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="d6491-120">Неотправленные сообщения обычно не задан **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) или это свойство.</span><span class="sxs-lookup"><span data-stu-id="d6491-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="d6491-121">Если они имеются в сообщения, пользователь может получить доступ в хранилищах открытого сообщения, в частном другим пользователям хранилищ в файлы на диске, или встроенный других полученные сообщения, они как правило, содержат значения, к которым они были определенного последнего поставщика транспорта доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="d6491-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d6491-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d6491-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6491-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d6491-123">Protocol specifications</span></span>

<span data-ttu-id="d6491-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6491-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6491-125">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d6491-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6491-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6491-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6491-127">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d6491-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6491-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d6491-128">Header files</span></span>

<span data-ttu-id="d6491-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6491-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6491-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d6491-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6491-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6491-131">Mapitags.h</span></span>
  
> <span data-ttu-id="d6491-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d6491-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6491-133">См. также</span><span class="sxs-lookup"><span data-stu-id="d6491-133">See also</span></span>



[<span data-ttu-id="d6491-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d6491-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6491-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d6491-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6491-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d6491-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6491-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d6491-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

