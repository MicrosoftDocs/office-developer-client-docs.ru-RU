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
ms.openlocfilehash: 68ad6bd888594d09ab8e1dac050f8181341f7ee4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570785"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="311a8-103">Каноническое свойство PidLidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="311a8-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="311a8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="311a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="311a8-105">Указывает, является ли данное свойство повторяющейся объекта календаря с одно или несколько исключений и, по крайней мере одно исключение внедренные сообщения содержит по крайней мере один RecipientRow.</span><span class="sxs-lookup"><span data-stu-id="311a8-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="311a8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="311a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="311a8-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="311a8-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="311a8-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="311a8-108">Property set:</span></span>  <br/> |<span data-ttu-id="311a8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="311a8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="311a8-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="311a8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="311a8-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="311a8-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="311a8-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="311a8-112">Data type:</span></span>  <br/> |<span data-ttu-id="311a8-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="311a8-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="311a8-114">Область:</span><span class="sxs-lookup"><span data-stu-id="311a8-114">Area:</span></span>  <br/> |<span data-ttu-id="311a8-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="311a8-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="311a8-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="311a8-116">Remarks</span></span>

<span data-ttu-id="311a8-117">Значение FALSE или отсутствие этого свойства показывает, что объект календаря либо не имеет исключений, или ни один исключение внедренных сообщений не имеет RecipientRows.</span><span class="sxs-lookup"><span data-stu-id="311a8-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="311a8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="311a8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="311a8-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="311a8-119">Protocol specifications</span></span>

<span data-ttu-id="311a8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="311a8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="311a8-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="311a8-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="311a8-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="311a8-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="311a8-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="311a8-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="311a8-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="311a8-124">Header files</span></span>

<span data-ttu-id="311a8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="311a8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="311a8-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="311a8-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="311a8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="311a8-127">See also</span></span>



[<span data-ttu-id="311a8-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="311a8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="311a8-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="311a8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="311a8-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="311a8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="311a8-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="311a8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

