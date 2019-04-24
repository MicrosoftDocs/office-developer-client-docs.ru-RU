---
title: Каноническое свойство PidLidToDoOrdinalDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345278"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="19af5-103">Каноническое свойство PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="19af5-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="19af5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19af5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19af5-105">Определяет порядок сортировки объектов в объединенном списке дел.</span><span class="sxs-lookup"><span data-stu-id="19af5-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19af5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="19af5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19af5-107">Диспидтодурдиналдате</span><span class="sxs-lookup"><span data-stu-id="19af5-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="19af5-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="19af5-108">Property set:</span></span>  <br/> |<span data-ttu-id="19af5-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="19af5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="19af5-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="19af5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="19af5-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="19af5-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="19af5-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="19af5-112">Data type:</span></span>  <br/> |<span data-ttu-id="19af5-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="19af5-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="19af5-114">Область:</span><span class="sxs-lookup"><span data-stu-id="19af5-114">Area:</span></span>  <br/> |<span data-ttu-id="19af5-115">Задача</span><span class="sxs-lookup"><span data-stu-id="19af5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19af5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19af5-116">Remarks</span></span>

<span data-ttu-id="19af5-117">Если объект помечен, для этого свойства должно быть задано текущее время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="19af5-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="19af5-118">Если клиент разрешает пользователям изменять порядок задач в объединенном списке задач с помощью перетаскивания или других механизмов, они могут использовать любой подходящий алгоритм, чтобы определить новое значение этого свойства, чтобы задача отображалась в правильном месте, если это свойство используется в качестве СОР поле тинг.</span><span class="sxs-lookup"><span data-stu-id="19af5-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="19af5-119">Если это свойство используется для сортировки объектов и результатов сортировки, то свойство **диспидтодосубординал** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) используется в качестве несвязанного средства разбивки.</span><span class="sxs-lookup"><span data-stu-id="19af5-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="19af5-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="19af5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19af5-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="19af5-121">Protocol specifications</span></span>

<span data-ttu-id="19af5-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19af5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19af5-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="19af5-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19af5-124">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19af5-124">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19af5-125">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="19af5-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19af5-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="19af5-126">Header files</span></span>

<span data-ttu-id="19af5-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="19af5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="19af5-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="19af5-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19af5-129">См. также</span><span class="sxs-lookup"><span data-stu-id="19af5-129">See also</span></span>



[<span data-ttu-id="19af5-130">Каноническое свойство PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="19af5-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="19af5-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="19af5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19af5-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="19af5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19af5-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="19af5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19af5-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="19af5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

