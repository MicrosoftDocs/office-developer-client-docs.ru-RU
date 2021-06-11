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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345502"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="4f916-103">Каноническое свойство PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="4f916-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="4f916-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f916-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f916-105">Представляет даты и время окончания сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f916-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f916-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4f916-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f916-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="4f916-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="4f916-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4f916-108">Property set:</span></span>  <br/> |<span data-ttu-id="4f916-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4f916-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4f916-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4f916-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4f916-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="4f916-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="4f916-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4f916-112">Data type:</span></span>  <br/> |<span data-ttu-id="4f916-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4f916-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4f916-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4f916-114">Area:</span></span>  <br/> |<span data-ttu-id="4f916-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="4f916-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f916-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f916-116">Remarks</span></span>

<span data-ttu-id="4f916-117">Это свойство указывает время окончания элемента.</span><span class="sxs-lookup"><span data-stu-id="4f916-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="4f916-118">Оно должно быть больше или равно значению свойства **dispidCommonStart** [(PidLidCommonStart).](pidlidcommonstart-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4f916-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="4f916-119">Это значение должно быть эквивалентом согласованного универсального времени (UTC) свойства **dispidTaskDueDate** [(PidLidTaskDueDate).](pidlidtaskduedate-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4f916-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f916-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4f916-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f916-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4f916-121">Protocol specifications</span></span>

<span data-ttu-id="4f916-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f916-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f916-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="4f916-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f916-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f916-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f916-125">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="4f916-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4f916-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f916-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f916-127">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="4f916-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f916-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="4f916-128">Header files</span></span>

<span data-ttu-id="4f916-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f916-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f916-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4f916-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f916-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4f916-131">See also</span></span>



[<span data-ttu-id="4f916-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4f916-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f916-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4f916-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f916-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4f916-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f916-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="4f916-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

