---
title: Каноническое свойство PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 90dc35e72fc863ab12d9d6df9c54def7af788efd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568891"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="b8408-103">Каноническое свойство PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="b8408-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="b8408-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8408-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8408-105">Задает сведения о часовом поясе повторяющееся собрание.</span><span class="sxs-lookup"><span data-stu-id="b8408-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8408-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b8408-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8408-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="b8408-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="b8408-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b8408-108">Property set:</span></span>  <br/> |<span data-ttu-id="b8408-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="b8408-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="b8408-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b8408-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b8408-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="b8408-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="b8408-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b8408-112">Data type:</span></span>  <br/> |<span data-ttu-id="b8408-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b8408-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b8408-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b8408-114">Area:</span></span>  <br/> |<span data-ttu-id="b8408-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="b8408-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8408-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b8408-116">Remarks</span></span>

<span data-ttu-id="b8408-117">Это свойство читаются только в том случае, если свойство **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) не установлено, но если свойство **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) имеет значение TRUE и **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) свойство имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="b8408-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="b8408-118">Снижение WORD задает индекс в таблицу, содержащую сведения о часовом поясе.</span><span class="sxs-lookup"><span data-stu-id="b8408-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="b8408-119">Из верхней WORD читать только высший бит.</span><span class="sxs-lookup"><span data-stu-id="b8408-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="b8408-120">Если этот бит задан, выберите часовой пояс по ссылке не увидите, что следует делать летнего времени (летнее время), в противном случае — подробное описание даты перехода на летнее время в [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b8408-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b8408-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b8408-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8408-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b8408-122">Protocol specifications</span></span>

<span data-ttu-id="b8408-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8408-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8408-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b8408-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8408-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8408-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8408-126">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="b8408-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8408-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b8408-127">Header files</span></span>

<span data-ttu-id="b8408-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8408-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8408-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b8408-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8408-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b8408-130">See also</span></span>



[<span data-ttu-id="b8408-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b8408-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8408-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b8408-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8408-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b8408-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8408-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b8408-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

