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
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="0edf5-103">Каноническое свойство PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="0edf5-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="0edf5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0edf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0edf5-105">Указывает точность свойства **dispidTaskOwner** ([PidLidTaskOwner).](pidlidtaskowner-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0edf5-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0edf5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0edf5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0edf5-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="0edf5-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="0edf5-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0edf5-108">Property set:</span></span>  <br/> |<span data-ttu-id="0edf5-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0edf5-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0edf5-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0edf5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0edf5-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="0edf5-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="0edf5-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0edf5-112">Data type:</span></span>  <br/> |<span data-ttu-id="0edf5-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0edf5-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0edf5-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0edf5-114">Area:</span></span>  <br/> |<span data-ttu-id="0edf5-115">Task</span><span class="sxs-lookup"><span data-stu-id="0edf5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0edf5-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0edf5-116">Remarks</span></span>

<span data-ttu-id="0edf5-117">Если свойство **dispidTaskFFixOffline** имеет значение FALSE или не замечено, значение свойства **dispidTaskOwner** является правильным.</span><span class="sxs-lookup"><span data-stu-id="0edf5-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="0edf5-118">Если **для dispidTaskFFixOffline** установлено значение TRUE, клиент не может определить точное значение **для dispidTaskOwner.**</span><span class="sxs-lookup"><span data-stu-id="0edf5-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="0edf5-119">В этом случае клиент может установить **для dispidTaskOwner** универсальное имя владельца, например "Unknown".</span><span class="sxs-lookup"><span data-stu-id="0edf5-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="0edf5-120">Однако если клиент сталкивается со значением **dispidTaskFFixOffline** true и может определить точное имя владельца, клиент должен обновить **dispidTaskOwner** и установить **для dispidTaskFFixOffline** значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="0edf5-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0edf5-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0edf5-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0edf5-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0edf5-122">Protocol specifications</span></span>

<span data-ttu-id="0edf5-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0edf5-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0edf5-124">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="0edf5-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0edf5-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0edf5-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0edf5-126">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="0edf5-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="0edf5-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="0edf5-127">Header files</span></span>

<span data-ttu-id="0edf5-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0edf5-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0edf5-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0edf5-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0edf5-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0edf5-130">See also</span></span>



[<span data-ttu-id="0edf5-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0edf5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0edf5-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0edf5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0edf5-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0edf5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0edf5-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0edf5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

