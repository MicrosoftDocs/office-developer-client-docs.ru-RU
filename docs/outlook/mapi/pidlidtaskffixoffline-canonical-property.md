---
title: Каноническое свойство PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303040"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="5ee47-103">Каноническое свойство PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="5ee47-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="5ee47-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ee47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ee47-105">Указывает точность свойства **диспидтасковнер** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5ee47-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ee47-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5ee47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ee47-107">диспидтаскффиксоффлине</span><span class="sxs-lookup"><span data-stu-id="5ee47-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="5ee47-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5ee47-108">Property set:</span></span>  <br/> |<span data-ttu-id="5ee47-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="5ee47-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="5ee47-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="5ee47-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5ee47-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="5ee47-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="5ee47-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5ee47-112">Data type:</span></span>  <br/> |<span data-ttu-id="5ee47-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5ee47-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5ee47-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5ee47-114">Area:</span></span>  <br/> |<span data-ttu-id="5ee47-115">Задача</span><span class="sxs-lookup"><span data-stu-id="5ee47-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ee47-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ee47-116">Remarks</span></span>

<span data-ttu-id="5ee47-117">Если свойство **диспидтаскффиксоффлине** имеет значение false или не задано, то значение свойства **диспидтасковнер** является правильным.</span><span class="sxs-lookup"><span data-stu-id="5ee47-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="5ee47-118">Если для **диспидтаскффиксоффлине** задано значение true, клиент не может определить точное значение для **диспидтасковнер**.</span><span class="sxs-lookup"><span data-stu-id="5ee47-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="5ee47-119">В этом случае клиент может задать **диспидтасковнер** в качестве имени универсального владельца, например "Unknown".</span><span class="sxs-lookup"><span data-stu-id="5ee47-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="5ee47-120">Тем не менее, если клиент встречает значение **диспидтаскффиксоффлине** в true и может определить точное имя владельца, клиент должен обновить **диспидтасковнер** и задать для **диспидтаскффиксоффлине** значение false.</span><span class="sxs-lookup"><span data-stu-id="5ee47-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5ee47-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ee47-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ee47-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5ee47-122">Protocol specifications</span></span>

<span data-ttu-id="5ee47-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ee47-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ee47-124">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5ee47-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ee47-125">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ee47-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ee47-126">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="5ee47-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="5ee47-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5ee47-127">Header files</span></span>

<span data-ttu-id="5ee47-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5ee47-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ee47-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5ee47-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ee47-130">См. также</span><span class="sxs-lookup"><span data-stu-id="5ee47-130">See also</span></span>



[<span data-ttu-id="5ee47-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ee47-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ee47-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5ee47-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ee47-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5ee47-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ee47-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5ee47-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

