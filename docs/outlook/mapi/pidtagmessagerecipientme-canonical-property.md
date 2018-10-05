---
title: Каноническое свойство PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382465"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="e1c1d-103">Каноническое свойство PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="e1c1d-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="e1c1d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1c1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1c1d-105">Содержит значение TRUE, если этого обмена сообщениями пользователя специально с именем как основной (по), скрытой копии (CC) или получателей скрытой копии (СК) сообщения и не является частью списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1c1d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e1c1d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1c1d-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="e1c1d-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="e1c1d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e1c1d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1c1d-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="e1c1d-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="e1c1d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e1c1d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1c1d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e1c1d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e1c1d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e1c1d-112">Area:</span></span>  <br/> |<span data-ttu-id="e1c1d-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="e1c1d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1c1d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e1c1d-114">Remarks</span></span>

<span data-ttu-id="e1c1d-115">Это свойство обеспечивает удобный способ для определения, является ли имя пользователя отображается явным образом в список получателей, без проверки всех записей в списке.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="e1c1d-116">Представляет значение логической операции **или** свойства **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) и **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) и сведения о скрытой копии (которая в противном случае не отображаются в свойство).</span><span class="sxs-lookup"><span data-stu-id="e1c1d-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="e1c1d-117">Это свойство используется для автоматической обработки сообщений, полученных во время поступления.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="e1c1d-118">В параметр поставщика транспорта это свойство содержит значение FALSE или не включена, если обмена сообщениями пользователя отсутствует в списке непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="e1c1d-119">Доставка сообщений, результаты из раскрытие списков рассылки не вызывает это свойство должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="e1c1d-120">Получатель должно быть задано явным образом.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="e1c1d-121">Неотправленные сообщения обычно не задавайте это свойство, **PR_MESSAGE_CC_ME**или **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="e1c1d-122">Если они имеются в сообщения, пользователь может получить доступ в хранилищах открытого сообщения, в частном другим пользователям хранилищ в файлы на диске, или встроенный других полученные сообщения, они как правило, содержат значения, к которым они были определенного последнего поставщика транспорта доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e1c1d-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1c1d-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1c1d-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e1c1d-124">Protocol specifications</span></span>

<span data-ttu-id="e1c1d-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1c1d-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1c1d-126">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1c1d-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1c1d-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1c1d-128">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1c1d-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e1c1d-129">Header files</span></span>

<span data-ttu-id="e1c1d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1c1d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1c1d-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1c1d-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1c1d-132">Mapitags.h</span></span>
  
> <span data-ttu-id="e1c1d-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e1c1d-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1c1d-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e1c1d-134">See also</span></span>



[<span data-ttu-id="e1c1d-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1c1d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1c1d-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1c1d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1c1d-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e1c1d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1c1d-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e1c1d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

