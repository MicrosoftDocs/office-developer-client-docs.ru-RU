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
ms.openlocfilehash: 987188db4a3aceb4b065f59cdf449f943f68e70d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565321"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="f4fda-103">Каноническое свойство PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="f4fda-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="f4fda-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4fda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4fda-105">Указывает количество времени, в минутах, что необходима для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="f4fda-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4fda-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f4fda-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4fda-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="f4fda-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="f4fda-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f4fda-108">Property set:</span></span>  <br/> |<span data-ttu-id="f4fda-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f4fda-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f4fda-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="f4fda-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f4fda-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="f4fda-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="f4fda-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f4fda-112">Data type:</span></span>  <br/> |<span data-ttu-id="f4fda-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f4fda-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f4fda-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f4fda-114">Area:</span></span>  <br/> |<span data-ttu-id="f4fda-115">Task</span><span class="sxs-lookup"><span data-stu-id="f4fda-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4fda-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="f4fda-116">Remarks</span></span>

<span data-ttu-id="f4fda-117">Значение должно быть больше или равно 0 и меньше, чем 0x5AE980DF (1,525,252,319), где 480 минут равно один день и 2400 минут равно 1 неделя (8 часов рабочего дня и пять дней в неделе).</span><span class="sxs-lookup"><span data-stu-id="f4fda-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4fda-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f4fda-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4fda-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f4fda-119">Protocol specifications</span></span>

<span data-ttu-id="f4fda-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4fda-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4fda-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f4fda-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4fda-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4fda-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4fda-123">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="f4fda-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="f4fda-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f4fda-124">Header files</span></span>

<span data-ttu-id="f4fda-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4fda-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4fda-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f4fda-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4fda-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f4fda-127">See also</span></span>



[<span data-ttu-id="f4fda-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4fda-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4fda-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4fda-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4fda-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f4fda-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4fda-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f4fda-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

