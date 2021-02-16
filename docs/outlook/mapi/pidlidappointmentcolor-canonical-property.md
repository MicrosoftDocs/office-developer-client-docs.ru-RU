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
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345439"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="7b8f8-103">Каноническое свойство PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="7b8f8-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="7b8f8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b8f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b8f8-105">Указывает цвет, который будет применяться при отобраке календаря.</span><span class="sxs-lookup"><span data-stu-id="7b8f8-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b8f8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7b8f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b8f8-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="7b8f8-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="7b8f8-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="7b8f8-108">Property set:</span></span>  <br/> |<span data-ttu-id="7b8f8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7b8f8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7b8f8-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="7b8f8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7b8f8-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="7b8f8-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="7b8f8-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7b8f8-112">Data type:</span></span>  <br/> |<span data-ttu-id="7b8f8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7b8f8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7b8f8-114">Область:</span><span class="sxs-lookup"><span data-stu-id="7b8f8-114">Area:</span></span>  <br/> |<span data-ttu-id="7b8f8-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="7b8f8-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b8f8-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b8f8-116">Remarks</span></span>

<span data-ttu-id="7b8f8-117">Это свойство указывает цвет, который будет применяться при отобраке календаря.</span><span class="sxs-lookup"><span data-stu-id="7b8f8-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="7b8f8-118">Клиент или сервер должны установить это значение для обратной совместимости с более старыми клиентами.</span><span class="sxs-lookup"><span data-stu-id="7b8f8-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="7b8f8-119">Вместо этого он может отображать календарь на основе значения свойства **Keywords** [(PidNameKeywords),](pidnamekeywords-canonical-property.md)как указано [в [MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7b8f8-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="7b8f8-120">При этом значение должно быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7b8f8-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="7b8f8-121">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7b8f8-121">**Value**</span></span>|<span data-ttu-id="7b8f8-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="7b8f8-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b8f8-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b8f8-123">0x00000000</span></span>  <br/> |<span data-ttu-id="7b8f8-124">Нет</span><span class="sxs-lookup"><span data-stu-id="7b8f8-124">None</span></span>  <br/> |
|<span data-ttu-id="7b8f8-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7b8f8-125">0x00000001</span></span>  <br/> |<span data-ttu-id="7b8f8-126">Красный</span><span class="sxs-lookup"><span data-stu-id="7b8f8-126">Red</span></span>  <br/> |
|<span data-ttu-id="7b8f8-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7b8f8-127">0x00000002</span></span>  <br/> |<span data-ttu-id="7b8f8-128">Синий</span><span class="sxs-lookup"><span data-stu-id="7b8f8-128">Blue</span></span>  <br/> |
|<span data-ttu-id="7b8f8-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="7b8f8-129">0x00000003</span></span>  <br/> |<span data-ttu-id="7b8f8-130">Зеленый</span><span class="sxs-lookup"><span data-stu-id="7b8f8-130">Green</span></span>  <br/> |
|<span data-ttu-id="7b8f8-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7b8f8-131">0x00000004</span></span>  <br/> |<span data-ttu-id="7b8f8-132">Серый</span><span class="sxs-lookup"><span data-stu-id="7b8f8-132">Grey</span></span>  <br/> |
|<span data-ttu-id="7b8f8-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7b8f8-133">0x00000005</span></span>  <br/> |<span data-ttu-id="7b8f8-134">Апельсин</span><span class="sxs-lookup"><span data-stu-id="7b8f8-134">Orange</span></span>  <br/> |
|<span data-ttu-id="7b8f8-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="7b8f8-135">0x00000006</span></span>  <br/> |<span data-ttu-id="7b8f8-136">Cyan</span><span class="sxs-lookup"><span data-stu-id="7b8f8-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="7b8f8-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="7b8f8-137">0x00000007</span></span>  <br/> |<span data-ttu-id="7b8f8-138">Оливковый</span><span class="sxs-lookup"><span data-stu-id="7b8f8-138">Olive</span></span>  <br/> |
|<span data-ttu-id="7b8f8-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7b8f8-139">0x00000008</span></span>  <br/> |<span data-ttu-id="7b8f8-140">Сиреневый</span><span class="sxs-lookup"><span data-stu-id="7b8f8-140">Purple</span></span>  <br/> |
|<span data-ttu-id="7b8f8-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="7b8f8-141">0x00000009</span></span>  <br/> |<span data-ttu-id="7b8f8-142">Сине-зеленая</span><span class="sxs-lookup"><span data-stu-id="7b8f8-142">Teal</span></span>  <br/> |
|<span data-ttu-id="7b8f8-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="7b8f8-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="7b8f8-144">Желтый</span><span class="sxs-lookup"><span data-stu-id="7b8f8-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7b8f8-145">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b8f8-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b8f8-146">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7b8f8-146">Protocol specifications</span></span>

<span data-ttu-id="7b8f8-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b8f8-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b8f8-148">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="7b8f8-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b8f8-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b8f8-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b8f8-150">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b8f8-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b8f8-151">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="7b8f8-151">Header files</span></span>

<span data-ttu-id="7b8f8-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b8f8-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b8f8-153">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b8f8-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b8f8-154">См. также</span><span class="sxs-lookup"><span data-stu-id="7b8f8-154">See also</span></span>



[<span data-ttu-id="7b8f8-155">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b8f8-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b8f8-156">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b8f8-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b8f8-157">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7b8f8-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b8f8-158">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7b8f8-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

