---
title: Каноническое свойство PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316193"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="7f8f5-103">Каноническое свойство PidTagFreeBusyCountMonths</span><span class="sxs-lookup"><span data-stu-id="7f8f5-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="7f8f5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f8f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f8f5-105">Содержит значение для вычисления дат начала и окончания диапазона бесплатных и загруженных данных, которые будут опубликованы в общедоступных папках.</span><span class="sxs-lookup"><span data-stu-id="7f8f5-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f8f5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7f8f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f8f5-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="7f8f5-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="7f8f5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7f8f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f8f5-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="7f8f5-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="7f8f5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7f8f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f8f5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7f8f5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7f8f5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7f8f5-112">Area:</span></span>  <br/> |<span data-ttu-id="7f8f5-113">Передаваемое сообщение с определенным классом сообщений</span><span class="sxs-lookup"><span data-stu-id="7f8f5-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f8f5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f8f5-114">Remarks</span></span>

<span data-ttu-id="7f8f5-115">Значение этого свойства должно быть больше или равно 0 и меньше или равно 36.</span><span class="sxs-lookup"><span data-stu-id="7f8f5-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="7f8f5-116">Это свойство не обязательно.</span><span class="sxs-lookup"><span data-stu-id="7f8f5-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f8f5-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7f8f5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f8f5-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7f8f5-118">Protocol specifications</span></span>

<span data-ttu-id="7f8f5-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f8f5-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f8f5-120">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="7f8f5-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="7f8f5-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f8f5-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f8f5-122">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7f8f5-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f8f5-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="7f8f5-123">Header files</span></span>

<span data-ttu-id="7f8f5-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f8f5-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f8f5-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7f8f5-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f8f5-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7f8f5-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7f8f5-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7f8f5-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f8f5-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7f8f5-128">See also</span></span>



[<span data-ttu-id="7f8f5-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7f8f5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f8f5-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7f8f5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f8f5-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7f8f5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f8f5-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="7f8f5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

