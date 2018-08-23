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
ms.openlocfilehash: e28bde9571081d61b37f6939a991c11ddeb75a4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566049"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="69734-103">Каноническое свойство PidLidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="69734-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="69734-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69734-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69734-105">Указывает дату и время в рамках повторов, которое заменит исключение.</span><span class="sxs-lookup"><span data-stu-id="69734-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69734-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="69734-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69734-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="69734-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="69734-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="69734-108">Property set:</span></span>  <br/> |<span data-ttu-id="69734-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="69734-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="69734-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="69734-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="69734-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="69734-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="69734-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="69734-112">Data type:</span></span>  <br/> |<span data-ttu-id="69734-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="69734-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="69734-114">Область:</span><span class="sxs-lookup"><span data-stu-id="69734-114">Area:</span></span>  <br/> |<span data-ttu-id="69734-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="69734-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69734-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="69734-116">Remarks</span></span>

<span data-ttu-id="69734-117">Значением должен быть указан в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="69734-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="69734-118">Это свойство позволяет найти для конкретного экземпляра объект исключения вложения.</span><span class="sxs-lookup"><span data-stu-id="69734-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="69734-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="69734-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69734-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="69734-120">Protocol specifications</span></span>

<span data-ttu-id="69734-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69734-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69734-122">Содержит определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="69734-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="69734-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69734-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69734-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="69734-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69734-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="69734-125">Header files</span></span>

<span data-ttu-id="69734-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69734-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="69734-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="69734-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69734-128">См. также</span><span class="sxs-lookup"><span data-stu-id="69734-128">See also</span></span>



[<span data-ttu-id="69734-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69734-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69734-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69734-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69734-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="69734-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69734-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="69734-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

