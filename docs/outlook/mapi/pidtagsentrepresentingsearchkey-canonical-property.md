---
title: Каноническое свойство PidTagSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 954e63e5b669ffdd15bbc2548d75c4d420eaf88d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591046"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="8d176-103">Каноническое свойство PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="8d176-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="8d176-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d176-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d176-105">Содержит ключ поиска для обмена сообщениями пользователя, представленного отправителя.</span><span class="sxs-lookup"><span data-stu-id="8d176-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d176-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8d176-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d176-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="8d176-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="8d176-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8d176-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d176-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="8d176-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="8d176-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8d176-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d176-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8d176-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8d176-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8d176-112">Area:</span></span>  <br/> |<span data-ttu-id="8d176-113">Address</span><span class="sxs-lookup"><span data-stu-id="8d176-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d176-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8d176-114">Remarks</span></span>

<span data-ttu-id="8d176-115">Это свойство является одним из свойств адреса для обмена мгновенными сообщениями пользователя, который представлен отправителем.</span><span class="sxs-lookup"><span data-stu-id="8d176-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="8d176-116">Когда клиентское приложение отправляет сообщения от имени другого клиента, его следует устанавливать все свойства представленного отправителя значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="8d176-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="8d176-117">Обмена сообщениями при отправке на собственный имени обычно оставляет свойства представленного отправителя удалить.</span><span class="sxs-lookup"><span data-stu-id="8d176-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="8d176-118">Исходящие поставщика транспорта всегда необходимо оставить это свойство без изменений, если он имеет значение с клиента.</span><span class="sxs-lookup"><span data-stu-id="8d176-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="8d176-119">Если оно не установлено, поставщика транспорта должен установить значение **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) в исходящих копии сообщения и оставить неопределенные на локальной копии.</span><span class="sxs-lookup"><span data-stu-id="8d176-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d176-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8d176-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d176-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8d176-121">Protocol specifications</span></span>

<span data-ttu-id="8d176-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d176-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d176-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8d176-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d176-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d176-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d176-125">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8d176-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8d176-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d176-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d176-127">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="8d176-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8d176-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d176-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d176-129">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="8d176-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8d176-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d176-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d176-131">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="8d176-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8d176-132">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d176-132">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d176-133">Указывает, что свойства и операции, допустимые для учета объекты.</span><span class="sxs-lookup"><span data-stu-id="8d176-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="8d176-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d176-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d176-135">Задает свойства и операции, допустимые для списков рассылки контакта и личные.</span><span class="sxs-lookup"><span data-stu-id="8d176-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d176-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8d176-136">Header files</span></span>

<span data-ttu-id="8d176-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d176-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d176-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8d176-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d176-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d176-139">Mapitags.h</span></span>
  
> <span data-ttu-id="8d176-140">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="8d176-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d176-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8d176-141">See also</span></span>



[<span data-ttu-id="8d176-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d176-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d176-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d176-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d176-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8d176-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d176-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8d176-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

