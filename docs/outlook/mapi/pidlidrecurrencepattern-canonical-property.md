---
title: Каноническое свойство PidLidRecurrencePattern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrencePattern
api_type:
- COM
ms.assetid: ac21ba98-f16b-4365-9134-bca7748189ee
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 94656a1444149efeb6e2e9cd3a239ff14fa46937
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810472"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="634b7-103">Каноническое свойство PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="634b7-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="634b7-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="634b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="634b7-105">Задает описание шаблона повторения объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="634b7-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="634b7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="634b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="634b7-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="634b7-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="634b7-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="634b7-108">Property set:</span></span>  <br/> |<span data-ttu-id="634b7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="634b7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="634b7-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="634b7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="634b7-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="634b7-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="634b7-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="634b7-112">Data type:</span></span>  <br/> |<span data-ttu-id="634b7-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="634b7-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="634b7-114">Области:</span><span class="sxs-lookup"><span data-stu-id="634b7-114">Area:</span></span>  <br/> |<span data-ttu-id="634b7-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="634b7-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="634b7-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="634b7-116">Remarks</span></span>

<span data-ttu-id="634b7-117">Если значение этого свойства, он должен иметь значение описание повторения, указанный в свойстве **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="634b7-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="634b7-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="634b7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="634b7-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="634b7-119">Protocol specifications</span></span>

<span data-ttu-id="634b7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="634b7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="634b7-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="634b7-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="634b7-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="634b7-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="634b7-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="634b7-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="634b7-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="634b7-124">Header files</span></span>

<span data-ttu-id="634b7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="634b7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="634b7-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="634b7-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="634b7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="634b7-127">See also</span></span>



[<span data-ttu-id="634b7-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="634b7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="634b7-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="634b7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="634b7-130">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="634b7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="634b7-131">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="634b7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

