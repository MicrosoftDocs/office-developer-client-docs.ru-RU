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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382801"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="044f4-103">Каноническое свойство PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="044f4-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="044f4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="044f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="044f4-105">Указывает количество времени, в минутах, что необходима для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="044f4-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="044f4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="044f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="044f4-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="044f4-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="044f4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="044f4-108">Property set:</span></span>  <br/> |<span data-ttu-id="044f4-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="044f4-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="044f4-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="044f4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="044f4-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="044f4-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="044f4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="044f4-112">Data type:</span></span>  <br/> |<span data-ttu-id="044f4-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="044f4-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="044f4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="044f4-114">Area:</span></span>  <br/> |<span data-ttu-id="044f4-115">Task</span><span class="sxs-lookup"><span data-stu-id="044f4-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="044f4-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="044f4-116">Remarks</span></span>

<span data-ttu-id="044f4-117">Значение должно быть больше или равно 0 и меньше, чем 0x5AE980DF (1,525,252,319), где 480 минут равно один день и 2400 минут равно 1 неделя (8 часов рабочего дня и пять дней в неделе).</span><span class="sxs-lookup"><span data-stu-id="044f4-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="044f4-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="044f4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="044f4-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="044f4-119">Protocol specifications</span></span>

<span data-ttu-id="044f4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="044f4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="044f4-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="044f4-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="044f4-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="044f4-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="044f4-123">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="044f4-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="044f4-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="044f4-124">Header files</span></span>

<span data-ttu-id="044f4-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="044f4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="044f4-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="044f4-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="044f4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="044f4-127">See also</span></span>



[<span data-ttu-id="044f4-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="044f4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="044f4-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="044f4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="044f4-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="044f4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="044f4-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="044f4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

