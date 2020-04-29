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
ms.openlocfilehash: 96a0b010a8ba26a0c1b0cb409f1aaabb308a1c01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356198"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="01db4-103">Каноническое свойство PidTagMessageToMe</span><span class="sxs-lookup"><span data-stu-id="01db4-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="01db4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01db4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01db4-105">Содержит значение TRUE, если этот пользователь обмена сообщениями является основным получателем (to) получателя этого сообщения и не входит в список рассылки.</span><span class="sxs-lookup"><span data-stu-id="01db4-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01db4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="01db4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01db4-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="01db4-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="01db4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="01db4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01db4-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="01db4-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="01db4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="01db4-110">Data type:</span></span>  <br/> |<span data-ttu-id="01db4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="01db4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="01db4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="01db4-112">Area:</span></span>  <br/> |<span data-ttu-id="01db4-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="01db4-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01db4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="01db4-114">Remarks</span></span>

<span data-ttu-id="01db4-115">Это свойство предоставляет удобный способ определения того, отображается ли имя пользователя явно в основном списке получателей, не проверяя все записи в списке.</span><span class="sxs-lookup"><span data-stu-id="01db4-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="01db4-116">Это свойство также помогает автоматически обрабатывать полученные сообщения на момент получения.</span><span class="sxs-lookup"><span data-stu-id="01db4-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="01db4-117">В параметре поставщика транспорта данное свойство содержит значение FALSE или не включается, если пользователь обмена сообщениями не указан непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="01db4-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="01db4-118">При доставке сообщений из расширения списка рассылки или с помощью скрытой копии это свойство не задается.</span><span class="sxs-lookup"><span data-stu-id="01db4-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="01db4-119">Получатель должен быть явно именованным.</span><span class="sxs-lookup"><span data-stu-id="01db4-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="01db4-120">Неотправленные сообщения обычно не задают **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) или это свойство.</span><span class="sxs-lookup"><span data-stu-id="01db4-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="01db4-121">Если они присутствуют в сообщениях, которые пользователь может получить доступ к общедоступным хранилищам сообщений, в личных хранилищах других пользователей, в файлах на диске или во всех полученных сообщениях, они обычно содержат значения, которые были заданы в последний раз, когда поставщик транспорта доставил сообщение.</span><span class="sxs-lookup"><span data-stu-id="01db4-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="01db4-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01db4-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01db4-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="01db4-123">Protocol specifications</span></span>

<span data-ttu-id="01db4-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01db4-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01db4-125">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="01db4-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01db4-126">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01db4-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01db4-127">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="01db4-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01db4-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="01db4-128">Header files</span></span>

<span data-ttu-id="01db4-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="01db4-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="01db4-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="01db4-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="01db4-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="01db4-131">Mapitags.h</span></span>
  
> <span data-ttu-id="01db4-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="01db4-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01db4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="01db4-133">See also</span></span>



[<span data-ttu-id="01db4-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01db4-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01db4-135">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="01db4-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01db4-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="01db4-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01db4-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="01db4-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

