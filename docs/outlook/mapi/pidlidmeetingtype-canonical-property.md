---
title: Каноническое свойство PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331579"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="15abc-103">Каноническое свойство PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="15abc-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="15abc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15abc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15abc-105">Указывает тип запроса на собрание или обновления собрания.</span><span class="sxs-lookup"><span data-stu-id="15abc-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15abc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="15abc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15abc-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="15abc-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="15abc-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="15abc-108">Property set:</span></span>  <br/> |<span data-ttu-id="15abc-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="15abc-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="15abc-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="15abc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="15abc-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="15abc-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="15abc-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="15abc-112">Data type:</span></span>  <br/> |<span data-ttu-id="15abc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="15abc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="15abc-114">Область:</span><span class="sxs-lookup"><span data-stu-id="15abc-114">Area:</span></span>  <br/> |<span data-ttu-id="15abc-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="15abc-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15abc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="15abc-116">Remarks</span></span>

<span data-ttu-id="15abc-117">Этому свойству необходимо установить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="15abc-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="15abc-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="15abc-118">**Property**</span></span>|<span data-ttu-id="15abc-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="15abc-119">**Value**</span></span>|<span data-ttu-id="15abc-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="15abc-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="15abc-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="15abc-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="15abc-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15abc-122">0x00000000</span></span>  <br/> |<span data-ttu-id="15abc-123">Не засвечено.</span><span class="sxs-lookup"><span data-stu-id="15abc-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="15abc-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="15abc-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="15abc-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15abc-125">0x00000001</span></span>  <br/> |<span data-ttu-id="15abc-126">Начальный запрос на собрание.</span><span class="sxs-lookup"><span data-stu-id="15abc-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="15abc-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="15abc-127">mtgFull</span></span>  <br/> |<span data-ttu-id="15abc-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="15abc-128">0x00010000</span></span>  <br/> |<span data-ttu-id="15abc-129">Полное обновление.</span><span class="sxs-lookup"><span data-stu-id="15abc-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="15abc-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="15abc-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="15abc-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="15abc-131">0x00020000</span></span>  <br/> |<span data-ttu-id="15abc-132">Информационное обновление.</span><span class="sxs-lookup"><span data-stu-id="15abc-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="15abc-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="15abc-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="15abc-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="15abc-134">0x00080000</span></span>  <br/> |<span data-ttu-id="15abc-135">После этого был получен более новый запрос на собрание или обновление собрания.</span><span class="sxs-lookup"><span data-stu-id="15abc-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="15abc-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="15abc-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="15abc-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="15abc-137">0x00100000</span></span>  <br/> |<span data-ttu-id="15abc-138">Он устанавливается в копии делегатора, когда делегат обрабатывает объекты, связанные с собранием.</span><span class="sxs-lookup"><span data-stu-id="15abc-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="15abc-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="15abc-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15abc-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="15abc-140">Protocol specifications</span></span>

<span data-ttu-id="15abc-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15abc-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15abc-142">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="15abc-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15abc-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15abc-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15abc-144">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="15abc-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15abc-145">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="15abc-145">Header files</span></span>

<span data-ttu-id="15abc-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15abc-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="15abc-147">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="15abc-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15abc-148">См. также</span><span class="sxs-lookup"><span data-stu-id="15abc-148">See also</span></span>



[<span data-ttu-id="15abc-149">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="15abc-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15abc-150">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="15abc-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15abc-151">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="15abc-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15abc-152">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="15abc-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

