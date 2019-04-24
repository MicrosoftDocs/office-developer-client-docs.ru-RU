---
title: Каноническое свойство PidLidTaskEstimatedEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskEstimatedEffort
api_type:
- COM
ms.assetid: c84167d8-f726-45c6-9b21-bcde64473148
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5700ab6baaab2a5e73448582a855e6f243d5361d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303047"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="846b8-103">Каноническое свойство PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="846b8-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="846b8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="846b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="846b8-105">Указывает количество времени (в минутах), в течение которого пользователь ожидает выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="846b8-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="846b8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="846b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="846b8-107">Диспидтаскестиматедеффорт</span><span class="sxs-lookup"><span data-stu-id="846b8-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="846b8-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="846b8-108">Property set:</span></span>  <br/> |<span data-ttu-id="846b8-109">Псетид_таск</span><span class="sxs-lookup"><span data-stu-id="846b8-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="846b8-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="846b8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="846b8-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="846b8-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="846b8-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="846b8-112">Data type:</span></span>  <br/> |<span data-ttu-id="846b8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="846b8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="846b8-114">Область:</span><span class="sxs-lookup"><span data-stu-id="846b8-114">Area:</span></span>  <br/> |<span data-ttu-id="846b8-115">Задача</span><span class="sxs-lookup"><span data-stu-id="846b8-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="846b8-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="846b8-116">Remarks</span></span>

<span data-ttu-id="846b8-117">Значение должно быть больше или равно 0 и меньше, чем 0x5AE980DF (1 525 252 319), где 480 минут равно 1 день и 2400 минут равно одной неделе (восемь часов в рабочем дне и пять дней в рабочей неделе).</span><span class="sxs-lookup"><span data-stu-id="846b8-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="846b8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="846b8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="846b8-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="846b8-119">Protocol specifications</span></span>

<span data-ttu-id="846b8-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="846b8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="846b8-121">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="846b8-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="846b8-122">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="846b8-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="846b8-123">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="846b8-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="846b8-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="846b8-124">Header files</span></span>

<span data-ttu-id="846b8-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="846b8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="846b8-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="846b8-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="846b8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="846b8-127">See also</span></span>



[<span data-ttu-id="846b8-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="846b8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="846b8-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="846b8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="846b8-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="846b8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="846b8-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="846b8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

