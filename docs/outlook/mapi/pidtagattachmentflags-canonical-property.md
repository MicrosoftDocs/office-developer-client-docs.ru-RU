---
title: Каноническое свойство PidTagAttachmentFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345803"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="7502d-103">Каноническое свойство PidTagAttachmentFlags</span><span class="sxs-lookup"><span data-stu-id="7502d-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="7502d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7502d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7502d-105">Указывает специальную обработку для этого объекта Attachment.</span><span class="sxs-lookup"><span data-stu-id="7502d-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7502d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7502d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7502d-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7502d-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="7502d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7502d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7502d-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="7502d-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="7502d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7502d-110">Data type:</span></span>  <br/> |<span data-ttu-id="7502d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7502d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7502d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7502d-112">Area:</span></span>  <br/> |<span data-ttu-id="7502d-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="7502d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7502d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7502d-114">Remarks</span></span>

<span data-ttu-id="7502d-115">Должен быть 0x00000000, если не переопределяется другими протоколами, которые расширяют протокол message и Attachment Object Protocol, как отмечено [в [MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7502d-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7502d-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7502d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7502d-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7502d-117">Protocol specifications</span></span>

<span data-ttu-id="7502d-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7502d-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7502d-119">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="7502d-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7502d-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7502d-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7502d-121">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7502d-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7502d-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="7502d-122">Header files</span></span>

<span data-ttu-id="7502d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7502d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7502d-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7502d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7502d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7502d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7502d-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7502d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7502d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7502d-127">See also</span></span>



[<span data-ttu-id="7502d-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7502d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7502d-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7502d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7502d-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7502d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7502d-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7502d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

