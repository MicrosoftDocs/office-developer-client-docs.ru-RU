---
title: Каноническое свойство PidLidExceptionReplaceTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b364fb91bda7e895b546f9a281ef14ce33b073f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337985"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="38b5e-103">Каноническое свойство PidLidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="38b5e-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="38b5e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38b5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38b5e-105">Указывает дату и время в шаблоне повторения, который заменит исключение.</span><span class="sxs-lookup"><span data-stu-id="38b5e-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38b5e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="38b5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38b5e-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="38b5e-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="38b5e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="38b5e-108">Property set:</span></span>  <br/> |<span data-ttu-id="38b5e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="38b5e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="38b5e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="38b5e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="38b5e-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="38b5e-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="38b5e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="38b5e-112">Data type:</span></span>  <br/> |<span data-ttu-id="38b5e-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="38b5e-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="38b5e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="38b5e-114">Area:</span></span>  <br/> |<span data-ttu-id="38b5e-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="38b5e-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38b5e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="38b5e-116">Remarks</span></span>

<span data-ttu-id="38b5e-117">Значение должно быть указано в координируется универсальное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="38b5e-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="38b5e-118">Это свойство позволяет найти объект вложения исключений для конкретного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="38b5e-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38b5e-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="38b5e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38b5e-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="38b5e-120">Protocol specifications</span></span>

<span data-ttu-id="38b5e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38b5e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38b5e-122">Предоставляет определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="38b5e-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="38b5e-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38b5e-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38b5e-124">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="38b5e-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38b5e-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="38b5e-125">Header files</span></span>

<span data-ttu-id="38b5e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38b5e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="38b5e-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="38b5e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38b5e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="38b5e-128">See also</span></span>



[<span data-ttu-id="38b5e-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="38b5e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38b5e-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="38b5e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38b5e-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="38b5e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38b5e-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="38b5e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

