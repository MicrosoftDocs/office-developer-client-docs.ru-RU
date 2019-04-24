---
title: Каноническое свойство PidLidTaskOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357962"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="af523-103">Каноническое свойство PidLidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="af523-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="af523-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af523-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af523-105">Предоставляет помощь в настраиваемых задачах сортировки.</span><span class="sxs-lookup"><span data-stu-id="af523-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af523-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="af523-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af523-107">Диспидтаскординал</span><span class="sxs-lookup"><span data-stu-id="af523-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="af523-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="af523-108">Property set:</span></span>  <br/> |<span data-ttu-id="af523-109">Псетид_таск</span><span class="sxs-lookup"><span data-stu-id="af523-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="af523-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="af523-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="af523-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="af523-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="af523-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="af523-112">Data type:</span></span>  <br/> |<span data-ttu-id="af523-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="af523-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="af523-114">Область:</span><span class="sxs-lookup"><span data-stu-id="af523-114">Area:</span></span>  <br/> |<span data-ttu-id="af523-115">Задача</span><span class="sxs-lookup"><span data-stu-id="af523-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af523-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="af523-116">Remarks</span></span>

<span data-ttu-id="af523-117">Это свойство может остаться неопределенным.</span><span class="sxs-lookup"><span data-stu-id="af523-117">This property may be left unset.</span></span> <span data-ttu-id="af523-118">Если этот параметр установлен, его значение должно быть больше, чем "0x800186A0" (-2 147 383 648) и меньше "0x7FFE7960" (2 147 383 648), и должно быть уникальным среди задач в одной папке.</span><span class="sxs-lookup"><span data-stu-id="af523-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="af523-119">Когда клиент задает для этого свойства число, меньшее, чем отрицательное значение свойства **пр_ординал_мост** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) папки, клиент должен также обновить **пр_ординал_мост** в папке.</span><span class="sxs-lookup"><span data-stu-id="af523-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="af523-120">Свойство **пр_ординал_мост** папки предоставляет эффективный способ определения уникального значения между задачами в одной папке.</span><span class="sxs-lookup"><span data-stu-id="af523-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="af523-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af523-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af523-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="af523-122">Protocol specifications</span></span>

<span data-ttu-id="af523-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af523-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af523-124">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="af523-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af523-125">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af523-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af523-126">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="af523-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="af523-127">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="af523-127">Header files</span></span>

<span data-ttu-id="af523-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="af523-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="af523-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="af523-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af523-130">См. также</span><span class="sxs-lookup"><span data-stu-id="af523-130">See also</span></span>



[<span data-ttu-id="af523-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af523-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af523-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="af523-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af523-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="af523-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af523-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="af523-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

