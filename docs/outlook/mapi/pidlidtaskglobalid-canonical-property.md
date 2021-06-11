---
title: Каноническое свойство PidLidTaskGlobalId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskGlobalId
api_type:
- COM
ms.assetid: 369d8c78-3cf6-4a55-ba14-9da0377d6ccf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 295eb9dcc6da7b0fb6c6fd7ea0b73134ffaadb3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303019"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="aa3f3-103">Каноническое свойство PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="aa3f3-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="aa3f3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa3f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa3f3-105">Находит существующую задачу с помощью GUID после получения ответа задачи или обновления задачи.</span><span class="sxs-lookup"><span data-stu-id="aa3f3-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa3f3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="aa3f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa3f3-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="aa3f3-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="aa3f3-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="aa3f3-108">Property set:</span></span>  <br/> |<span data-ttu-id="aa3f3-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="aa3f3-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="aa3f3-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="aa3f3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="aa3f3-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="aa3f3-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="aa3f3-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="aa3f3-112">Data type:</span></span>  <br/> |<span data-ttu-id="aa3f3-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aa3f3-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aa3f3-114">Область:</span><span class="sxs-lookup"><span data-stu-id="aa3f3-114">Area:</span></span>  <br/> |<span data-ttu-id="aa3f3-115">Задача</span><span class="sxs-lookup"><span data-stu-id="aa3f3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa3f3-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa3f3-116">Remarks</span></span>

<span data-ttu-id="aa3f3-117">Это свойство остается неустановленным для ненаписаных задач.</span><span class="sxs-lookup"><span data-stu-id="aa3f3-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aa3f3-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="aa3f3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aa3f3-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="aa3f3-119">Protocol specifications</span></span>

<span data-ttu-id="aa3f3-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa3f3-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa3f3-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="aa3f3-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aa3f3-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa3f3-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa3f3-123">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="aa3f3-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aa3f3-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="aa3f3-124">Header files</span></span>

<span data-ttu-id="aa3f3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa3f3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa3f3-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="aa3f3-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa3f3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="aa3f3-127">See also</span></span>



[<span data-ttu-id="aa3f3-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aa3f3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa3f3-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aa3f3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa3f3-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="aa3f3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa3f3-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="aa3f3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

