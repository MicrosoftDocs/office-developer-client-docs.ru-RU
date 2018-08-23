---
title: Каноническое свойство PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f20c3e988c0a0461a966a109a8d345c22e1fccee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585740"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="b376c-103">Каноническое свойство PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="b376c-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="b376c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b376c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b376c-105">Рекомендации по оптимизации о получателей задачи.</span><span class="sxs-lookup"><span data-stu-id="b376c-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b376c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b376c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b376c-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="b376c-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="b376c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b376c-108">Property set:</span></span>  <br/> |<span data-ttu-id="b376c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b376c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b376c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b376c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b376c-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="b376c-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="b376c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b376c-112">Data type:</span></span>  <br/> |<span data-ttu-id="b376c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b376c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b376c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b376c-114">Area:</span></span>  <br/> |<span data-ttu-id="b376c-115">Task</span><span class="sxs-lookup"><span data-stu-id="b376c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b376c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b376c-116">Remarks</span></span>

<span data-ttu-id="b376c-117">Если задано, это свойство должно быть присвоено побитовую операцию **или** ноль или более из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b376c-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="b376c-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b376c-118">**Name**</span></span>|<span data-ttu-id="b376c-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b376c-119">**Value**</span></span>|<span data-ttu-id="b376c-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b376c-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b376c-121">Sent</span><span class="sxs-lookup"><span data-stu-id="b376c-121">Sent</span></span>  <br/> |<span data-ttu-id="b376c-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b376c-122">0x00000001</span></span>  <br/> |<span data-ttu-id="b376c-123">Задача имеет несколько получателей.</span><span class="sxs-lookup"><span data-stu-id="b376c-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="b376c-124">Получено</span><span class="sxs-lookup"><span data-stu-id="b376c-124">Received</span></span>  <br/> |<span data-ttu-id="b376c-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b376c-125">0x00000002</span></span>  <br/> |<span data-ttu-id="b376c-126">Несмотря на то, что подсказка отправлено не задан, клиент обнаружил, что задачи несколько получателей.</span><span class="sxs-lookup"><span data-stu-id="b376c-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="b376c-127">Резерв</span><span class="sxs-lookup"><span data-stu-id="b376c-127">Reserved</span></span>  <br/> |<span data-ttu-id="b376c-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b376c-128">0x00000004</span></span>  <br/> |<span data-ttu-id="b376c-129">Это значение зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="b376c-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b376c-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b376c-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b376c-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b376c-131">Protocol specifications</span></span>

<span data-ttu-id="b376c-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b376c-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b376c-133">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b376c-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b376c-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b376c-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b376c-135">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="b376c-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b376c-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b376c-136">Header files</span></span>

<span data-ttu-id="b376c-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b376c-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="b376c-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b376c-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b376c-139">См. также</span><span class="sxs-lookup"><span data-stu-id="b376c-139">See also</span></span>



[<span data-ttu-id="b376c-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b376c-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b376c-141">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b376c-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b376c-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b376c-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b376c-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b376c-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

