---
title: Каноническое свойство PidLidFExceptionalAttendees
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 544b5b5ac945eeedf787af0e311491da1f9d0217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327477"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="95082-103">Каноническое свойство PidLidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="95082-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="95082-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95082-105">Указывает, является ли это свойство повторяющимся объектом календаря с одним или более исключениями, и по крайней мере одно из встроенных сообщений исключений имеет по крайней мере одно RecipientRow.</span><span class="sxs-lookup"><span data-stu-id="95082-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95082-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="95082-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95082-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="95082-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="95082-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="95082-108">Property set:</span></span>  <br/> |<span data-ttu-id="95082-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="95082-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="95082-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="95082-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="95082-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="95082-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="95082-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="95082-112">Data type:</span></span>  <br/> |<span data-ttu-id="95082-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="95082-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="95082-114">Область:</span><span class="sxs-lookup"><span data-stu-id="95082-114">Area:</span></span>  <br/> |<span data-ttu-id="95082-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="95082-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95082-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="95082-116">Remarks</span></span>

<span data-ttu-id="95082-117">Значение FALSE или отсутствие этого свойства указывает на то, что объект календаря не имеет исключений или ни одно из встроенных сообщений исключений не имеет RecipientRows.</span><span class="sxs-lookup"><span data-stu-id="95082-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="95082-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="95082-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95082-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="95082-119">Protocol specifications</span></span>

<span data-ttu-id="95082-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95082-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95082-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="95082-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="95082-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95082-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95082-123">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="95082-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95082-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="95082-124">Header files</span></span>

<span data-ttu-id="95082-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95082-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="95082-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="95082-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95082-127">См. также</span><span class="sxs-lookup"><span data-stu-id="95082-127">See also</span></span>



[<span data-ttu-id="95082-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95082-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95082-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95082-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95082-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="95082-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95082-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="95082-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

