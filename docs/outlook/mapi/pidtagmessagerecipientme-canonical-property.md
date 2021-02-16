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
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="f7a94-103">Каноническое свойство PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="f7a94-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="f7a94-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7a94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7a94-105">Содержит true, если этот пользователь обмена сообщениями назван в качестве основного получателя (To), копии (CC) или неявного получателя копии (BCC) этого сообщения и не входит в список рассылки.</span><span class="sxs-lookup"><span data-stu-id="f7a94-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7a94-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f7a94-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7a94-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="f7a94-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="f7a94-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f7a94-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7a94-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="f7a94-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="f7a94-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f7a94-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7a94-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f7a94-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f7a94-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f7a94-112">Area:</span></span>  <br/> |<span data-ttu-id="f7a94-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="f7a94-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7a94-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7a94-114">Remarks</span></span>

<span data-ttu-id="f7a94-115">Это свойство предоставляет удобный способ определить, отображается ли имя пользователя явным образом в списке получателей без проверки всех записей в списке.</span><span class="sxs-lookup"><span data-stu-id="f7a94-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="f7a94-116">Значение представляет логическую операцию **OR** свойств **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md)и **PR_MESSAGE_TO_ME** ([PidTagMessageToMe),](pidtagmessagetome-canonical-property.md)а также сведения о BCC (которые иначе не отображаются в свойстве).</span><span class="sxs-lookup"><span data-stu-id="f7a94-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="f7a94-117">Это свойство помогает автоматизировать обработку полученных сообщений во время получения.</span><span class="sxs-lookup"><span data-stu-id="f7a94-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="f7a94-118">При указании поставщика транспорта это свойство либо содержит false, либо не включается, если пользователь сообщения не указан непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="f7a94-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="f7a94-119">При доставке сообщений, полученных в результате расширения списка рассылки, это свойство не задается.</span><span class="sxs-lookup"><span data-stu-id="f7a94-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="f7a94-120">Получатель должен иметь явное имя.</span><span class="sxs-lookup"><span data-stu-id="f7a94-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="f7a94-121">Как правило, в неавентных сообщениях это **свойство,** PR_MESSAGE_CC_ME или **PR_MESSAGE_TO_ME.**</span><span class="sxs-lookup"><span data-stu-id="f7a94-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="f7a94-122">Если они присутствуют в сообщениях, к которым пользователь может получить доступ в общедоступных хранилищах сообщений, в частных хранилищах других пользователей, в файлах на диске или внедренных в другие полученные сообщения, они обычно содержат значения, которыми они были заданы при последней доставке сообщения поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="f7a94-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f7a94-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f7a94-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7a94-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f7a94-124">Protocol specifications</span></span>

<span data-ttu-id="f7a94-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7a94-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7a94-126">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f7a94-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7a94-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7a94-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7a94-128">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f7a94-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7a94-129">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="f7a94-129">Header files</span></span>

<span data-ttu-id="f7a94-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7a94-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7a94-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f7a94-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7a94-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7a94-132">Mapitags.h</span></span>
  
> <span data-ttu-id="f7a94-133">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f7a94-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7a94-134">См. также</span><span class="sxs-lookup"><span data-stu-id="f7a94-134">See also</span></span>



[<span data-ttu-id="f7a94-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f7a94-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7a94-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f7a94-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7a94-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f7a94-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7a94-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f7a94-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

