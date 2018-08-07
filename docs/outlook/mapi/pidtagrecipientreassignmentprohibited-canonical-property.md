---
title: Каноническое свойство PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811668"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="14ca3-103">Каноническое свойство PidTagRecipientReassignmentProhibited</span><span class="sxs-lookup"><span data-stu-id="14ca3-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="14ca3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14ca3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14ca3-105">Запрещение ли добавление дополнительных получателей при пересылке сообщения, для сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="14ca3-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14ca3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="14ca3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14ca3-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="14ca3-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="14ca3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="14ca3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14ca3-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="14ca3-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="14ca3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="14ca3-110">Data type:</span></span>  <br/> |<span data-ttu-id="14ca3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="14ca3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="14ca3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="14ca3-112">Area:</span></span>  <br/> |<span data-ttu-id="14ca3-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="14ca3-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14ca3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="14ca3-114">Remarks</span></span>

<span data-ttu-id="14ca3-115">Это свойство устанавливается на основе значение **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="14ca3-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="14ca3-116">Если **PR_SENSITIVITY** задано значение «0x00000000» (обычный) или «0x00000003» (confidential), это свойство необходимо установить для «0x00» или отсутствует означает, что добавление дополнительных или других получателей на сообщение электронной почты, разрешено.</span><span class="sxs-lookup"><span data-stu-id="14ca3-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="14ca3-117">Если сообщение электронной почты объекта **PR_SENSITIVITY** задано значение «0x00000001» (личные) или «0x00000002» (личные), это свойство должно иметь значение «0x01» для предотвращения добавления дополнительных или других получателей в этом электронной почты через переадресации.</span><span class="sxs-lookup"><span data-stu-id="14ca3-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="14ca3-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="14ca3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14ca3-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="14ca3-119">Protocol specifications</span></span>

<span data-ttu-id="14ca3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14ca3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14ca3-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="14ca3-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14ca3-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14ca3-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14ca3-123">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="14ca3-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14ca3-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="14ca3-124">Header files</span></span>

<span data-ttu-id="14ca3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14ca3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="14ca3-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="14ca3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="14ca3-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="14ca3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="14ca3-128">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="14ca3-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14ca3-129">См. также</span><span class="sxs-lookup"><span data-stu-id="14ca3-129">See also</span></span>



[<span data-ttu-id="14ca3-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14ca3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14ca3-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14ca3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14ca3-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="14ca3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14ca3-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="14ca3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

