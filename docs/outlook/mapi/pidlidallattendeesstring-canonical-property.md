---
title: Каноническое свойство PidLidAllAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: a9580428cd985902d3af6320dd754947565b74e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810099"
---
# <a name="pidlidallattendeesstring-canonical-property"></a><span data-ttu-id="3b562-103">Каноническое свойство PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="3b562-103">PidLidAllAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="3b562-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b562-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b562-105">Указывает список всех участников, кроме организатора, включая ресурсы и отправить участников.</span><span class="sxs-lookup"><span data-stu-id="3b562-105">Specifies a list of all the attendees except for the organizer, including resources and unsendable attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b562-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3b562-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b562-107">dispidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="3b562-107">dispidAllAttendeesString</span></span>  <br/> |
|<span data-ttu-id="3b562-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="3b562-108">Property set:</span></span>  <br/> |<span data-ttu-id="3b562-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="3b562-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="3b562-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="3b562-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3b562-111">0x00008238</span><span class="sxs-lookup"><span data-stu-id="3b562-111">0x00008238</span></span>  <br/> |
|<span data-ttu-id="3b562-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3b562-112">Data type:</span></span>  <br/> |<span data-ttu-id="3b562-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3b562-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3b562-114">Области:</span><span class="sxs-lookup"><span data-stu-id="3b562-114">Area:</span></span>  <br/> |<span data-ttu-id="3b562-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="3b562-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b562-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b562-116">Remarks</span></span>

<span data-ttu-id="3b562-117">Значение для каждого участника — отображаемое имя участника.</span><span class="sxs-lookup"><span data-stu-id="3b562-117">The value for each attendee is the attendee's display name.</span></span> <span data-ttu-id="3b562-118">Отдельные записи должны быть разделены точкой с запятой, а затем пробел.</span><span class="sxs-lookup"><span data-stu-id="3b562-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="3b562-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="3b562-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3b562-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3b562-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b562-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3b562-121">Protocol specifications</span></span>

<span data-ttu-id="3b562-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b562-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b562-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3b562-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b562-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b562-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b562-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="3b562-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b562-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3b562-126">Header files</span></span>

<span data-ttu-id="3b562-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b562-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b562-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3b562-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b562-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3b562-129">See also</span></span>



[<span data-ttu-id="3b562-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3b562-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b562-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3b562-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b562-132">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="3b562-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b562-133">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="3b562-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

