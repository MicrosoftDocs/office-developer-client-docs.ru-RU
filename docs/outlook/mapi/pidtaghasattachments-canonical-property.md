---
title: Каноническое свойство PidTagHasAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 505f9bb80c86b956cd920348f2120f7fc8494d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587504"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="64b90-103">Каноническое свойство PidTagHasAttachments</span><span class="sxs-lookup"><span data-stu-id="64b90-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="64b90-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64b90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64b90-105">Содержит значение TRUE, если сообщение содержит по крайней мере одного вложения.</span><span class="sxs-lookup"><span data-stu-id="64b90-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64b90-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="64b90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64b90-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="64b90-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="64b90-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="64b90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64b90-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="64b90-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="64b90-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="64b90-110">Data type:</span></span>  <br/> |<span data-ttu-id="64b90-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="64b90-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="64b90-112">Область:</span><span class="sxs-lookup"><span data-stu-id="64b90-112">Area:</span></span>  <br/> |<span data-ttu-id="64b90-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="64b90-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64b90-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="64b90-114">Remarks</span></span>

<span data-ttu-id="64b90-115">Это свойство копирует хранилища сообщений из флаг **MSGFLAG_HASATTACH** свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64b90-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="64b90-116">Клиентское приложение затем можно использовать **PR_HASATTACH** для сортировки вложений сообщений в средстве просмотра сообщений.</span><span class="sxs-lookup"><span data-stu-id="64b90-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="64b90-117">Значение этого свойства обновляются с помощью метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="64b90-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="64b90-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="64b90-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64b90-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="64b90-119">Protocol specifications</span></span>

<span data-ttu-id="64b90-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64b90-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64b90-121">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="64b90-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64b90-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="64b90-122">Header files</span></span>

<span data-ttu-id="64b90-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64b90-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="64b90-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="64b90-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="64b90-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64b90-125">Mapitags.h</span></span>
  
> <span data-ttu-id="64b90-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="64b90-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64b90-127">См. также</span><span class="sxs-lookup"><span data-stu-id="64b90-127">See also</span></span>



[<span data-ttu-id="64b90-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="64b90-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64b90-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="64b90-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64b90-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="64b90-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64b90-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="64b90-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

