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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329738"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="a376c-103">Каноническое свойство PidTagMessageCcMe</span><span class="sxs-lookup"><span data-stu-id="a376c-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="a376c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a376c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a376c-105">Содержит TRUE, если этот пользователь обмена сообщениями конкретно назван получателем этого сообщения в качестве получателя копии углерода (CC) и не входит в список рассылки.</span><span class="sxs-lookup"><span data-stu-id="a376c-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a376c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a376c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a376c-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="a376c-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="a376c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a376c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a376c-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="a376c-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="a376c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a376c-110">Data type:</span></span>  <br/> |<span data-ttu-id="a376c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a376c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a376c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a376c-112">Area:</span></span>  <br/> |<span data-ttu-id="a376c-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="a376c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a376c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a376c-114">Remarks</span></span>

<span data-ttu-id="a376c-115">Это свойство предоставляет удобный способ определить, отображается ли имя пользователя явно в списке получателей копий углерода без изучения всех записей в списке.</span><span class="sxs-lookup"><span data-stu-id="a376c-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="a376c-116">Это свойство также помогает автоматизированной обработке полученных сообщений во время получения.</span><span class="sxs-lookup"><span data-stu-id="a376c-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="a376c-117">В варианте поставщика транспорта это свойство содержит FALSE или не заданной, если пользователь обмена сообщениями не указан непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="a376c-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="a376c-118">Доставка сообщений в результате расширения списка рассылки или в виде слепой копии углерода не вызывает задатки этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a376c-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="a376c-119">Получатель должен быть явно назван.</span><span class="sxs-lookup"><span data-stu-id="a376c-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="a376c-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** [(PidTagMessageRecipientMe),](pidtagmessagerecipientme-canonical-property.md)or **PR_MESSAGE_TO_ME** [(PidTagMessageToMe).](pidtagmessagetome-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a376c-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="a376c-121">Если они присутствуют в сообщениях, к которым пользователь может получить доступ в общедоступных хранилищах сообщений, в частных магазинах других пользователей, в файлах на диске или встроенных внутри других полученных сообщений, они обычно содержат значения, которым они были заданы при последнем доставке сообщения поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="a376c-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a376c-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a376c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a376c-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a376c-123">Protocol specifications</span></span>

<span data-ttu-id="a376c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a376c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a376c-125">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a376c-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a376c-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a376c-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a376c-127">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a376c-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a376c-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="a376c-128">Header files</span></span>

<span data-ttu-id="a376c-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a376c-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="a376c-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a376c-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="a376c-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a376c-131">Mapitags.h</span></span>
  
> <span data-ttu-id="a376c-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a376c-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a376c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="a376c-133">See also</span></span>



[<span data-ttu-id="a376c-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a376c-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a376c-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a376c-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a376c-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a376c-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a376c-137">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="a376c-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

