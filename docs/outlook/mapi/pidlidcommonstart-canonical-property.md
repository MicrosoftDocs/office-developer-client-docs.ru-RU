---
title: Каноническое свойство PidLidCommonStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonStart
api_type:
- COM
ms.assetid: d999852d-ce98-4c3c-a772-87f5db4aa04e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec7c213d7eec9ab0ef5766442e3de59a24811d37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345488"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="5a575-103">Каноническое свойство PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="5a575-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="5a575-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a575-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a575-105">Представляет дату начала и время сообщения.</span><span class="sxs-lookup"><span data-stu-id="5a575-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a575-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5a575-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a575-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="5a575-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="5a575-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5a575-108">Property set:</span></span>  <br/> |<span data-ttu-id="5a575-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5a575-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5a575-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5a575-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5a575-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="5a575-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="5a575-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5a575-112">Data type:</span></span>  <br/> |<span data-ttu-id="5a575-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5a575-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5a575-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5a575-114">Area:</span></span>  <br/> |<span data-ttu-id="5a575-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="5a575-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a575-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a575-116">Remarks</span></span>

<span data-ttu-id="5a575-117">Это свойство указывает время начала элемента.</span><span class="sxs-lookup"><span data-stu-id="5a575-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="5a575-118">Оно должно быть меньше или равно значению свойства **dispidCommonEnd** [(PidLidCommonEnd).](pidlidcommonend-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5a575-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="5a575-119">Значение этого свойства должно быть эквивалентом согласованного универсального времени (UTC) свойства **dispidTaskStartDate** [(PidLidTaskStartDate).](pidlidtaskstartdate-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5a575-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a575-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5a575-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a575-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5a575-121">Protocol specifications</span></span>

<span data-ttu-id="5a575-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a575-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a575-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="5a575-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a575-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a575-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a575-125">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="5a575-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5a575-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a575-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a575-127">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="5a575-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a575-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5a575-128">Header files</span></span>

<span data-ttu-id="5a575-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a575-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a575-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5a575-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a575-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5a575-131">See also</span></span>



[<span data-ttu-id="5a575-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a575-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a575-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a575-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a575-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5a575-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a575-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5a575-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

