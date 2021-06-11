---
title: PidTagRecipientReassignmentProhibited Canonical Property
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
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341113"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="5ef0b-103">PidTagRecipientReassignmentProhibited Canonical Property</span><span class="sxs-lookup"><span data-stu-id="5ef0b-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="5ef0b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ef0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ef0b-105">Указывает, запрещено ли добавлять дополнительных получателей при отправке сообщения для сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ef0b-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ef0b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5ef0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ef0b-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="5ef0b-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="5ef0b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5ef0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ef0b-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="5ef0b-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="5ef0b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5ef0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ef0b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5ef0b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5ef0b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5ef0b-112">Area:</span></span>  <br/> |<span data-ttu-id="5ef0b-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="5ef0b-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ef0b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ef0b-114">Remarks</span></span>

<span data-ttu-id="5ef0b-115">Это свойство устанавливается на основе значения  PR_SENSITIVITY[(PidTagSensitivity).](pidtagsensitivity-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5ef0b-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="5ef0b-116">Если **PR_SENSITIVITY** установлено значение "0x00000000" (нормальное) или "0x00000003" (конфиденциальное), это свойство должно быть заданной на значение "0x00" или отсутствовать, что допускается добавление дополнительных или разных получателей в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ef0b-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="5ef0b-117">Если PR_SENSITIVITY объекта  электронной почты задают "0x00000001" (личное) или "0x00000002" (частное), это свойство должно быть задано "0x01", чтобы предотвратить добавление дополнительных или разных получателей этой электронной почты путем переададки.</span><span class="sxs-lookup"><span data-stu-id="5ef0b-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5ef0b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ef0b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ef0b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5ef0b-119">Protocol specifications</span></span>

<span data-ttu-id="5ef0b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ef0b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ef0b-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="5ef0b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ef0b-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ef0b-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ef0b-123">Указывает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ef0b-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ef0b-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5ef0b-124">Header files</span></span>

<span data-ttu-id="5ef0b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ef0b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ef0b-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5ef0b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ef0b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5ef0b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5ef0b-128">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="5ef0b-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ef0b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5ef0b-129">See also</span></span>



[<span data-ttu-id="5ef0b-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ef0b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ef0b-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ef0b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ef0b-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5ef0b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ef0b-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5ef0b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

