---
title: Каноническое свойство PidLidIsRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390851"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="bb346-103">Каноническое свойство PidLidIsRecurring</span><span class="sxs-lookup"><span data-stu-id="bb346-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="bb346-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb346-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb346-105">Указывает, связан ли объект с серии повторяющихся.</span><span class="sxs-lookup"><span data-stu-id="bb346-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb346-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bb346-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb346-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="bb346-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="bb346-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="bb346-108">Property set:</span></span>  <br/> |<span data-ttu-id="bb346-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="bb346-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="bb346-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="bb346-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bb346-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="bb346-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="bb346-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bb346-112">Data type:</span></span>  <br/> |<span data-ttu-id="bb346-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bb346-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bb346-114">Область:</span><span class="sxs-lookup"><span data-stu-id="bb346-114">Area:</span></span>  <br/> |<span data-ttu-id="bb346-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="bb346-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb346-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="bb346-116">Remarks</span></span>

<span data-ttu-id="bb346-117">Значение TRUE указывает, что объект представляет серии повторяющихся или исключение (включая потерянного экземпляра).</span><span class="sxs-lookup"><span data-stu-id="bb346-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="bb346-118">Значение FALSE или отсутствие этого свойства указывает, что объект представляет один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="bb346-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="bb346-119">Обратите внимание на разницу между этого свойства и свойства **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bb346-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb346-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bb346-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb346-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bb346-121">Protocol specifications</span></span>

<span data-ttu-id="bb346-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb346-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb346-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bb346-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb346-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb346-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb346-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="bb346-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb346-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bb346-126">Header files</span></span>

<span data-ttu-id="bb346-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb346-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb346-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bb346-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb346-129">См. также</span><span class="sxs-lookup"><span data-stu-id="bb346-129">See also</span></span>



[<span data-ttu-id="bb346-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bb346-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb346-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bb346-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb346-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bb346-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb346-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bb346-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

