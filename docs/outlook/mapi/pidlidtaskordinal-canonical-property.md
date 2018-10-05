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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387736"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="16144-103">Каноническое свойство PidLidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="16144-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="16144-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16144-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16144-105">Предоставляет поддержки для пользовательских задач сортировки.</span><span class="sxs-lookup"><span data-stu-id="16144-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16144-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="16144-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16144-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="16144-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="16144-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="16144-108">Property set:</span></span>  <br/> |<span data-ttu-id="16144-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="16144-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="16144-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="16144-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="16144-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="16144-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="16144-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="16144-112">Data type:</span></span>  <br/> |<span data-ttu-id="16144-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="16144-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="16144-114">Область:</span><span class="sxs-lookup"><span data-stu-id="16144-114">Area:</span></span>  <br/> |<span data-ttu-id="16144-115">Task</span><span class="sxs-lookup"><span data-stu-id="16144-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16144-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="16144-116">Remarks</span></span>

<span data-ttu-id="16144-117">Это свойство можно оставить неопределенные.</span><span class="sxs-lookup"><span data-stu-id="16144-117">This property may be left unset.</span></span> <span data-ttu-id="16144-118">Если задано, его значение должно быть больше, чем «0x800186A0» (-2,147,383,648) и меньше, чем «0x7FFE7960» (2,147,383,648) и должно быть уникальным во задачи в той же папке.</span><span class="sxs-lookup"><span data-stu-id="16144-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="16144-119">Каждый раз, когда клиент этому свойству присваивается значение меньше отрицательное текущее значение свойства **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) к папке, необходимо также обновления **PR_ORDINAL_MOST** в общей папке.</span><span class="sxs-lookup"><span data-stu-id="16144-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="16144-120">Свойство **PR_ORDINAL_MOST** папки предоставляет эффективный способ определения уникальное значение между задачами в той же папке.</span><span class="sxs-lookup"><span data-stu-id="16144-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="16144-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="16144-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="16144-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="16144-122">Protocol specifications</span></span>

<span data-ttu-id="16144-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16144-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16144-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="16144-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="16144-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16144-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16144-126">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="16144-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="16144-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="16144-127">Header files</span></span>

<span data-ttu-id="16144-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16144-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="16144-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="16144-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16144-130">См. также</span><span class="sxs-lookup"><span data-stu-id="16144-130">See also</span></span>



[<span data-ttu-id="16144-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16144-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16144-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16144-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16144-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="16144-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16144-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="16144-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

