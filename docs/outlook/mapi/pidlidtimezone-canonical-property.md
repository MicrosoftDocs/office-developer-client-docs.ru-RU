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
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319273"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="9347f-103">Каноническое свойство PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="9347f-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="9347f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9347f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9347f-105">Указывает сведения о часовом поясе повторяющегося собрания.</span><span class="sxs-lookup"><span data-stu-id="9347f-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9347f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9347f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9347f-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="9347f-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="9347f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9347f-108">Property set:</span></span>  <br/> |<span data-ttu-id="9347f-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="9347f-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="9347f-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="9347f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9347f-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="9347f-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="9347f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9347f-112">Data type:</span></span>  <br/> |<span data-ttu-id="9347f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9347f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9347f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9347f-114">Area:</span></span>  <br/> |<span data-ttu-id="9347f-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="9347f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9347f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9347f-116">Remarks</span></span>

<span data-ttu-id="9347f-117">Это свойство считывается только в том случае, если свойство **dispidApptRecur** ([PidLidAppointmentRecur)](pidlidappointmentrecur-canonical-property.md)не за установлено, но если свойство **LID_IS_RECURRING** ([PidLidIsRecurring)](pidlidisrecurring-canonical-property.md)имеет true, а свойство **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) — FALSE.</span><span class="sxs-lookup"><span data-stu-id="9347f-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="9347f-118">В нижней части WORD индекс указывается в таблице, которая содержит сведения о часовом поясе.</span><span class="sxs-lookup"><span data-stu-id="9347f-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="9347f-119">Из верхней части WORD считыется только самый высокий бит.</span><span class="sxs-lookup"><span data-stu-id="9347f-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="9347f-120">Если этот бит установлен, то часовой пояс, на который ссылается ссылка, не будет соблюдать летнее время (DST), в противном случае будут следовать даты DST, подробные [в [MS-OXOCAL].](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9347f-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9347f-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9347f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9347f-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9347f-122">Protocol specifications</span></span>

<span data-ttu-id="9347f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9347f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9347f-124">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="9347f-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9347f-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9347f-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9347f-126">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9347f-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9347f-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="9347f-127">Header files</span></span>

<span data-ttu-id="9347f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9347f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9347f-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9347f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9347f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9347f-130">See also</span></span>



[<span data-ttu-id="9347f-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9347f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9347f-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9347f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9347f-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9347f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9347f-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9347f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

