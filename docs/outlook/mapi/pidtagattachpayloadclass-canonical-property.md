---
title: Каноническое свойство PidTagAttachPayloadClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6a84e51325fcb60c54c2f6b42af0c26a0efd3382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327239"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="bbbdf-103">Каноническое свойство PidTagAttachPayloadClass</span><span class="sxs-lookup"><span data-stu-id="bbbdf-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="bbbdf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbbdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbbdf-105">Содержит значение поля загона MIME X-Payload-Class.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bbbdf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bbbdf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbbdf-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="bbbdf-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="bbbdf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bbbdf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbbdf-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="bbbdf-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="bbbdf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bbbdf-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbbdf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bbbdf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bbbdf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bbbdf-112">Area:</span></span>  <br/> |<span data-ttu-id="bbbdf-113">Outlook приложение</span><span class="sxs-lookup"><span data-stu-id="bbbdf-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbbdf-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bbbdf-114">Remarks</span></span>

<span data-ttu-id="bbbdf-115">Чтобы установить значение этих свойств, клиенты MIME должны написать загон X-Payload-Class в объект MIME, который будет анализироваться как вложение.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="bbbdf-116">Читатели MIME должны скопировать это значение поля загона к значению соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="bbbdf-117">Читателям MIME следует игнорировать это поле заголовки, когда оно отображается в объекте MIME, которое анализируется как тело сообщения или сообщения, а не как вложение.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bbbdf-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bbbdf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbbdf-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bbbdf-119">Protocol specifications</span></span>

<span data-ttu-id="bbbdf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbbdf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbbdf-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bbbdf-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbbdf-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbbdf-123">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbbdf-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="bbbdf-124">Header files</span></span>

<span data-ttu-id="bbbdf-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbbdf-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbbdf-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbbdf-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bbbdf-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bbbdf-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbbdf-129">См. также</span><span class="sxs-lookup"><span data-stu-id="bbbdf-129">See also</span></span>



[<span data-ttu-id="bbbdf-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bbbdf-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbbdf-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bbbdf-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbbdf-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bbbdf-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbbdf-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="bbbdf-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

