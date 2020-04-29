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
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345362"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="8352d-103">Каноническое свойство PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="8352d-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="8352d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8352d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8352d-105">Задает битовое поле, описывающее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8352d-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8352d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8352d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8352d-107">диспидапптстатефлагс</span><span class="sxs-lookup"><span data-stu-id="8352d-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="8352d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8352d-108">Property set:</span></span>  <br/> |<span data-ttu-id="8352d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8352d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8352d-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="8352d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8352d-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="8352d-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="8352d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8352d-112">Data type:</span></span>  <br/> |<span data-ttu-id="8352d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8352d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8352d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8352d-114">Area:</span></span>  <br/> |<span data-ttu-id="8352d-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="8352d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8352d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8352d-116">Remarks</span></span>

<span data-ttu-id="8352d-117">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8352d-117">This property is not required.</span></span> <span data-ttu-id="8352d-118">Ниже приводятся отдельные флаги, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="8352d-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="8352d-119">M (Асфмитинг, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="8352d-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="8352d-120">Этот флаг указывает, что объект является объектом собрания или объектом, связанным с собранием.</span><span class="sxs-lookup"><span data-stu-id="8352d-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="8352d-121">R (Асфрецеивед, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="8352d-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="8352d-122">Этот флаг указывает, что предоставленный объект был получен от другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="8352d-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="8352d-123">C (Асфканцелед, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="8352d-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="8352d-124">Этот флаг указывает, что объект собрания, представленный объектом, был отменен.</span><span class="sxs-lookup"><span data-stu-id="8352d-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8352d-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8352d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8352d-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8352d-126">Protocol specifications</span></span>

<span data-ttu-id="8352d-127">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8352d-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8352d-128">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8352d-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8352d-129">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8352d-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8352d-130">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8352d-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8352d-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8352d-131">Header files</span></span>

<span data-ttu-id="8352d-132">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8352d-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="8352d-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8352d-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8352d-134">См. также</span><span class="sxs-lookup"><span data-stu-id="8352d-134">See also</span></span>



[<span data-ttu-id="8352d-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8352d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8352d-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8352d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8352d-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8352d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8352d-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8352d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

