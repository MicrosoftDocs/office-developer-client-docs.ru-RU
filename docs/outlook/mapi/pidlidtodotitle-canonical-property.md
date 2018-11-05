---
title: Каноническое свойство PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397585"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="b27a1-103">Каноническое свойство PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="b27a1-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="b27a1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b27a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b27a1-105">Содержит текст, при этом задаваемый пользователем для идентификации этот объект сообщения в списке дел консолидированной среды.</span><span class="sxs-lookup"><span data-stu-id="b27a1-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b27a1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b27a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b27a1-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="b27a1-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="b27a1-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b27a1-108">Property set:</span></span>  <br/> |<span data-ttu-id="b27a1-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b27a1-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b27a1-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b27a1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b27a1-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="b27a1-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="b27a1-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b27a1-112">Data type:</span></span>  <br/> |<span data-ttu-id="b27a1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b27a1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b27a1-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b27a1-114">Area:</span></span>  <br/> |<span data-ttu-id="b27a1-115">Task</span><span class="sxs-lookup"><span data-stu-id="b27a1-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b27a1-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b27a1-116">Remarks</span></span>

<span data-ttu-id="b27a1-117">Это свойство не должен задаваться на задачу.</span><span class="sxs-lookup"><span data-stu-id="b27a1-117">This property must not be set on a task.</span></span> <span data-ttu-id="b27a1-118">Для указания пустой свойство, не задавайте это свойство строку нулевой длины, но вместо этого удалите его.</span><span class="sxs-lookup"><span data-stu-id="b27a1-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="b27a1-119">Когда пометка объекта message и свойство не существует, клиент указывайте значение **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) для данного свойства.</span><span class="sxs-lookup"><span data-stu-id="b27a1-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="b27a1-120">В списке дел консолидированной Если это свойство не существует, клиент следует заменить значение свойства **PR_NORMALIZED_SUBJECT** при отображении этого свойства в списке дел.</span><span class="sxs-lookup"><span data-stu-id="b27a1-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="b27a1-121">Для объекта черновика сообщения Если клиент реализует флаги отправителя, это свойство должно быть присвоено совпадает со значением **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b27a1-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b27a1-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b27a1-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b27a1-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b27a1-123">Protocol specifications</span></span>

<span data-ttu-id="b27a1-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b27a1-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b27a1-125">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server</span><span class="sxs-lookup"><span data-stu-id="b27a1-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="b27a1-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b27a1-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b27a1-127">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="b27a1-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b27a1-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b27a1-128">Header files</span></span>

<span data-ttu-id="b27a1-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b27a1-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="b27a1-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b27a1-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b27a1-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b27a1-131">See also</span></span>



[<span data-ttu-id="b27a1-132">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="b27a1-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="b27a1-133">Каноническое свойство PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="b27a1-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="b27a1-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b27a1-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b27a1-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b27a1-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b27a1-136">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="b27a1-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b27a1-137">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="b27a1-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

