---
title: Каноническое свойство PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321324"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="23077-103">Каноническое свойство PidTagScheduleInfoAppointmentTombstone</span><span class="sxs-lookup"><span data-stu-id="23077-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="23077-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23077-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23077-105">Содержит список блоков данных, представляющих отклоненные собрания.</span><span class="sxs-lookup"><span data-stu-id="23077-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23077-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="23077-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23077-107">ПР_СЧДИНФО_АППТ_ТОМБСТОНЕ</span><span class="sxs-lookup"><span data-stu-id="23077-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="23077-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="23077-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23077-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="23077-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="23077-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="23077-110">Data type:</span></span>  <br/> |<span data-ttu-id="23077-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="23077-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="23077-112">Область:</span><span class="sxs-lookup"><span data-stu-id="23077-112">Area:</span></span>  <br/> |<span data-ttu-id="23077-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="23077-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23077-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="23077-114">Remarks</span></span>

<span data-ttu-id="23077-115">Блоки данных начинаются с заголовка 32 битовых значений, заданных как:</span><span class="sxs-lookup"><span data-stu-id="23077-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="23077-116">**Value**</span><span class="sxs-lookup"><span data-stu-id="23077-116">**Value**</span></span>|<span data-ttu-id="23077-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23077-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23077-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="23077-118">Identifier</span></span>  <br/> |<span data-ttu-id="23077-119">Это поле должно быть значением 0xBEDEAFCD.</span><span class="sxs-lookup"><span data-stu-id="23077-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="23077-120">Хеадерсизе</span><span class="sxs-lookup"><span data-stu-id="23077-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="23077-121">Это поле должно иметь значение 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="23077-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="23077-122">Версия</span><span class="sxs-lookup"><span data-stu-id="23077-122">Version</span></span>  <br/> |<span data-ttu-id="23077-123">Это поле должно иметь значение 3.</span><span class="sxs-lookup"><span data-stu-id="23077-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="23077-124">Рекордскаунт</span><span class="sxs-lookup"><span data-stu-id="23077-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="23077-125">Количество последующих записей.</span><span class="sxs-lookup"><span data-stu-id="23077-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="23077-126">Рекордссизе</span><span class="sxs-lookup"><span data-stu-id="23077-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="23077-127">Это поле должно иметь значение 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="23077-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="23077-128">За заголовком следуют записи **рекордскаунт** со значениями 32 бит, определенные как:</span><span class="sxs-lookup"><span data-stu-id="23077-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="23077-129">**Value**</span><span class="sxs-lookup"><span data-stu-id="23077-129">**Value**</span></span>|<span data-ttu-id="23077-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23077-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23077-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="23077-131">StartTime</span></span>  <br/> |<span data-ttu-id="23077-132">Время начала объекта собрания (в минутах), начиная с полуночи 1 января 1601,, UTC.</span><span class="sxs-lookup"><span data-stu-id="23077-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="23077-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="23077-133">EndTime</span></span>  <br/> |<span data-ttu-id="23077-134">Время окончания объекта собрания (в минутах), начиная с полуночи 1 января 1601,, UTC.</span><span class="sxs-lookup"><span data-stu-id="23077-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="23077-135">Глобалобжектидсизе</span><span class="sxs-lookup"><span data-stu-id="23077-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="23077-136">Размер (в байтах) поля Глобалобжектид.</span><span class="sxs-lookup"><span data-stu-id="23077-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="23077-137">Глобалобжектид</span><span class="sxs-lookup"><span data-stu-id="23077-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="23077-138">Значение свойства **лид_глобал_обжид** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) собрания, представляющего эту запись.</span><span class="sxs-lookup"><span data-stu-id="23077-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="23077-139">UserName</span><span class="sxs-lookup"><span data-stu-id="23077-139">UserName</span></span>  <br/> |<span data-ttu-id="23077-140">Первые два байта — это длина строки PT_STRING8, приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="23077-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="23077-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="23077-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23077-142">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="23077-142">Protocol specifications</span></span>

<span data-ttu-id="23077-143">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23077-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23077-144">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="23077-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23077-145">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23077-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23077-146">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="23077-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23077-147">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="23077-147">Header files</span></span>

<span data-ttu-id="23077-148">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="23077-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="23077-149">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="23077-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="23077-150">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="23077-150">Mapitags.h</span></span>
  
> <span data-ttu-id="23077-151">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="23077-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23077-152">См. также</span><span class="sxs-lookup"><span data-stu-id="23077-152">See also</span></span>



[<span data-ttu-id="23077-153">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="23077-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23077-154">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="23077-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23077-155">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="23077-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23077-156">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="23077-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

