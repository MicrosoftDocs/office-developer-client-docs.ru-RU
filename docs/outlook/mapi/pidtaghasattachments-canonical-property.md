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
ms.openlocfilehash: aca9c9f9c22fc4057f1650d1342492d2ed34653c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316130"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="30ec4-103">Каноническое свойство PidTagHasAttachments</span><span class="sxs-lookup"><span data-stu-id="30ec4-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="30ec4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30ec4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30ec4-105">Содержит TRUE, если сообщение содержит по крайней мере одно вложение.</span><span class="sxs-lookup"><span data-stu-id="30ec4-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30ec4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="30ec4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30ec4-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="30ec4-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="30ec4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="30ec4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30ec4-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="30ec4-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="30ec4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="30ec4-110">Data type:</span></span>  <br/> |<span data-ttu-id="30ec4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="30ec4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="30ec4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="30ec4-112">Area:</span></span>  <br/> |<span data-ttu-id="30ec4-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="30ec4-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30ec4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="30ec4-114">Remarks</span></span>

<span data-ttu-id="30ec4-115">Хранилище сообщений копирует **это свойство** из флага MSGFLAG_HASATTACH свойства [PR_MESSAGE_FLAGS (PidTagMessageFlags).](pidtagmessageflags-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="30ec4-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="30ec4-116">Клиентские приложения могут использовать **PR_HASATTACH** для сортировки вложений сообщений в просмотре сообщений.</span><span class="sxs-lookup"><span data-stu-id="30ec4-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="30ec4-117">Значение этого свойства обновляется методом [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="30ec4-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="30ec4-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="30ec4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30ec4-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="30ec4-119">Protocol specifications</span></span>

<span data-ttu-id="30ec4-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30ec4-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30ec4-121">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="30ec4-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30ec4-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="30ec4-122">Header files</span></span>

<span data-ttu-id="30ec4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30ec4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="30ec4-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="30ec4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="30ec4-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="30ec4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="30ec4-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="30ec4-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30ec4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="30ec4-127">See also</span></span>



[<span data-ttu-id="30ec4-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="30ec4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30ec4-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="30ec4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30ec4-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="30ec4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30ec4-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="30ec4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

