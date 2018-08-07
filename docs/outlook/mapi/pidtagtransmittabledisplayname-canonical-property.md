---
title: Каноническое свойство PidTagTransmittableDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96eaf6c3f9ddc9d4bf6bc16ddc28a6f38bc311f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812011"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="feb06-103">Каноническое свойство PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="feb06-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="feb06-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="feb06-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="feb06-105">Содержит отображаемое имя получателя в безопасной формы, которая не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="feb06-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="feb06-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="feb06-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="feb06-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="feb06-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="feb06-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="feb06-108">Identifier:</span></span>  <br/> |<span data-ttu-id="feb06-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="feb06-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="feb06-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="feb06-110">Data type:</span></span>  <br/> |<span data-ttu-id="feb06-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="feb06-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="feb06-112">Область:</span><span class="sxs-lookup"><span data-stu-id="feb06-112">Area:</span></span>  <br/> |<span data-ttu-id="feb06-113">Address</span><span class="sxs-lookup"><span data-stu-id="feb06-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="feb06-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="feb06-114">Remarks</span></span>

<span data-ttu-id="feb06-115">Эти свойства должны реализовывать все поставщиками адресной книги.</span><span class="sxs-lookup"><span data-stu-id="feb06-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="feb06-116">Они содержат версии отображаемое имя получателя, который передается с сообщением.</span><span class="sxs-lookup"><span data-stu-id="feb06-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="feb06-117">Для большинства поставщиками адресных книг эти свойства имеют совпадает со значением свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="feb06-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="feb06-118">Поставщики, которые не имеют безопасных отображаемое имя возврата PT_ERROR и MAPI изменения отображаемого имени, добавив имя в кавычки.</span><span class="sxs-lookup"><span data-stu-id="feb06-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="feb06-119">Это свойство можно использовать клиентское приложение для предотвращения изменения или «спуфинг» записей.</span><span class="sxs-lookup"><span data-stu-id="feb06-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="feb06-120">Пример спуфинг передает Иван Петров как (что Guy) Иван Петров.</span><span class="sxs-lookup"><span data-stu-id="feb06-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="feb06-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="feb06-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="feb06-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="feb06-122">Protocol specifications</span></span>

<span data-ttu-id="feb06-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feb06-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feb06-124">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="feb06-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="feb06-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feb06-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feb06-126">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="feb06-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="feb06-127">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feb06-127">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feb06-128">Обрабатывает клиентами с сервером интерфейса поставщика имя службы (NSPI).</span><span class="sxs-lookup"><span data-stu-id="feb06-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="feb06-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feb06-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feb06-130">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="feb06-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="feb06-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feb06-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feb06-132">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="feb06-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="feb06-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="feb06-133">Header files</span></span>

<span data-ttu-id="feb06-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="feb06-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="feb06-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="feb06-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="feb06-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="feb06-136">Mapitags.h</span></span>
  
> <span data-ttu-id="feb06-137">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="feb06-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="feb06-138">См. также</span><span class="sxs-lookup"><span data-stu-id="feb06-138">See also</span></span>



[<span data-ttu-id="feb06-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="feb06-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="feb06-140">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="feb06-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="feb06-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="feb06-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="feb06-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="feb06-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

