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
ms.openlocfilehash: b19f36337459753e153a96021b1d70308b374bed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577761"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="80059-103">Каноническое свойство PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="80059-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="80059-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80059-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80059-105">Определяет порядок сортировки объектов в список дел консолидированной среды.</span><span class="sxs-lookup"><span data-stu-id="80059-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80059-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="80059-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80059-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="80059-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="80059-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="80059-108">Property set:</span></span>  <br/> |<span data-ttu-id="80059-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="80059-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="80059-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="80059-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="80059-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="80059-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="80059-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="80059-112">Data type:</span></span>  <br/> |<span data-ttu-id="80059-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="80059-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="80059-114">Область:</span><span class="sxs-lookup"><span data-stu-id="80059-114">Area:</span></span>  <br/> |<span data-ttu-id="80059-115">Task</span><span class="sxs-lookup"><span data-stu-id="80059-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80059-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="80059-116">Remarks</span></span>

<span data-ttu-id="80059-117">Когда объект имеет флаг, это свойство необходимо задать текущее время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="80059-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="80059-118">Если клиент позволяет пользователю изменять их порядок задач в списке консолидированной задач путем перетаскивания или другие механизмы, они могут использовать любой подходящий алгоритм для определения нового значения этого свойства, чтобы задачи отображается в нужное место, когда это свойство используется в качестве озрастанию поля области.</span><span class="sxs-lookup"><span data-stu-id="80059-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="80059-119">Когда это свойство используется для сортировки объектов и сортировка результатов в набор функций, как средства разбиения слов связывают используется свойство **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="80059-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80059-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="80059-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80059-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="80059-121">Protocol specifications</span></span>

<span data-ttu-id="80059-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80059-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80059-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="80059-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80059-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80059-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80059-125">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="80059-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80059-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="80059-126">Header files</span></span>

<span data-ttu-id="80059-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80059-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="80059-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="80059-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80059-129">См. также</span><span class="sxs-lookup"><span data-stu-id="80059-129">See also</span></span>



[<span data-ttu-id="80059-130">Каноническое свойство PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="80059-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="80059-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="80059-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80059-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="80059-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80059-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="80059-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80059-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="80059-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

