---
title: Каноническое свойство PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8086bc3ea35fdbb4e0f7758b7931e305259a3a9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578670"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="dae6d-103">Каноническое свойство PidTagSwappedToDoData</span><span class="sxs-lookup"><span data-stu-id="dae6d-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="dae6d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dae6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dae6d-105">Поддерживает второй набор значений свойств, которые не влияют на отмеченного состояние объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="dae6d-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dae6d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dae6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dae6d-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="dae6d-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="dae6d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dae6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dae6d-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="dae6d-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="dae6d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dae6d-110">Data type:</span></span>  <br/> |<span data-ttu-id="dae6d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dae6d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dae6d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dae6d-112">Area:</span></span>  <br/> |<span data-ttu-id="dae6d-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="dae6d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dae6d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dae6d-114">Remarks</span></span>

<span data-ttu-id="dae6d-115">Если поддерживается флаги отправителя или напоминания отправителя будет действовать как флаг дополнительного места хранения данных, эта структура предоставляет расположение, в котором хранятся все свойства, относящиеся к информационные Пометка протокола, которые поддерживаются в флаги отправителя и всех свойства относящиеся к протокола параметры напоминания, которые поддерживаются в отправителя напоминаний без предоставление доступа к сведениям о напоминание отправителя в список получателей сообщения или флаг отправителя.</span><span class="sxs-lookup"><span data-stu-id="dae6d-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="dae6d-116">Аналогично эта структура предоставляет расположение, в котором хранятся все свойства относящиеся к информационного протокола Пометка, поддерживаемые в получателей флаги и свойства, относящиеся к протокола параметры напоминания, которые поддерживаются в получателя напоминания на ранее отправленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="dae6d-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="dae6d-117">Дополнительные сведения об этом свойстве можно [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dae6d-117">For more information about this property, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dae6d-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dae6d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dae6d-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dae6d-119">Protocol specifications</span></span>

<span data-ttu-id="dae6d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dae6d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dae6d-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dae6d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dae6d-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dae6d-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dae6d-123">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="dae6d-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="dae6d-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dae6d-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dae6d-125">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="dae6d-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dae6d-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="dae6d-126">Header files</span></span>

<span data-ttu-id="dae6d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dae6d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="dae6d-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dae6d-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="dae6d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dae6d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="dae6d-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="dae6d-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dae6d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="dae6d-131">See also</span></span>



[<span data-ttu-id="dae6d-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dae6d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dae6d-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dae6d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dae6d-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dae6d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dae6d-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dae6d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

