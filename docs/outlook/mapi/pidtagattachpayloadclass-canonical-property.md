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
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="bcdb8-103">Каноническое свойство PidTagAttachPayloadClass</span><span class="sxs-lookup"><span data-stu-id="bcdb8-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="bcdb8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcdb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcdb8-105">Содержит значение поля заголовка MIME X — полезные данные.</span><span class="sxs-lookup"><span data-stu-id="bcdb8-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcdb8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bcdb8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcdb8-107">ПР_АТТАЧ_ПАЙЛОАД_КЛАСС, ПР_АТТАЧ_ПАЙЛОАД_КЛАСС_А, ПР_АТТАЧ_ПАЙЛОАД_КЛАСС_В</span><span class="sxs-lookup"><span data-stu-id="bcdb8-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="bcdb8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bcdb8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcdb8-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="bcdb8-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="bcdb8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bcdb8-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcdb8-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="bcdb8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bcdb8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bcdb8-112">Area:</span></span>  <br/> |<span data-ttu-id="bcdb8-113">Приложение Outlook</span><span class="sxs-lookup"><span data-stu-id="bcdb8-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcdb8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bcdb8-114">Remarks</span></span>

<span data-ttu-id="bcdb8-115">Чтобы задать значение этих свойств, клиенты MIME должны записать поле заголовка X — полезные данные в объект MIME, который будет анализироваться как вложение.</span><span class="sxs-lookup"><span data-stu-id="bcdb8-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="bcdb8-116">Считыватели MIME должны скопировать значение поля заголовка в значение соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="bcdb8-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="bcdb8-117">Средства чтения MIME должны игнорировать это поле заголовка, если оно отображается в объекте MIME, анализируемом в виде сообщения или текста сообщения, а не вложения.</span><span class="sxs-lookup"><span data-stu-id="bcdb8-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcdb8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bcdb8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcdb8-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bcdb8-119">Protocol specifications</span></span>

<span data-ttu-id="bcdb8-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcdb8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcdb8-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bcdb8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcdb8-122">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcdb8-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcdb8-123">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="bcdb8-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcdb8-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="bcdb8-124">Header files</span></span>

<span data-ttu-id="bcdb8-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="bcdb8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcdb8-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bcdb8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcdb8-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="bcdb8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bcdb8-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="bcdb8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcdb8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="bcdb8-129">See also</span></span>



[<span data-ttu-id="bcdb8-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bcdb8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcdb8-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="bcdb8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcdb8-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bcdb8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcdb8-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bcdb8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

