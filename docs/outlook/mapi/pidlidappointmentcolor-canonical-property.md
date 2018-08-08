---
title: Каноническое свойство PidLidAppointmentColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810094"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="de9c3-103">Каноническое свойство PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="de9c3-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="de9c3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de9c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de9c3-105">Определяет цвет, используемый при отображении в календаре.</span><span class="sxs-lookup"><span data-stu-id="de9c3-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de9c3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="de9c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de9c3-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="de9c3-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="de9c3-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="de9c3-108">Property set:</span></span>  <br/> |<span data-ttu-id="de9c3-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="de9c3-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="de9c3-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="de9c3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="de9c3-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="de9c3-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="de9c3-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="de9c3-112">Data type:</span></span>  <br/> |<span data-ttu-id="de9c3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="de9c3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="de9c3-114">Область:</span><span class="sxs-lookup"><span data-stu-id="de9c3-114">Area:</span></span>  <br/> |<span data-ttu-id="de9c3-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="de9c3-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de9c3-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="de9c3-116">Remarks</span></span>

<span data-ttu-id="de9c3-117">Это свойство определяет цвет, используемый при отображении в календаре.</span><span class="sxs-lookup"><span data-stu-id="de9c3-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="de9c3-118">Клиент или сервер следует установить это значение для обеспечения обратной совместимости с клиентами, возраст которых.</span><span class="sxs-lookup"><span data-stu-id="de9c3-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="de9c3-119">Вместо этого он может отображать календаря на основе значения свойства **ключевые слова** ([PidNameKeywords](pidnamekeywords-canonical-property.md)), как указано в [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="de9c3-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="de9c3-120">Если задано значение должно быть одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="de9c3-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="de9c3-121">**Значение**</span><span class="sxs-lookup"><span data-stu-id="de9c3-121">**Value**</span></span>|<span data-ttu-id="de9c3-122">**Цвет**</span><span class="sxs-lookup"><span data-stu-id="de9c3-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de9c3-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de9c3-123">0x00000000</span></span>  <br/> |<span data-ttu-id="de9c3-124">Нет</span><span class="sxs-lookup"><span data-stu-id="de9c3-124">None</span></span>  <br/> |
|<span data-ttu-id="de9c3-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="de9c3-125">0x00000001</span></span>  <br/> |<span data-ttu-id="de9c3-126">Красный</span><span class="sxs-lookup"><span data-stu-id="de9c3-126">Red</span></span>  <br/> |
|<span data-ttu-id="de9c3-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="de9c3-127">0x00000002</span></span>  <br/> |<span data-ttu-id="de9c3-128">Синий</span><span class="sxs-lookup"><span data-stu-id="de9c3-128">Blue</span></span>  <br/> |
|<span data-ttu-id="de9c3-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="de9c3-129">0x00000003</span></span>  <br/> |<span data-ttu-id="de9c3-130">Зеленый</span><span class="sxs-lookup"><span data-stu-id="de9c3-130">Green</span></span>  <br/> |
|<span data-ttu-id="de9c3-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="de9c3-131">0x00000004</span></span>  <br/> |<span data-ttu-id="de9c3-132">Серый цвет</span><span class="sxs-lookup"><span data-stu-id="de9c3-132">Grey</span></span>  <br/> |
|<span data-ttu-id="de9c3-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="de9c3-133">0x00000005</span></span>  <br/> |<span data-ttu-id="de9c3-134">Оранжевый</span><span class="sxs-lookup"><span data-stu-id="de9c3-134">Orange</span></span>  <br/> |
|<span data-ttu-id="de9c3-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="de9c3-135">0x00000006</span></span>  <br/> |<span data-ttu-id="de9c3-136">Голубой</span><span class="sxs-lookup"><span data-stu-id="de9c3-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="de9c3-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="de9c3-137">0x00000007</span></span>  <br/> |<span data-ttu-id="de9c3-138">Оливковый</span><span class="sxs-lookup"><span data-stu-id="de9c3-138">Olive</span></span>  <br/> |
|<span data-ttu-id="de9c3-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="de9c3-139">0x00000008</span></span>  <br/> |<span data-ttu-id="de9c3-140">Сиреневый</span><span class="sxs-lookup"><span data-stu-id="de9c3-140">Purple</span></span>  <br/> |
|<span data-ttu-id="de9c3-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="de9c3-141">0x00000009</span></span>  <br/> |<span data-ttu-id="de9c3-142">Сине-зеленый</span><span class="sxs-lookup"><span data-stu-id="de9c3-142">Teal</span></span>  <br/> |
|<span data-ttu-id="de9c3-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="de9c3-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="de9c3-144">Желтый</span><span class="sxs-lookup"><span data-stu-id="de9c3-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="de9c3-145">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="de9c3-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de9c3-146">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="de9c3-146">Protocol specifications</span></span>

<span data-ttu-id="de9c3-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de9c3-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de9c3-148">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="de9c3-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de9c3-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de9c3-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de9c3-150">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="de9c3-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de9c3-151">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="de9c3-151">Header files</span></span>

<span data-ttu-id="de9c3-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de9c3-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="de9c3-153">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="de9c3-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de9c3-154">См. также</span><span class="sxs-lookup"><span data-stu-id="de9c3-154">See also</span></span>



[<span data-ttu-id="de9c3-155">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="de9c3-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de9c3-156">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="de9c3-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de9c3-157">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="de9c3-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de9c3-158">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="de9c3-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

