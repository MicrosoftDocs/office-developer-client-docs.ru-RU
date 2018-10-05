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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387134"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="58d02-103">Каноническое свойство PidTagFlagCompleteTime</span><span class="sxs-lookup"><span data-stu-id="58d02-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="58d02-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58d02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58d02-105">Указывает дату и время в формате универсального времени (UTC), который объект message был помечен как выполненное.</span><span class="sxs-lookup"><span data-stu-id="58d02-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58d02-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="58d02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58d02-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="58d02-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="58d02-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="58d02-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58d02-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="58d02-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="58d02-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="58d02-110">Data type:</span></span>  <br/> |<span data-ttu-id="58d02-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="58d02-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="58d02-112">Область:</span><span class="sxs-lookup"><span data-stu-id="58d02-112">Area:</span></span>  <br/> |<span data-ttu-id="58d02-113">Разное</span><span class="sxs-lookup"><span data-stu-id="58d02-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58d02-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="58d02-114">Remarks</span></span>

<span data-ttu-id="58d02-115">Это свойство удаляется, если объект сообщения не имеет флаг завершена.</span><span class="sxs-lookup"><span data-stu-id="58d02-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="58d02-116">Разрешение наименьшее время должно быть минут (значение должно быть множитель 600,000,000).</span><span class="sxs-lookup"><span data-stu-id="58d02-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="58d02-117">Это свойство не должна существовать, если объект является объектом, связанные с собрания и не должно быть для объекта задачи.</span><span class="sxs-lookup"><span data-stu-id="58d02-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="58d02-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="58d02-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58d02-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="58d02-119">Protocol specifications</span></span>

<span data-ttu-id="58d02-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58d02-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58d02-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="58d02-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58d02-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58d02-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58d02-123">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="58d02-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58d02-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="58d02-124">Header files</span></span>

<span data-ttu-id="58d02-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58d02-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="58d02-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="58d02-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="58d02-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="58d02-127">Mapitags.h</span></span>
  
> <span data-ttu-id="58d02-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="58d02-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58d02-129">См. также</span><span class="sxs-lookup"><span data-stu-id="58d02-129">See also</span></span>



[<span data-ttu-id="58d02-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="58d02-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58d02-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="58d02-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58d02-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="58d02-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58d02-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="58d02-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

