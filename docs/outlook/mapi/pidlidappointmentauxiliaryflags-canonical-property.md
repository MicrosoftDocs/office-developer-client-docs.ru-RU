---
title: Каноническое свойство PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345432"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="9469b-103">Каноническое свойство PidLidAppointmentAuxiliaryFlags</span><span class="sxs-lookup"><span data-stu-id="9469b-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="9469b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9469b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9469b-105">Задает битовое поле, описывающее дополнительное состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9469b-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9469b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9469b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9469b-107">Диспидапптауксфлагс</span><span class="sxs-lookup"><span data-stu-id="9469b-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="9469b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9469b-108">Property set:</span></span>  <br/> |<span data-ttu-id="9469b-109">Псетид_аппоинтмент</span><span class="sxs-lookup"><span data-stu-id="9469b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="9469b-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="9469b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9469b-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="9469b-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="9469b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9469b-112">Data type:</span></span>  <br/> |<span data-ttu-id="9469b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9469b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9469b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9469b-114">Area:</span></span>  <br/> |<span data-ttu-id="9469b-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="9469b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9469b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9469b-116">Remarks</span></span>

<span data-ttu-id="9469b-117">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9469b-117">This property is not required.</span></span> <span data-ttu-id="9469b-118">Ниже приводятся отдельные флаги, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="9469b-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="9469b-119">C (Ауксапптфлагкопиед, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9469b-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="9469b-120">Этот флаг указывает, что объект Calendar был скопирован из другой папки "Календарь".</span><span class="sxs-lookup"><span data-stu-id="9469b-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="9469b-121">R (Ауксапптфлагфорцемтгреспонсе, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9469b-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="9469b-122">Этот флаг в приглашении на собрание указывает на то, что клиент или сервер должен отправить ответ о собрании обратно организатору при выборе ответа.</span><span class="sxs-lookup"><span data-stu-id="9469b-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="9469b-123">F (Ауксапптфлагфорвардед, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="9469b-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="9469b-124">Этот флаг в приглашении на собрание указывает на то, что он был переадресован (в том числе переадресация организатором), а не приглашением организатора.</span><span class="sxs-lookup"><span data-stu-id="9469b-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9469b-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9469b-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9469b-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9469b-126">Protocol specifications</span></span>

<span data-ttu-id="9469b-127">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9469b-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9469b-128">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9469b-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9469b-129">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9469b-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9469b-130">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9469b-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9469b-131">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="9469b-131">Header files</span></span>

<span data-ttu-id="9469b-132">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9469b-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="9469b-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9469b-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9469b-134">См. также</span><span class="sxs-lookup"><span data-stu-id="9469b-134">See also</span></span>



[<span data-ttu-id="9469b-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9469b-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9469b-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9469b-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9469b-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9469b-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9469b-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9469b-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

