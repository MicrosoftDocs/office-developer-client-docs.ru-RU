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
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="ac082-103">Каноническое свойство PidTagMessageCcMe</span><span class="sxs-lookup"><span data-stu-id="ac082-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="ac082-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac082-105">Содержит значение TRUE, если этот пользователь системы обмена сообщениями является особым именем получателя копии этого сообщения и не входит в список рассылки.</span><span class="sxs-lookup"><span data-stu-id="ac082-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac082-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ac082-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac082-107">ПР_МЕССАЖЕ_КК_МЕ</span><span class="sxs-lookup"><span data-stu-id="ac082-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="ac082-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ac082-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac082-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="ac082-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="ac082-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ac082-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac082-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ac082-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ac082-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ac082-112">Area:</span></span>  <br/> |<span data-ttu-id="ac082-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="ac082-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac082-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac082-114">Remarks</span></span>

<span data-ttu-id="ac082-115">Это свойство предоставляет удобный способ определения того, отображается ли имя пользователя явно в списке получателей копии, не проверяя все записи в списке.</span><span class="sxs-lookup"><span data-stu-id="ac082-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="ac082-116">Это свойство также помогает автоматически обрабатывать полученные сообщения на момент получения.</span><span class="sxs-lookup"><span data-stu-id="ac082-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="ac082-117">В параметре поставщика транспорта данное свойство содержит значение FALSE или не задано, если пользователь обмена сообщениями не указан непосредственно в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="ac082-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="ac082-118">При доставке сообщений из расширения списка рассылки или с помощью скрытой копии это свойство не задается.</span><span class="sxs-lookup"><span data-stu-id="ac082-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="ac082-119">Получатель должен быть явно именованным.</span><span class="sxs-lookup"><span data-stu-id="ac082-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="ac082-120">Неотправленные сообщения обычно не задают значение этого свойства, **пр_мессаже_реЦип_ме** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) или **пр_мессаже_то_ме** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ac082-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="ac082-121">Если они присутствуют в сообщениях, которые пользователь может получить доступ к хранилищам общедоступных сообщений, в частных хранилищах других пользователей, в файлах на диске или во всех полученных сообщениях, они обычно содержат значения, для которых они были заданы в последний раз, когда поставщик транспорта доставлено сообщение.</span><span class="sxs-lookup"><span data-stu-id="ac082-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ac082-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ac082-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac082-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ac082-123">Protocol specifications</span></span>

<span data-ttu-id="ac082-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac082-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac082-125">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ac082-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac082-126">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac082-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac082-127">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ac082-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac082-128">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="ac082-128">Header files</span></span>

<span data-ttu-id="ac082-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ac082-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac082-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ac082-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac082-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ac082-131">Mapitags.h</span></span>
  
> <span data-ttu-id="ac082-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="ac082-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac082-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ac082-133">See also</span></span>



[<span data-ttu-id="ac082-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ac082-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac082-135">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ac082-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac082-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ac082-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac082-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ac082-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

