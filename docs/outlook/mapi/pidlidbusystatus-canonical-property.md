---
title: Каноническое свойство PidLidBusyStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb73a0e09436177b8b53a05588508886ee28a0a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342030"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="b0e9c-103">Каноническое свойство PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="b0e9c-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="b0e9c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0e9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0e9c-105">Представляет доступность пользователя для встречи.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0e9c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b0e9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0e9c-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="b0e9c-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="b0e9c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b0e9c-108">Property set:</span></span>  <br/> |<span data-ttu-id="b0e9c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b0e9c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b0e9c-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b0e9c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b0e9c-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="b0e9c-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="b0e9c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b0e9c-112">Data type:</span></span>  <br/> |<span data-ttu-id="b0e9c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b0e9c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b0e9c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b0e9c-114">Area:</span></span>  <br/> |<span data-ttu-id="b0e9c-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="b0e9c-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0e9c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0e9c-116">Remarks</span></span>

<span data-ttu-id="b0e9c-117">Это свойство указывает доступность пользователя для события, описанного объектом, и должно быть одним из значений, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="b0e9c-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b0e9c-118">**Value**</span></span>|<span data-ttu-id="b0e9c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b0e9c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0e9c-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0e9c-120">0x00000000</span></span>  <br/> |<span data-ttu-id="b0e9c-121">Пользователь доступен.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="b0e9c-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b0e9c-122">0x00000001</span></span>  <br/> |<span data-ttu-id="b0e9c-123">У пользователя запланировано предварительное событие.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="b0e9c-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b0e9c-124">0x00000002</span></span>  <br/> |<span data-ttu-id="b0e9c-125">Пользователь занят.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="b0e9c-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b0e9c-126">0x00000003</span></span>  <br/> |<span data-ttu-id="b0e9c-127">Пользователь находится вне офиса.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b0e9c-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b0e9c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0e9c-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b0e9c-129">Protocol specifications</span></span>

<span data-ttu-id="b0e9c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0e9c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0e9c-131">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0e9c-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0e9c-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0e9c-133">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0e9c-134">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b0e9c-134">Header files</span></span>

<span data-ttu-id="b0e9c-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0e9c-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0e9c-136">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b0e9c-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0e9c-137">См. также</span><span class="sxs-lookup"><span data-stu-id="b0e9c-137">See also</span></span>



[<span data-ttu-id="b0e9c-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b0e9c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0e9c-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b0e9c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0e9c-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b0e9c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0e9c-141">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b0e9c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

