---
title: Каноническое свойство PidLidCommonEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 97d6ef6343cedb6fbed93cccda9f65476bb73f4f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393308"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="c5a16-103">Каноническое свойство PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="c5a16-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="c5a16-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5a16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5a16-105">Представляет дату и время сообщения.</span><span class="sxs-lookup"><span data-stu-id="c5a16-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5a16-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c5a16-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5a16-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="c5a16-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="c5a16-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c5a16-108">Property set:</span></span>  <br/> |<span data-ttu-id="c5a16-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c5a16-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c5a16-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c5a16-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c5a16-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="c5a16-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="c5a16-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c5a16-112">Data type:</span></span>  <br/> |<span data-ttu-id="c5a16-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c5a16-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c5a16-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c5a16-114">Area:</span></span>  <br/> |<span data-ttu-id="c5a16-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="c5a16-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5a16-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c5a16-116">Remarks</span></span>

<span data-ttu-id="c5a16-117">Это свойство показывает время окончания для элемента.</span><span class="sxs-lookup"><span data-stu-id="c5a16-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="c5a16-118">Это должно быть больше или равно значению свойства **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c5a16-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c5a16-119">Это значение должно быть эквивалент по Гринвичу (UTC) свойство **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c5a16-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5a16-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c5a16-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5a16-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c5a16-121">Protocol specifications</span></span>

<span data-ttu-id="c5a16-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5a16-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5a16-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c5a16-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5a16-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5a16-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5a16-125">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="c5a16-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c5a16-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5a16-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5a16-127">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="c5a16-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5a16-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c5a16-128">Header files</span></span>

<span data-ttu-id="c5a16-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5a16-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5a16-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c5a16-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5a16-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c5a16-131">See also</span></span>



[<span data-ttu-id="c5a16-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a16-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5a16-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a16-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5a16-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a16-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5a16-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c5a16-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

