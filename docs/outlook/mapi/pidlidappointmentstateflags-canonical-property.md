---
title: Каноническое свойство PidLidAppointmentStateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c42649b231e691fec8b5a8d7024b87346cd8ce18
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568548"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="7fdaa-103">Каноническое свойство PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="7fdaa-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="7fdaa-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fdaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fdaa-105">Задает битовое поле, которое описывает состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fdaa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7fdaa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7fdaa-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="7fdaa-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="7fdaa-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="7fdaa-108">Property set:</span></span>  <br/> |<span data-ttu-id="7fdaa-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7fdaa-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7fdaa-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="7fdaa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7fdaa-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="7fdaa-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="7fdaa-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7fdaa-112">Data type:</span></span>  <br/> |<span data-ttu-id="7fdaa-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7fdaa-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7fdaa-114">Область:</span><span class="sxs-lookup"><span data-stu-id="7fdaa-114">Area:</span></span>  <br/> |<span data-ttu-id="7fdaa-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="7fdaa-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fdaa-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="7fdaa-116">Remarks</span></span>

<span data-ttu-id="7fdaa-117">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-117">This property is not required.</span></span> <span data-ttu-id="7fdaa-118">Ниже приведены отдельные флаги, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="7fdaa-119">M (asfMeeting, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="7fdaa-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="7fdaa-120">Этот флаг указывает, что объект является собрания объектов или объектов, относящихся к собранию.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="7fdaa-121">R (asfReceived 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="7fdaa-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="7fdaa-122">Этот флаг указывает, что представляемого объекта было получено из другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="7fdaa-123">C (asfCanceled 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="7fdaa-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="7fdaa-124">Этот флаг указывает, что объект собрания, представленного объектом была отменена.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="7fdaa-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7fdaa-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7fdaa-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7fdaa-126">Protocol specifications</span></span>

<span data-ttu-id="7fdaa-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fdaa-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fdaa-128">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7fdaa-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fdaa-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fdaa-130">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7fdaa-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7fdaa-131">Header files</span></span>

<span data-ttu-id="7fdaa-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7fdaa-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="7fdaa-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fdaa-134">См. также</span><span class="sxs-lookup"><span data-stu-id="7fdaa-134">See also</span></span>



[<span data-ttu-id="7fdaa-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7fdaa-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7fdaa-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7fdaa-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7fdaa-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7fdaa-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7fdaa-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7fdaa-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

