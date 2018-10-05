---
title: Каноническое свойство PidLidAttendeeCriticalChange
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAttendeeCriticalChange
api_type:
- COM
ms.assetid: 2b46966d-c63d-4241-92d4-001d6a674e97
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d6464a346d8543a128ec1af9f605667c6a51ca3c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399300"
---
# <a name="pidlidattendeecriticalchange-canonical-property"></a><span data-ttu-id="25354-103">Каноническое свойство PidLidAttendeeCriticalChange</span><span class="sxs-lookup"><span data-stu-id="25354-103">PidLidAttendeeCriticalChange Canonical Property</span></span>

  
  
<span data-ttu-id="25354-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25354-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25354-105">Указывает дату и время отправки объекта относящихся к собранию.</span><span class="sxs-lookup"><span data-stu-id="25354-105">Specifies the date and time when the meeting-related object was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25354-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="25354-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25354-107">LID_ATTENDEE_CRITICAL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="25354-107">LID_ATTENDEE_CRITICAL_CHANGE</span></span>  <br/> |
|<span data-ttu-id="25354-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="25354-108">Property set:</span></span>  <br/> |<span data-ttu-id="25354-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="25354-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="25354-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="25354-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25354-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="25354-111">0x00000001</span></span>  <br/> |
|<span data-ttu-id="25354-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="25354-112">Data type:</span></span>  <br/> |<span data-ttu-id="25354-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="25354-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="25354-114">Область:</span><span class="sxs-lookup"><span data-stu-id="25354-114">Area:</span></span>  <br/> |<span data-ttu-id="25354-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="25354-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25354-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="25354-116">Remarks</span></span>

<span data-ttu-id="25354-117">Значением должен быть указан в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="25354-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="25354-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="25354-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25354-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="25354-119">Protocol specifications</span></span>

<span data-ttu-id="25354-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25354-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25354-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="25354-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25354-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25354-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25354-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="25354-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25354-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="25354-124">Header files</span></span>

<span data-ttu-id="25354-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25354-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="25354-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="25354-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25354-127">См. также</span><span class="sxs-lookup"><span data-stu-id="25354-127">See also</span></span>



[<span data-ttu-id="25354-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="25354-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25354-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="25354-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25354-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="25354-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25354-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="25354-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

