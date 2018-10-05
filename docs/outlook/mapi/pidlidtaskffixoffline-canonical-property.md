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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386266"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="50317-103">Каноническое свойство PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="50317-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="50317-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50317-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50317-105">Указывает точность свойство **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="50317-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50317-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="50317-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50317-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="50317-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="50317-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="50317-108">Property set:</span></span>  <br/> |<span data-ttu-id="50317-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="50317-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="50317-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="50317-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="50317-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="50317-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="50317-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="50317-112">Data type:</span></span>  <br/> |<span data-ttu-id="50317-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="50317-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="50317-114">Область:</span><span class="sxs-lookup"><span data-stu-id="50317-114">Area:</span></span>  <br/> |<span data-ttu-id="50317-115">Task</span><span class="sxs-lookup"><span data-stu-id="50317-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50317-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="50317-116">Remarks</span></span>

<span data-ttu-id="50317-117">Если свойство **dispidTaskFFixOffline** имеет значение FALSE или не установлено, значение для свойства **dispidTaskOwner** является правильным.</span><span class="sxs-lookup"><span data-stu-id="50317-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="50317-118">Если **dispidTaskFFixOffline** имеет значение TRUE, клиент не может определить точное значение **dispidTaskOwner**.</span><span class="sxs-lookup"><span data-stu-id="50317-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="50317-119">В этом случае клиента можно включить **dispidTaskOwner** универсальный владелец имя, например, «Неизвестно».</span><span class="sxs-lookup"><span data-stu-id="50317-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="50317-120">Тем не менее если это клиент обнаруживает **dispidTaskFFixOffline** значение TRUE и можно определить имя владельца точных, клиент должен обновить **dispidTaskOwner** и **dispidTaskFFixOffline** задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="50317-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="50317-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="50317-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50317-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="50317-122">Protocol specifications</span></span>

<span data-ttu-id="50317-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50317-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50317-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="50317-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50317-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50317-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50317-126">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="50317-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="50317-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="50317-127">Header files</span></span>

<span data-ttu-id="50317-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50317-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="50317-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="50317-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50317-130">См. также</span><span class="sxs-lookup"><span data-stu-id="50317-130">See also</span></span>



[<span data-ttu-id="50317-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="50317-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50317-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="50317-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50317-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="50317-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50317-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="50317-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

