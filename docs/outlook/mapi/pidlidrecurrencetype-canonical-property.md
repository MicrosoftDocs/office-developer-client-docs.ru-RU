---
title: Каноническое свойство PidLidRecurrenceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a0ea0dfe236341815fe94fb570908d7034fc83e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315913"
---
# <a name="pidlidrecurrencetype-canonical-property"></a><span data-ttu-id="4447f-103">Каноническое свойство PidLidRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="4447f-103">PidLidRecurrenceType Canonical Property</span></span>

  
  
<span data-ttu-id="4447f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4447f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4447f-105">Указывает тип повторения повторяющегося ряда.</span><span class="sxs-lookup"><span data-stu-id="4447f-105">Specifies the recurrence type of the recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4447f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4447f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4447f-107">dispidRecurType</span><span class="sxs-lookup"><span data-stu-id="4447f-107">dispidRecurType</span></span>  <br/> |
|<span data-ttu-id="4447f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4447f-108">Property set:</span></span>  <br/> |<span data-ttu-id="4447f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4447f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4447f-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="4447f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4447f-111">0x00008231</span><span class="sxs-lookup"><span data-stu-id="4447f-111">0x00008231</span></span>  <br/> |
|<span data-ttu-id="4447f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4447f-112">Data type:</span></span>  <br/> |<span data-ttu-id="4447f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4447f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4447f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4447f-114">Area:</span></span>  <br/> |<span data-ttu-id="4447f-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="4447f-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4447f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4447f-116">Remarks</span></span>

<span data-ttu-id="4447f-117">Это свойство указывает тип повторения повторяющегося ряда с помощью одного из значений, перечисленных ниже.</span><span class="sxs-lookup"><span data-stu-id="4447f-117">This property specifies the recurrence type of the recurring series by using one of the values listed below.</span></span>
  
|<span data-ttu-id="4447f-118">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="4447f-118">**Status**</span></span>|<span data-ttu-id="4447f-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4447f-119">**Value**</span></span>|<span data-ttu-id="4447f-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4447f-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4447f-121">rectypeNone</span><span class="sxs-lookup"><span data-stu-id="4447f-121">rectypeNone</span></span>  <br/> |<span data-ttu-id="4447f-122">0</span><span class="sxs-lookup"><span data-stu-id="4447f-122">0</span></span>  <br/> |<span data-ttu-id="4447f-123">Встреча с одним экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4447f-123">A single instance appointment.</span></span>  <br/> |
|<span data-ttu-id="4447f-124">rectypeDaily</span><span class="sxs-lookup"><span data-stu-id="4447f-124">rectypeDaily</span></span>  <br/> |<span data-ttu-id="4447f-125">1 </span><span class="sxs-lookup"><span data-stu-id="4447f-125">1</span></span>  <br/> |<span data-ttu-id="4447f-126">Ежедневный шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="4447f-126">A daily recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="4447f-127">rectypeWeekly</span><span class="sxs-lookup"><span data-stu-id="4447f-127">rectypeWeekly</span></span>  <br/> |<span data-ttu-id="4447f-128">2 </span><span class="sxs-lookup"><span data-stu-id="4447f-128">2</span></span>  <br/> |<span data-ttu-id="4447f-129">Еженедельный шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="4447f-129">A weekly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="4447f-130">rectypeMonthly</span><span class="sxs-lookup"><span data-stu-id="4447f-130">rectypeMonthly</span></span>  <br/> |<span data-ttu-id="4447f-131">3 </span><span class="sxs-lookup"><span data-stu-id="4447f-131">3</span></span>  <br/> |<span data-ttu-id="4447f-132">Ежемесячный шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="4447f-132">A monthly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="4447f-133">rectypeYearly</span><span class="sxs-lookup"><span data-stu-id="4447f-133">rectypeYearly</span></span>  <br/> |<span data-ttu-id="4447f-134">4 </span><span class="sxs-lookup"><span data-stu-id="4447f-134">4</span></span>  <br/> |<span data-ttu-id="4447f-135">Ежегодное регулярное повторение.</span><span class="sxs-lookup"><span data-stu-id="4447f-135">A yearly recurrence pattern.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4447f-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4447f-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4447f-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4447f-137">Protocol specifications</span></span>

<span data-ttu-id="4447f-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4447f-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4447f-139">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="4447f-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4447f-140">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4447f-140">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4447f-141">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4447f-141">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4447f-142">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="4447f-142">Header files</span></span>

<span data-ttu-id="4447f-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4447f-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="4447f-144">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4447f-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4447f-145">См. также</span><span class="sxs-lookup"><span data-stu-id="4447f-145">See also</span></span>



[<span data-ttu-id="4447f-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4447f-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4447f-147">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4447f-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4447f-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4447f-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4447f-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4447f-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

