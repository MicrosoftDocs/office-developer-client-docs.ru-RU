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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388940"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="84077-103">Каноническое свойство PidTagFreeBusyCountMonths</span><span class="sxs-lookup"><span data-stu-id="84077-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="84077-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84077-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84077-105">Содержит значение для расчета начальную и конечную даты диапазона данных о доступности для публикации для общих папок.</span><span class="sxs-lookup"><span data-stu-id="84077-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84077-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="84077-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84077-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="84077-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="84077-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="84077-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84077-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="84077-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="84077-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="84077-110">Data type:</span></span>  <br/> |<span data-ttu-id="84077-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="84077-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="84077-112">Область:</span><span class="sxs-lookup"><span data-stu-id="84077-112">Area:</span></span>  <br/> |<span data-ttu-id="84077-113">Сообщение, определенное класс передаваемого</span><span class="sxs-lookup"><span data-stu-id="84077-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84077-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="84077-114">Remarks</span></span>

<span data-ttu-id="84077-115">Значение этого свойства должно быть больше или равно 0 и меньше или равно 36.</span><span class="sxs-lookup"><span data-stu-id="84077-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="84077-116">Это не обязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="84077-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84077-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="84077-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84077-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="84077-118">Protocol specifications</span></span>

<span data-ttu-id="84077-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84077-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84077-120">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="84077-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="84077-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84077-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84077-122">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="84077-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84077-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="84077-123">Header files</span></span>

<span data-ttu-id="84077-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84077-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="84077-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="84077-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="84077-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84077-126">Mapitags.h</span></span>
  
> <span data-ttu-id="84077-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="84077-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84077-128">См. также</span><span class="sxs-lookup"><span data-stu-id="84077-128">See also</span></span>



[<span data-ttu-id="84077-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="84077-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84077-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="84077-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84077-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="84077-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84077-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="84077-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

