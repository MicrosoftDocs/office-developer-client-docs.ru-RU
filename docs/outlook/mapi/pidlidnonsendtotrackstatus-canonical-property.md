---
title: Каноническое свойство PidLidNonSendToTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bdfbd553e130a4e463017168a76dc94fc0df827b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331369"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="ae40d-103">Каноническое свойство PidLidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="ae40d-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ae40d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae40d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae40d-105">Содержит значение для каждого участника, перечисленное в свойстве **dispidNonSendableTo** [(PidLidNonSendableTo).](pidlidnonsendableto-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ae40d-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae40d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ae40d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae40d-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="ae40d-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="ae40d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ae40d-108">Property set:</span></span>  <br/> |<span data-ttu-id="ae40d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ae40d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ae40d-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ae40d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ae40d-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="ae40d-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="ae40d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ae40d-112">Data type:</span></span>  <br/> |<span data-ttu-id="ae40d-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="ae40d-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="ae40d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ae40d-114">Area:</span></span>  <br/> |<span data-ttu-id="ae40d-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="ae40d-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae40d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae40d-116">Remarks</span></span>

<span data-ttu-id="ae40d-117">Это свойство требуется только при заданном **свойстве dispidNonSendableTo.**</span><span class="sxs-lookup"><span data-stu-id="ae40d-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="ae40d-118">Количество значений в этом свойстве должно равняться числу значений в **dispidNonSendableTo**.</span><span class="sxs-lookup"><span data-stu-id="ae40d-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="ae40d-119">Каждое PT_LONG в этом свойстве соответствует участнику в свойстве **dispidNonSendableTo** с тем же индексом.</span><span class="sxs-lookup"><span data-stu-id="ae40d-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ae40d-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ae40d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ae40d-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ae40d-121">Protocol specifications</span></span>

<span data-ttu-id="ae40d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae40d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae40d-123">Предоставляет определение набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="ae40d-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ae40d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae40d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae40d-125">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="ae40d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ae40d-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="ae40d-126">Header files</span></span>

<span data-ttu-id="ae40d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae40d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae40d-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ae40d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae40d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ae40d-129">See also</span></span>



[<span data-ttu-id="ae40d-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ae40d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae40d-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ae40d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae40d-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ae40d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae40d-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="ae40d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

