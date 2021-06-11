---
title: Каноническое свойство PidTagAttachmentLinkId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentLinkId
api_type:
- HeaderDef
ms.assetid: 5d0daae7-248d-459f-9d96-cb949b86f590
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 623b4195b7128667b9aaa6bc97d03c21d62c690a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345698"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="50f37-103">Каноническое свойство PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="50f37-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="50f37-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50f37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50f37-105">Указывает тип объекта Message, к которому связано это вложение.</span><span class="sxs-lookup"><span data-stu-id="50f37-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50f37-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="50f37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50f37-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="50f37-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="50f37-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="50f37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50f37-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="50f37-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="50f37-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="50f37-110">Data type:</span></span>  <br/> |<span data-ttu-id="50f37-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="50f37-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="50f37-112">Область:</span><span class="sxs-lookup"><span data-stu-id="50f37-112">Area:</span></span>  <br/> |<span data-ttu-id="50f37-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="50f37-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50f37-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="50f37-114">Remarks</span></span>

<span data-ttu-id="50f37-115">Должно быть 0, если не переопределяться другими протоколами, которые расширяют протокол объектов сообщения и вложений, как отмечено [в [MS-OXCMSG].](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50f37-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50f37-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="50f37-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50f37-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="50f37-117">Protocol specifications</span></span>

<span data-ttu-id="50f37-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50f37-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50f37-119">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="50f37-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="50f37-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50f37-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50f37-121">Указывает свойства и операции, допустимые для объектов журнала.</span><span class="sxs-lookup"><span data-stu-id="50f37-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="50f37-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50f37-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50f37-123">Указывает свойства и модель взаимодействия для электронной почты и других напоминаний объектов.</span><span class="sxs-lookup"><span data-stu-id="50f37-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50f37-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="50f37-124">Header files</span></span>

<span data-ttu-id="50f37-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50f37-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="50f37-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="50f37-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="50f37-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="50f37-127">Mapitags.h</span></span>
  
> <span data-ttu-id="50f37-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="50f37-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50f37-129">См. также</span><span class="sxs-lookup"><span data-stu-id="50f37-129">See also</span></span>



[<span data-ttu-id="50f37-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="50f37-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50f37-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="50f37-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50f37-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="50f37-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50f37-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="50f37-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

