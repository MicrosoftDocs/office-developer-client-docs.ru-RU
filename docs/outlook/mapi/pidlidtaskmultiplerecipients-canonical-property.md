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
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360069"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="e46d1-103">Каноническое свойство PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="e46d1-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="e46d1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e46d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e46d1-105">Предоставляет подсказки по оптимизации для получателей задачи.</span><span class="sxs-lookup"><span data-stu-id="e46d1-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e46d1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e46d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e46d1-107">диспидтаскмултреЦипс</span><span class="sxs-lookup"><span data-stu-id="e46d1-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="e46d1-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="e46d1-108">Property set:</span></span>  <br/> |<span data-ttu-id="e46d1-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e46d1-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e46d1-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="e46d1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e46d1-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="e46d1-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="e46d1-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e46d1-112">Data type:</span></span>  <br/> |<span data-ttu-id="e46d1-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e46d1-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e46d1-114">Область:</span><span class="sxs-lookup"><span data-stu-id="e46d1-114">Area:</span></span>  <br/> |<span data-ttu-id="e46d1-115">Задача</span><span class="sxs-lookup"><span data-stu-id="e46d1-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e46d1-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e46d1-116">Remarks</span></span>

<span data-ttu-id="e46d1-117">Если этот параметр установлен, для этого свойства должно быть задано **побитовое действие or с** нулевым или более из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e46d1-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="e46d1-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="e46d1-118">**Name**</span></span>|<span data-ttu-id="e46d1-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="e46d1-119">**Value**</span></span>|<span data-ttu-id="e46d1-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e46d1-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e46d1-121">Sent</span><span class="sxs-lookup"><span data-stu-id="e46d1-121">Sent</span></span>  <br/> |<span data-ttu-id="e46d1-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e46d1-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e46d1-123">Задача имеет несколько основных получателей.</span><span class="sxs-lookup"><span data-stu-id="e46d1-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="e46d1-124">ПОЛУЧЕНО</span><span class="sxs-lookup"><span data-stu-id="e46d1-124">Received</span></span>  <br/> |<span data-ttu-id="e46d1-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e46d1-125">0x00000002</span></span>  <br/> |<span data-ttu-id="e46d1-126">Хотя подсказка отправления отсутствует, клиент обнаружил, что у задачи несколько основных получателей.</span><span class="sxs-lookup"><span data-stu-id="e46d1-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="e46d1-127">Reserved</span><span class="sxs-lookup"><span data-stu-id="e46d1-127">Reserved</span></span>  <br/> |<span data-ttu-id="e46d1-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e46d1-128">0x00000004</span></span>  <br/> |<span data-ttu-id="e46d1-129">Это значение зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e46d1-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e46d1-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e46d1-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e46d1-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e46d1-131">Protocol specifications</span></span>

<span data-ttu-id="e46d1-132">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e46d1-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e46d1-133">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e46d1-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e46d1-134">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e46d1-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e46d1-135">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="e46d1-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e46d1-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e46d1-136">Header files</span></span>

<span data-ttu-id="e46d1-137">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e46d1-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e46d1-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e46d1-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e46d1-139">См. также</span><span class="sxs-lookup"><span data-stu-id="e46d1-139">See also</span></span>



[<span data-ttu-id="e46d1-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e46d1-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e46d1-141">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e46d1-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e46d1-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e46d1-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e46d1-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e46d1-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

