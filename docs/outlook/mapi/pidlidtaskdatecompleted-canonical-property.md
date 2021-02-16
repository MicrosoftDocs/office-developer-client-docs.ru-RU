---
title: Каноническое свойство PidLidTaskDateCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3096e7ab2133d2984be0534cb091d61d2c7157bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303215"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="c33aa-103">Каноническое свойство PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="c33aa-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="c33aa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c33aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c33aa-105">Указывает дату завершения задачи пользователем.</span><span class="sxs-lookup"><span data-stu-id="c33aa-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c33aa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c33aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c33aa-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="c33aa-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="c33aa-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c33aa-108">Property set:</span></span>  <br/> |<span data-ttu-id="c33aa-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c33aa-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c33aa-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c33aa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c33aa-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="c33aa-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="c33aa-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c33aa-112">Data type:</span></span>  <br/> |<span data-ttu-id="c33aa-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c33aa-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c33aa-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c33aa-114">Area:</span></span>  <br/> |<span data-ttu-id="c33aa-115">Task</span><span class="sxs-lookup"><span data-stu-id="c33aa-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c33aa-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c33aa-116">Remarks</span></span>

<span data-ttu-id="c33aa-117">Если этот элемент заданной, это свойство должно иметь компонент времени в полночь в локальном часовом поясе, преобразованный в UTC.</span><span class="sxs-lookup"><span data-stu-id="c33aa-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c33aa-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c33aa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c33aa-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c33aa-119">Protocol specifications</span></span>

<span data-ttu-id="c33aa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c33aa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c33aa-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="c33aa-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c33aa-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c33aa-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c33aa-123">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="c33aa-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="c33aa-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c33aa-124">Header files</span></span>

<span data-ttu-id="c33aa-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c33aa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c33aa-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c33aa-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c33aa-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c33aa-127">See also</span></span>



[<span data-ttu-id="c33aa-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c33aa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c33aa-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c33aa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c33aa-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c33aa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c33aa-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c33aa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

