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
ms.openlocfilehash: cac9c735403e6cb65dfe3111a2246a8387339339
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810092"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="fc7cf-103">Каноническое свойство PidLidAppointmentAuxiliaryFlags</span><span class="sxs-lookup"><span data-stu-id="fc7cf-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="fc7cf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc7cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc7cf-105">Задает битовое поле, которое описывает дополнительный состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc7cf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fc7cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc7cf-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="fc7cf-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="fc7cf-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="fc7cf-108">Property set:</span></span>  <br/> |<span data-ttu-id="fc7cf-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fc7cf-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fc7cf-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="fc7cf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fc7cf-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="fc7cf-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="fc7cf-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fc7cf-112">Data type:</span></span>  <br/> |<span data-ttu-id="fc7cf-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fc7cf-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fc7cf-114">Область:</span><span class="sxs-lookup"><span data-stu-id="fc7cf-114">Area:</span></span>  <br/> |<span data-ttu-id="fc7cf-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="fc7cf-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc7cf-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="fc7cf-116">Remarks</span></span>

<span data-ttu-id="fc7cf-117">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-117">This property is not required.</span></span> <span data-ttu-id="fc7cf-118">Ниже приведены отдельные флаги, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="fc7cf-119">C (auxApptFlagCopied, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="fc7cf-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="fc7cf-120">Этот флаг указывает, что объект календаря, скопированный из другой папки календаря.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="fc7cf-121">R (auxApptFlagForceMtgResponse 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="fc7cf-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="fc7cf-122">Этот флаг на приглашения на собрание указывает, что клиент или сервер следует отправить ответ на приглашение к организатора, при выборе ответа.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="fc7cf-123">F (auxApptFlagForwarded 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="fc7cf-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="fc7cf-124">Этот флаг на приглашения на собрание указывает, что оно было перенаправлено (включая переадресацию организатором), а не приглашение из картинок.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="fc7cf-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fc7cf-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc7cf-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fc7cf-126">Protocol specifications</span></span>

<span data-ttu-id="fc7cf-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc7cf-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc7cf-128">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc7cf-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc7cf-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc7cf-130">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc7cf-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fc7cf-131">Header files</span></span>

<span data-ttu-id="fc7cf-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc7cf-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc7cf-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc7cf-134">См. также</span><span class="sxs-lookup"><span data-stu-id="fc7cf-134">See also</span></span>



[<span data-ttu-id="fc7cf-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fc7cf-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc7cf-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fc7cf-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc7cf-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fc7cf-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc7cf-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fc7cf-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

