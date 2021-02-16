---
title: Каноническое свойство PidLidAppointmentReplyTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyTime
api_type:
- COM
ms.assetid: 80a2608b-fc44-455a-86be-d6235caba99e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ba79498569c544d1b0ee22e968477d5b68812c09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331789"
---
# <a name="pidlidappointmentreplytime-canonical-property"></a><span data-ttu-id="b128b-103">Каноническое свойство PidLidAppointmentReplyTime</span><span class="sxs-lookup"><span data-stu-id="b128b-103">PidLidAppointmentReplyTime Canonical Property</span></span>

  
  
<span data-ttu-id="b128b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b128b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b128b-105">Указывает дату и время, когда участник ответил на полученный запрос на собрание или обновление собрания.</span><span class="sxs-lookup"><span data-stu-id="b128b-105">Specifies the date and time when the attendee responded to a received meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b128b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b128b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b128b-107">dispidApptReplyTime</span><span class="sxs-lookup"><span data-stu-id="b128b-107">dispidApptReplyTime</span></span>  <br/> |
|<span data-ttu-id="b128b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b128b-108">Property set:</span></span>  <br/> |<span data-ttu-id="b128b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b128b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b128b-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b128b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b128b-111">0x00008220</span><span class="sxs-lookup"><span data-stu-id="b128b-111">0x00008220</span></span>  <br/> |
|<span data-ttu-id="b128b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b128b-112">Data type:</span></span>  <br/> |<span data-ttu-id="b128b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b128b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b128b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b128b-114">Area:</span></span>  <br/> |<span data-ttu-id="b128b-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="b128b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b128b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b128b-116">Remarks</span></span>

<span data-ttu-id="b128b-117">Значение должно быть указано в UTC.</span><span class="sxs-lookup"><span data-stu-id="b128b-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b128b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b128b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b128b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b128b-119">Protocol specifications</span></span>

<span data-ttu-id="b128b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b128b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b128b-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="b128b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b128b-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b128b-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b128b-123">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b128b-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b128b-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="b128b-124">Header files</span></span>

<span data-ttu-id="b128b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b128b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b128b-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b128b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b128b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b128b-127">See also</span></span>



[<span data-ttu-id="b128b-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b128b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b128b-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b128b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b128b-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b128b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b128b-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b128b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

