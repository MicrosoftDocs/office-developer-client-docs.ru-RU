---
title: Каноническое свойство PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389773"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="067c0-103">Каноническое свойство PidTagMessageCcMe</span><span class="sxs-lookup"><span data-stu-id="067c0-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="067c0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="067c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="067c0-105">Содержит значение TRUE, если этого обмена сообщениями пользователя специально с именем как получателей скрытой копии (CC) сообщения и не является частью списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="067c0-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="067c0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="067c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="067c0-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="067c0-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="067c0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="067c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="067c0-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="067c0-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="067c0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="067c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="067c0-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="067c0-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="067c0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="067c0-112">Area:</span></span>  <br/> |<span data-ttu-id="067c0-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="067c0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="067c0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="067c0-114">Remarks</span></span>

<span data-ttu-id="067c0-115">Это свойство обеспечивает удобный способ для определения, является ли имя пользователя отображается явным образом из списка получателей скрытой копии без проверки всех записей в списке.</span><span class="sxs-lookup"><span data-stu-id="067c0-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="067c0-116">Это свойство также используется для автоматической обработки сообщений, полученных во время поступления.</span><span class="sxs-lookup"><span data-stu-id="067c0-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="067c0-117">В параметр поставщика транспорта это свойство содержит значение FALSE или не задано, если обмена сообщениями пользователя отсутствует в списке непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="067c0-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="067c0-118">Доставка сообщений, связанные с обозначение скрытой копии или раскрытие списков рассылки не вызывает это свойство должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="067c0-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="067c0-119">Получатель должно быть задано явным образом.</span><span class="sxs-lookup"><span data-stu-id="067c0-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="067c0-120">Неотправленные сообщения, как правило, не задавайте это свойство, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) или **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="067c0-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="067c0-121">Если они имеются в сообщения, пользователь может получить доступ в хранилищах открытого сообщения, в частном другим пользователям хранилищ в файлы на диске, или встроенный других полученные сообщения, они как правило, содержат значения, к которым они были определенного последнего поставщика транспорта доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="067c0-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="067c0-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="067c0-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="067c0-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="067c0-123">Protocol specifications</span></span>

<span data-ttu-id="067c0-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="067c0-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="067c0-125">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="067c0-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="067c0-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="067c0-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="067c0-127">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="067c0-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="067c0-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="067c0-128">Header files</span></span>

<span data-ttu-id="067c0-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="067c0-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="067c0-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="067c0-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="067c0-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="067c0-131">Mapitags.h</span></span>
  
> <span data-ttu-id="067c0-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="067c0-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="067c0-133">См. также</span><span class="sxs-lookup"><span data-stu-id="067c0-133">See also</span></span>



[<span data-ttu-id="067c0-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="067c0-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="067c0-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="067c0-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="067c0-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="067c0-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="067c0-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="067c0-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

