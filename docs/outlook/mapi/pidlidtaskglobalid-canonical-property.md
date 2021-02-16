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
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="edc69-103">Каноническое свойство PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="edc69-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="edc69-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edc69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edc69-105">Находит существующую задачу, используя GUID, после получения ответа на задачу или обновления задачи.</span><span class="sxs-lookup"><span data-stu-id="edc69-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edc69-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="edc69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edc69-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="edc69-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="edc69-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="edc69-108">Property set:</span></span>  <br/> |<span data-ttu-id="edc69-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="edc69-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="edc69-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="edc69-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="edc69-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="edc69-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="edc69-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="edc69-112">Data type:</span></span>  <br/> |<span data-ttu-id="edc69-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="edc69-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="edc69-114">Область:</span><span class="sxs-lookup"><span data-stu-id="edc69-114">Area:</span></span>  <br/> |<span data-ttu-id="edc69-115">Task</span><span class="sxs-lookup"><span data-stu-id="edc69-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edc69-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="edc69-116">Remarks</span></span>

<span data-ttu-id="edc69-117">Это свойство не замечено для ненаписаных задач.</span><span class="sxs-lookup"><span data-stu-id="edc69-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edc69-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="edc69-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edc69-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="edc69-119">Protocol specifications</span></span>

<span data-ttu-id="edc69-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edc69-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edc69-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="edc69-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edc69-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edc69-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edc69-123">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="edc69-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edc69-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="edc69-124">Header files</span></span>

<span data-ttu-id="edc69-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edc69-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="edc69-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="edc69-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edc69-127">См. также</span><span class="sxs-lookup"><span data-stu-id="edc69-127">See also</span></span>



[<span data-ttu-id="edc69-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="edc69-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edc69-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="edc69-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edc69-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="edc69-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edc69-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="edc69-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

