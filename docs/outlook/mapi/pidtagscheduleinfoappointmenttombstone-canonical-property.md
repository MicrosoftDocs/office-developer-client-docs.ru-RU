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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399167"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="62eff-103">Каноническое свойство PidTagScheduleInfoAppointmentTombstone</span><span class="sxs-lookup"><span data-stu-id="62eff-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="62eff-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62eff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62eff-105">Содержит список блоков данных, которые представляют собрания, которые было отклонено.</span><span class="sxs-lookup"><span data-stu-id="62eff-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62eff-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="62eff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62eff-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="62eff-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="62eff-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="62eff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="62eff-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="62eff-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="62eff-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="62eff-110">Data type:</span></span>  <br/> |<span data-ttu-id="62eff-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="62eff-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="62eff-112">Область:</span><span class="sxs-lookup"><span data-stu-id="62eff-112">Area:</span></span>  <br/> |<span data-ttu-id="62eff-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="62eff-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62eff-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="62eff-114">Remarks</span></span>

<span data-ttu-id="62eff-115">Блоки данных начинаются с заголовком 32-разрядная версия значения, определенные как:</span><span class="sxs-lookup"><span data-stu-id="62eff-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="62eff-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="62eff-116">**Value**</span></span>|<span data-ttu-id="62eff-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62eff-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62eff-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="62eff-118">Identifier</span></span>  <br/> |<span data-ttu-id="62eff-119">В этом поле должно быть значение 0xBEDEAFCD.</span><span class="sxs-lookup"><span data-stu-id="62eff-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="62eff-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="62eff-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="62eff-121">В этом поле должно иметь значение 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="62eff-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="62eff-122">Версия</span><span class="sxs-lookup"><span data-stu-id="62eff-122">Version</span></span>  <br/> |<span data-ttu-id="62eff-123">В этом поле должно иметь значение 3.</span><span class="sxs-lookup"><span data-stu-id="62eff-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="62eff-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="62eff-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="62eff-125">Количество записей, выполните.</span><span class="sxs-lookup"><span data-stu-id="62eff-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="62eff-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="62eff-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="62eff-127">В этом поле должно иметь значение 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="62eff-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="62eff-128">Заголовок следуют записи **RecordsCount** значений 32-разрядная версия, определенного как:</span><span class="sxs-lookup"><span data-stu-id="62eff-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="62eff-129">**Значение**</span><span class="sxs-lookup"><span data-stu-id="62eff-129">**Value**</span></span>|<span data-ttu-id="62eff-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62eff-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62eff-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="62eff-131">StartTime</span></span>  <br/> |<span data-ttu-id="62eff-132">Время начала собрания объекта в минут, начиная с полуночи 1 января 1601 UTC.</span><span class="sxs-lookup"><span data-stu-id="62eff-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="62eff-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="62eff-133">EndTime</span></span>  <br/> |<span data-ttu-id="62eff-134">Время окончания собрания объекта в минут, начиная с полуночи 1 января 1601 UTC.</span><span class="sxs-lookup"><span data-stu-id="62eff-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="62eff-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="62eff-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="62eff-136">Размер в байтах, поля GlobalObjectId.</span><span class="sxs-lookup"><span data-stu-id="62eff-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="62eff-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="62eff-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="62eff-138">Представляет значение свойства **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) данная запись собрания.</span><span class="sxs-lookup"><span data-stu-id="62eff-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="62eff-139">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="62eff-139">UserName</span></span>  <br/> |<span data-ttu-id="62eff-140">Первые два байта являются длина строки PT_STRING8, исходя из.</span><span class="sxs-lookup"><span data-stu-id="62eff-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="62eff-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="62eff-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62eff-142">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="62eff-142">Protocol specifications</span></span>

<span data-ttu-id="62eff-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62eff-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62eff-144">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="62eff-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62eff-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62eff-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62eff-146">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="62eff-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62eff-147">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="62eff-147">Header files</span></span>

<span data-ttu-id="62eff-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62eff-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="62eff-149">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="62eff-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="62eff-150">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="62eff-150">Mapitags.h</span></span>
  
> <span data-ttu-id="62eff-151">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="62eff-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62eff-152">См. также</span><span class="sxs-lookup"><span data-stu-id="62eff-152">See also</span></span>



[<span data-ttu-id="62eff-153">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="62eff-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62eff-154">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="62eff-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62eff-155">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="62eff-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62eff-156">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="62eff-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

