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
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="4d51c-103">Каноническое свойство PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="4d51c-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="4d51c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d51c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d51c-105">Содержит значение TRUE, если этот пользователь обмена сообщениями является основным (to), Recipient копия (CC) или скрытой копии (BCC) этого сообщения, но не является частью списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="4d51c-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d51c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4d51c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d51c-107">ПР_МЕССАЖЕ_РЕЦИП_МЕ</span><span class="sxs-lookup"><span data-stu-id="4d51c-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="4d51c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4d51c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d51c-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="4d51c-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="4d51c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4d51c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d51c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4d51c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4d51c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4d51c-112">Area:</span></span>  <br/> |<span data-ttu-id="4d51c-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="4d51c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d51c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d51c-114">Remarks</span></span>

<span data-ttu-id="4d51c-115">Это свойство предоставляет удобный способ определения того, отображается ли имя пользователя явно в списке получателей, не проверяя все записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4d51c-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="4d51c-116">Значение представляет логическую операцию **или** операцию свойств **пр_мессаже_кк_ме** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) и **пр_мессаже_то_ме** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), а также информацию скрытой копии (которая не отображается в элементе свойство).</span><span class="sxs-lookup"><span data-stu-id="4d51c-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="4d51c-117">Это свойство помогает автоматически обрабатывать полученные сообщения на момент получения.</span><span class="sxs-lookup"><span data-stu-id="4d51c-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="4d51c-118">В параметре поставщика транспорта данное свойство содержит значение FALSE или не включается, если пользователь обмена сообщениями не указан непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="4d51c-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="4d51c-119">Доставка сообщений, получаемых в результате расширения списка рассылки, не приводит к заданию этого свойства.</span><span class="sxs-lookup"><span data-stu-id="4d51c-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="4d51c-120">Получатель должен быть явно именованным.</span><span class="sxs-lookup"><span data-stu-id="4d51c-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="4d51c-121">Неотправленные сообщения обычно не задают значение этого свойства, **пр_мессаже_кк_ме**или **пр_мессаже_то_ме**.</span><span class="sxs-lookup"><span data-stu-id="4d51c-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="4d51c-122">Если они присутствуют в сообщениях, которые пользователь может получить доступ к хранилищам общедоступных сообщений, в частных хранилищах других пользователей, в файлах на диске или во всех полученных сообщениях, они обычно содержат значения, для которых они были заданы в последний раз, когда поставщик транспорта доставлено сообщение.</span><span class="sxs-lookup"><span data-stu-id="4d51c-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4d51c-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d51c-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d51c-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4d51c-124">Protocol specifications</span></span>

<span data-ttu-id="4d51c-125">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d51c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d51c-126">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4d51c-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d51c-127">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d51c-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d51c-128">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4d51c-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d51c-129">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="4d51c-129">Header files</span></span>

<span data-ttu-id="4d51c-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4d51c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d51c-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4d51c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d51c-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="4d51c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="4d51c-133">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="4d51c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d51c-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4d51c-134">See also</span></span>



[<span data-ttu-id="4d51c-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4d51c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d51c-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4d51c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d51c-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4d51c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d51c-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4d51c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

