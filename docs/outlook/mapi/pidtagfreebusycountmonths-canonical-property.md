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
ms.openlocfilehash: 5ba76b5735687e3bb65e530b3de0d257754559c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811174"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="f05c8-103">Каноническое свойство PidTagFreeBusyCountMonths</span><span class="sxs-lookup"><span data-stu-id="f05c8-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="f05c8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f05c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f05c8-105">Содержит значение для расчета начальную и конечную даты диапазона данных о доступности для публикации для общих папок.</span><span class="sxs-lookup"><span data-stu-id="f05c8-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f05c8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f05c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f05c8-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="f05c8-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="f05c8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f05c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f05c8-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="f05c8-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="f05c8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f05c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f05c8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f05c8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f05c8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f05c8-112">Area:</span></span>  <br/> |<span data-ttu-id="f05c8-113">Сообщение, определенное класс передаваемого</span><span class="sxs-lookup"><span data-stu-id="f05c8-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f05c8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f05c8-114">Remarks</span></span>

<span data-ttu-id="f05c8-115">Значение этого свойства должно быть больше или равно 0 и меньше или равно 36.</span><span class="sxs-lookup"><span data-stu-id="f05c8-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="f05c8-116">Это не обязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="f05c8-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f05c8-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f05c8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f05c8-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f05c8-118">Protocol specifications</span></span>

<span data-ttu-id="f05c8-119">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f05c8-119">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f05c8-120">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="f05c8-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="f05c8-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f05c8-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f05c8-122">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="f05c8-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f05c8-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f05c8-123">Header files</span></span>

<span data-ttu-id="f05c8-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f05c8-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f05c8-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f05c8-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f05c8-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f05c8-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f05c8-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f05c8-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f05c8-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f05c8-128">See also</span></span>



[<span data-ttu-id="f05c8-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f05c8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f05c8-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f05c8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f05c8-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f05c8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f05c8-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f05c8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

