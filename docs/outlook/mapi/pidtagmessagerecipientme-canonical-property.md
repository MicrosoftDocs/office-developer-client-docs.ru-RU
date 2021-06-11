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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325622"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="8aa32-103">Каноническое свойство PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="8aa32-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="8aa32-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aa32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aa32-105">Содержит TRUE, если этот пользователь обмена сообщениями конкретно назван в качестве основного (To), углеродной копии (CC) или слепой копии углерода (BCC) получателя этого сообщения и не входит в список рассылки.</span><span class="sxs-lookup"><span data-stu-id="8aa32-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8aa32-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8aa32-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8aa32-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="8aa32-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="8aa32-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8aa32-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8aa32-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="8aa32-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="8aa32-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8aa32-110">Data type:</span></span>  <br/> |<span data-ttu-id="8aa32-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8aa32-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8aa32-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8aa32-112">Area:</span></span>  <br/> |<span data-ttu-id="8aa32-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="8aa32-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8aa32-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8aa32-114">Remarks</span></span>

<span data-ttu-id="8aa32-115">Это свойство позволяет определить, явно ли имя пользователя отображается в списке получателей без изучения всех записей в списке.</span><span class="sxs-lookup"><span data-stu-id="8aa32-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="8aa32-116">Это значение представляет  логическую операцию или эксплуатацию свойств **PR_MESSAGE_CC_ME** [(PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md)и **PR_MESSAGE_TO_ME** [(PidTagMessageToMe)](pidtagmessagetome-canonical-property.md)и сведений BCC (которые не отображаются в свойстве).</span><span class="sxs-lookup"><span data-stu-id="8aa32-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="8aa32-117">Это свойство помогает автоматизированной обработке полученных сообщений во время получения.</span><span class="sxs-lookup"><span data-stu-id="8aa32-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="8aa32-118">В варианте поставщика транспорта это свойство содержит FALSE или не включается, если пользователь обмена сообщениями не указан непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="8aa32-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="8aa32-119">Доставка сообщений в результате расширения списка рассылки не вызывает задатки этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8aa32-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="8aa32-120">Получатель должен быть явно назван.</span><span class="sxs-lookup"><span data-stu-id="8aa32-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="8aa32-121">Неуявные сообщения обычно не устанавливают это **свойство, PR_MESSAGE_CC_ME** или **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="8aa32-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="8aa32-122">Если они присутствуют в сообщениях, к которым пользователь может получить доступ в общедоступных хранилищах сообщений, в частных магазинах других пользователей, в файлах на диске или встроенных внутри других полученных сообщений, они обычно содержат значения, которым они были заданы при последнем доставке сообщения поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="8aa32-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8aa32-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8aa32-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8aa32-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8aa32-124">Protocol specifications</span></span>

<span data-ttu-id="8aa32-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8aa32-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8aa32-126">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="8aa32-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8aa32-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8aa32-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8aa32-128">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8aa32-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8aa32-129">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="8aa32-129">Header files</span></span>

<span data-ttu-id="8aa32-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8aa32-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="8aa32-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8aa32-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="8aa32-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8aa32-132">Mapitags.h</span></span>
  
> <span data-ttu-id="8aa32-133">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8aa32-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8aa32-134">См. также</span><span class="sxs-lookup"><span data-stu-id="8aa32-134">See also</span></span>



[<span data-ttu-id="8aa32-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8aa32-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8aa32-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8aa32-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8aa32-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8aa32-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8aa32-138">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="8aa32-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

