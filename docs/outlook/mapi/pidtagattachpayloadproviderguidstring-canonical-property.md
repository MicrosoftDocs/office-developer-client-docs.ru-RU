---
title: Каноническое свойство PidTagAttachPayloadProviderGuidString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361105"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a><span data-ttu-id="5a0dc-103">Каноническое свойство PidTagAttachPayloadProviderGuidString</span><span class="sxs-lookup"><span data-stu-id="5a0dc-103">PidTagAttachPayloadProviderGuidString Canonical Property</span></span>

  
  
<span data-ttu-id="5a0dc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a0dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a0dc-105">Содержит значение поля заголовка MIME X — полезных данных provider – GUID.</span><span class="sxs-lookup"><span data-stu-id="5a0dc-105">Contains the value of a MIME X-Payload-Provider-Guid header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a0dc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5a0dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a0dc-107">ПР_АТТАЧ_ПАЙЛОАД_ПРОВ_ГУИД_СТР, ПР_АТТАЧ_ПАЙЛОАД_ПРОВ_ГУИД_СТР_А, ПР_АТТАЧ_ПАЙЛОАД_ПРОВ_ГУИД_СТР_В</span><span class="sxs-lookup"><span data-stu-id="5a0dc-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span></span>  <br/> |
|<span data-ttu-id="5a0dc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5a0dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a0dc-109">0x3719</span><span class="sxs-lookup"><span data-stu-id="5a0dc-109">0x3719</span></span>  <br/> |
|<span data-ttu-id="5a0dc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5a0dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a0dc-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="5a0dc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5a0dc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5a0dc-112">Area:</span></span>  <br/> |<span data-ttu-id="5a0dc-113">Приложение Outlook</span><span class="sxs-lookup"><span data-stu-id="5a0dc-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a0dc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a0dc-114">Remarks</span></span>

<span data-ttu-id="5a0dc-115">Чтобы задать значение этих свойств, клиенты MIME должны записать поле заголовка X — полезных данных provider – GUID в сущность MIME, которая будет анализироваться как вложение.</span><span class="sxs-lookup"><span data-stu-id="5a0dc-115">To set the value of these properties, MIME clients should write an X-Payload-Provider-Guid header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="5a0dc-116">Считыватели MIME должны скопировать значение поля заголовка в значение соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="5a0dc-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="5a0dc-117">Средства чтения MIME должны игнорировать это поле заголовка, если оно отображается в объекте MIME, анализируемом в виде сообщения или текста сообщения, а не вложения.</span><span class="sxs-lookup"><span data-stu-id="5a0dc-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a0dc-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5a0dc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a0dc-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5a0dc-119">Protocol specifications</span></span>

<span data-ttu-id="5a0dc-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a0dc-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a0dc-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5a0dc-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a0dc-122">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a0dc-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a0dc-123">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a0dc-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a0dc-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="5a0dc-124">Header files</span></span>

<span data-ttu-id="5a0dc-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5a0dc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a0dc-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5a0dc-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a0dc-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="5a0dc-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5a0dc-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="5a0dc-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a0dc-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5a0dc-129">See also</span></span>



[<span data-ttu-id="5a0dc-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a0dc-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a0dc-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5a0dc-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a0dc-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5a0dc-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a0dc-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5a0dc-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

