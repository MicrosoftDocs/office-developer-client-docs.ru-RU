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
ms.openlocfilehash: cef412d212bf29cfd1a1d5c4b2911440fae6a15e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810874"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="55c9b-103">Каноническое свойство PidTagAttachPayloadClass</span><span class="sxs-lookup"><span data-stu-id="55c9b-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="55c9b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55c9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55c9b-105">Содержит значение поля заголовка X-полезной нагрузки-класса MIME.</span><span class="sxs-lookup"><span data-stu-id="55c9b-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55c9b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="55c9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55c9b-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="55c9b-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="55c9b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="55c9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55c9b-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="55c9b-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="55c9b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="55c9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="55c9b-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="55c9b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="55c9b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="55c9b-112">Area:</span></span>  <br/> |<span data-ttu-id="55c9b-113">Приложения Outlook</span><span class="sxs-lookup"><span data-stu-id="55c9b-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55c9b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="55c9b-114">Remarks</span></span>

<span data-ttu-id="55c9b-115">Чтобы задать значения этих свойств, клиенты MIME указывайте поле заголовка X-полезной нагрузки-класс MIME лицо, которое будет анализироваться как вложение.</span><span class="sxs-lookup"><span data-stu-id="55c9b-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="55c9b-116">Читатели MIME, должен скопировать это значение поля заголовка на значение соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="55c9b-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="55c9b-117">Читатели MIME следует игнорировать это поле заголовка при его отображении в сущности MIME, анализируется как сообщение или текст сообщения, а не как вложение.</span><span class="sxs-lookup"><span data-stu-id="55c9b-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55c9b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="55c9b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55c9b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="55c9b-119">Protocol specifications</span></span>

<span data-ttu-id="55c9b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c9b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c9b-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="55c9b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55c9b-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c9b-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c9b-123">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="55c9b-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55c9b-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="55c9b-124">Header files</span></span>

<span data-ttu-id="55c9b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55c9b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="55c9b-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="55c9b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="55c9b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55c9b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="55c9b-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="55c9b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55c9b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="55c9b-129">See also</span></span>



[<span data-ttu-id="55c9b-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="55c9b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55c9b-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="55c9b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55c9b-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="55c9b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55c9b-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="55c9b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

