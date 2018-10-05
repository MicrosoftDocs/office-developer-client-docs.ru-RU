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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383305"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="521a6-103">Каноническое свойство PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="521a6-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="521a6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="521a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="521a6-105">Представляет пользователя доступности для встречи.</span><span class="sxs-lookup"><span data-stu-id="521a6-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="521a6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="521a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="521a6-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="521a6-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="521a6-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="521a6-108">Property set:</span></span>  <br/> |<span data-ttu-id="521a6-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="521a6-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="521a6-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="521a6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="521a6-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="521a6-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="521a6-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="521a6-112">Data type:</span></span>  <br/> |<span data-ttu-id="521a6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="521a6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="521a6-114">Область:</span><span class="sxs-lookup"><span data-stu-id="521a6-114">Area:</span></span>  <br/> |<span data-ttu-id="521a6-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="521a6-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="521a6-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="521a6-116">Remarks</span></span>

<span data-ttu-id="521a6-117">Это свойство определяет доступность пользователя для события, описанные объектом и должно быть одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="521a6-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="521a6-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="521a6-118">**Value**</span></span>|<span data-ttu-id="521a6-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="521a6-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="521a6-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="521a6-120">0x00000000</span></span>  <br/> |<span data-ttu-id="521a6-121">Пользователь доступен.</span><span class="sxs-lookup"><span data-stu-id="521a6-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="521a6-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="521a6-122">0x00000001</span></span>  <br/> |<span data-ttu-id="521a6-123">Пользователь имеет под вопросом событие запланировано.</span><span class="sxs-lookup"><span data-stu-id="521a6-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="521a6-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="521a6-124">0x00000002</span></span>  <br/> |<span data-ttu-id="521a6-125">Пользователь занят.</span><span class="sxs-lookup"><span data-stu-id="521a6-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="521a6-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="521a6-126">0x00000003</span></span>  <br/> |<span data-ttu-id="521a6-127">Пользователь является нет на месте.</span><span class="sxs-lookup"><span data-stu-id="521a6-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="521a6-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="521a6-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="521a6-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="521a6-129">Protocol specifications</span></span>

<span data-ttu-id="521a6-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="521a6-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="521a6-131">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="521a6-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="521a6-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="521a6-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="521a6-133">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="521a6-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="521a6-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="521a6-134">Header files</span></span>

<span data-ttu-id="521a6-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="521a6-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="521a6-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="521a6-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="521a6-137">См. также</span><span class="sxs-lookup"><span data-stu-id="521a6-137">See also</span></span>



[<span data-ttu-id="521a6-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="521a6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="521a6-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="521a6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="521a6-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="521a6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="521a6-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="521a6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

