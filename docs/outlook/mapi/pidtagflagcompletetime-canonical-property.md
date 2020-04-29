---
title: Каноническое свойство PidTagFlagCompleteTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5dd0d4c19f30e189218b1aeddd333df58e42102a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316291"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="bcafa-103">Каноническое свойство PidTagFlagCompleteTime</span><span class="sxs-lookup"><span data-stu-id="bcafa-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="bcafa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcafa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcafa-105">Указывает дату и время в формате UTC, когда объект Message был помечен как завершенный.</span><span class="sxs-lookup"><span data-stu-id="bcafa-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcafa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bcafa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcafa-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="bcafa-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="bcafa-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bcafa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcafa-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="bcafa-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="bcafa-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bcafa-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcafa-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bcafa-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="bcafa-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bcafa-112">Area:</span></span>  <br/> |<span data-ttu-id="bcafa-113">Разное</span><span class="sxs-lookup"><span data-stu-id="bcafa-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcafa-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bcafa-114">Remarks</span></span>

<span data-ttu-id="bcafa-115">Это свойство удаляется, если объект Message не помечен как завершенный.</span><span class="sxs-lookup"><span data-stu-id="bcafa-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="bcafa-116">Наименьшее разрешение времени должно быть в минутах (значение должно быть кратно 600 000 000).</span><span class="sxs-lookup"><span data-stu-id="bcafa-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="bcafa-117">Это свойство не должно существовать, если объект является объектом, связанным с собранием, и он не должен существовать в объекте Task.</span><span class="sxs-lookup"><span data-stu-id="bcafa-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcafa-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bcafa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcafa-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bcafa-119">Protocol specifications</span></span>

<span data-ttu-id="bcafa-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcafa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcafa-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bcafa-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcafa-122">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcafa-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcafa-123">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="bcafa-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcafa-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bcafa-124">Header files</span></span>

<span data-ttu-id="bcafa-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="bcafa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcafa-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bcafa-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcafa-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="bcafa-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bcafa-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="bcafa-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcafa-129">См. также</span><span class="sxs-lookup"><span data-stu-id="bcafa-129">See also</span></span>



[<span data-ttu-id="bcafa-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bcafa-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcafa-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="bcafa-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcafa-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bcafa-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcafa-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bcafa-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

