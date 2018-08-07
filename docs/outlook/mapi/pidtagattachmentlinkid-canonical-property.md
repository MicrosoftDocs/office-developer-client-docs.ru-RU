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
ms.openlocfilehash: e467fb7c05a647265d007429930ee522fd77b2fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810853"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="5f659-103">Каноническое свойство PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="5f659-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="5f659-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f659-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f659-105">Указывает тип объекта сообщения, с которым связан этот вложения.</span><span class="sxs-lookup"><span data-stu-id="5f659-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f659-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5f659-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f659-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="5f659-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="5f659-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5f659-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f659-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="5f659-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="5f659-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5f659-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f659-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5f659-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5f659-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5f659-112">Area:</span></span>  <br/> |<span data-ttu-id="5f659-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="5f659-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f659-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5f659-114">Remarks</span></span>

<span data-ttu-id="5f659-115">Должен иметь значение 0, если не переопределено других протоколов, расширение сообщения и вложения объектов протокол как было указано в [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5f659-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f659-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5f659-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f659-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5f659-117">Protocol specifications</span></span>

<span data-ttu-id="5f659-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f659-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f659-119">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="5f659-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5f659-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f659-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f659-121">Задает свойства и операции, допустимые для объектов журнала.</span><span class="sxs-lookup"><span data-stu-id="5f659-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="5f659-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f659-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f659-123">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="5f659-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f659-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5f659-124">Header files</span></span>

<span data-ttu-id="5f659-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f659-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f659-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5f659-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f659-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f659-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5f659-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5f659-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f659-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5f659-129">See also</span></span>



[<span data-ttu-id="5f659-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5f659-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f659-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5f659-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f659-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5f659-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f659-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5f659-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

